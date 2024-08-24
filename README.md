# Gemma Android Demo

## Overview
 This project uses Jetpack Compose for the UI and includes a chat interface powered by a local inference model: Namely Gemma 2B model 

## Prerequisites
- Android Studio Flamingo or later
- JDK 11 or later
- Android device or emulator running Android 7.0 (API level 24) or higher

## Download instructions for Gemma 2B Model: 

### MediaPipe LLM Inference API

The LLM Inference API enables you to run large language models directly on your device and is capable of performing a wide range of tasks such as text generation, question-answering, document summarization, etc.

### Supported Models
Below are some of the open models supported by the LLM Inference Task:
- Gemma 2B
- Phi-2
- Falcon-RW-1B
- StableLM-3B

### Download and Setup Gemma 2B IT CPU-based Model with 4-bit Quantization:

### Step 1: Download the Model
Download the Gemma 2B IT CPU-based model with 4-bit quantization from [Hugging Face](https://huggingface.co/google/gemma-2b-it).

### Step 2: Setup Android Debug Bridge (ADB)
Android Debug Bridge (ADB) is a command-line tool that helps you communicate between the computer and device. Connect your Android phone with your computer and open command prompt/terminal.

### Step 3: Initialize ADB Shell
```
adb shell
```

### Step 4: Remove Any Previously Loaded Model
```
rm -r /data/local/tmp/llm/
exit
```

### Step 5: Push the Model to Your Android Phone
```
adb push /data/local/tmp/llm/gemma-2b-it-cpu-int4.bin
```

The above command creates a new directory locally on your phone from which the model will be invoked. 
For more information on the Gemma model, visit the [Gemma Model Card on Hugging Face](https://huggingface.co/google/gemma-2b-it).

## Setup Instructions

### 1. Clone the Repository

sh
git clone https://github.com/yourusername/GemmaDemoWithCouchBase.git

### 2. Open the Project in Android Studio
1. Launch Android Studio.
2. Select `Open an existing project`.
3. Navigate to the cloned repository and select the `GemmaDemoWithCouchBase` directory.

### 3. Configure the Project
Ensure that you have the necessary SDKs and tools installed:
1. Open the `build.gradle.kts` file in the root directory and sync the project.
2. Make sure you have the required SDKs installed. You can check this in the `File > Project Structure > SDK Location`.

### 4. Build the Project
1. Click on the `Build` menu.
2. Select `Make Project` or press `Ctrl+F9`.

### 5. Run the Project
1. Connect your Android device or start an emulator.
2. Click on the `Run` menu.
3. Select `Run 'app'` or press `Shift+F10`.

## Project Structure
- `app/src/main/java/com/example/scigemma/`: Contains the main Kotlin source files.
- `app/src/main/res/`: Contains the resource files like layouts, strings, and drawables.
- `app/build.gradle.kts`: Contains the Gradle build configuration for the app module.
- `settings.gradle.kts`: Contains the settings for the Gradle project.
- `gradle/wrapper/gradle-wrapper.properties`: Contains the configuration for the Gradle wrapper.

## Key Files
- `MainActivity.kt`: The main entry point of the application.
- - `build.gradle.kts`: The Gradle build script for the app module.
 
  - 
## Dependencies
The project uses several dependencies, including:
- AndroidX libraries for core functionality and lifecycle management.
- Jetpack Compose for UI.
- MediaPipe for local inference.

You can find the complete list of dependencies in the `build.gradle.kts` file.
