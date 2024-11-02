#include <SD.h>
#include <SPI.h>
#include <TMRpcm.h> // Include the library for audio playback

TMRpcm audio; // Create an audio object

const int trigPin = 8;  // Trigger pin for the HC-SR04
const int echoPin = 7;  // Echo pin
const int speakerPin = 9; // Speaker pin
const int ledPins[] = {2, 3, 4}; // LED pins
const int numLEDs = sizeof(ledPins) / sizeof(ledPins[0]);
const int sdPin = 10; // CS pin for SD card set to 10

enum DistanceCategory {NONE, FAR, MEDIUM, CLOSE};
DistanceCategory currentCategory = NONE; // Track current distance category

unsigned long lastTriggerTime = 0; // To track last playback time
const unsigned long debounceTime = 3000; // 3 seconds debounce time to prevent frequent retriggering

void setup() {
    Serial.begin(9600);
   
    pinMode(trigPin, OUTPUT);
    pinMode(echoPin, INPUT);
    pinMode(speakerPin, OUTPUT);
    for (int i = 0; i < numLEDs; i++) {
        pinMode(ledPins[i], OUTPUT);
    }
   
    audio.speakerPin = speakerPin; // Set the speaker pin
   
    if (!SD.begin(sdPin)) {
        Serial.println("SD card initialization failed!");
        return;
    }
    Serial.println("SD card initialized.");
}

void loop() {
    long duration, distance;
    digitalWrite(trigPin, LOW);
    delayMicroseconds(2);
    digitalWrite(trigPin, HIGH);
    delayMicroseconds(10);
    digitalWrite(trigPin, LOW);

    duration = pulseIn(echoPin, HIGH);
    distance = (duration * 0.034 / 2); // Convert to cm
    Serial.println(distance);

    DistanceCategory newCategory;

    if (distance >= 15 && distance <= 40) {
        newCategory = FAR;
    } else if (distance >= 5 && distance < 15) {
        newCategory = MEDIUM;
    } else if (distance < 5) {
        newCategory = CLOSE;
    } else {
        newCategory = NONE;
    }

    // Check if the distance category has changed and debounce
    if (newCategory != currentCategory && (millis() - lastTriggerTime) > debounceTime) {
        currentCategory = newCategory;
        lastTriggerTime = millis(); // Update last trigger time

        // Stop any currently playing audio before starting new audio
        if (audio.isPlaying()) {
            audio.stopPlayback();
        }

        switch (currentCategory) {
            case FAR:
                activateLEDs(1);
                playAudio("lig"); // Play random file for far distance
                break;
            case MEDIUM:
                activateLEDs(2);
                playAudio("med"); // Play random file for medium distance
                break;
            case CLOSE:
                activateLEDs(3);
                playAudio("hig"); // Play random file for close distance
                break;
            default:
                deactivateLEDs();
                break;
        }
    }

    delay(100); // Short delay to avoid excessive checking
}

void activateLEDs(int count) {
    for (int i = 0; i < numLEDs; i++) {
        digitalWrite(ledPins[i], i < count ? HIGH : LOW);
    }
}

void deactivateLEDs() {
    for (int i = 0; i < numLEDs; i++) {
        digitalWrite(ledPins[i], LOW);
    }
}

void playAudio(const char* prefix) {
    int randomIndex = random(1, 4); // Generate a random number between 1 and 3
    String fileName = String(prefix) + String(randomIndex) + ".wav"; // Construct file name with random number

    Serial.print("Attempting to play file: ");
    Serial.println(fileName); // Print file path to check it

    if (SD.exists(fileName.c_str())) { // Check if file exists
        audio.play(fileName.c_str()); // Play the audio file
        Serial.print("Playing: ");
        Serial.println(fileName);
    } else {
        Serial.print("File not found: ");
        Serial.println(fileName);
    }
}
