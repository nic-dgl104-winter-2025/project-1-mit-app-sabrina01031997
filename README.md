<div id="readme-top"></div>

# MIT App Inventor Project

<!--
*** README.md Reference: https://github.com/othneildrew/Best-README-Template/tree/master
-->

<!-- PROJECT LOGO -->
<div align="center">
   <a href="https://github.com/othneildrew/Best-README-Template">
    <img src="assets/logo.png" alt="Logo" width="180">
  </a><h3>Fitness Exercise App</h3> <p> A simple fitness exercise app built using MIT App Inventor. </p> </div>

<!-- ABOUT THE PROJECT -->

## About The Project

The Fitness Exercise App is a mobile application designed for individuals who want to stay active and fit through structured exercise routines. It provides a guided workout experience with visual demonstrations, audio instructions and countdown timers to keep users engaged and motivated.

The app is built using MIT App Inventor, incorporating Text-to-Speech (TTS) for verbal workout instructions, visual exercise demonstrations, and a 30-second countdown timer to help users stay on track. Users can choose from three exercise categories, allowing them to customize their fitness routine based on their personal goals.

This project was developed with the goal of creating a simple yet effective fitness assistant, removing the need for printed workout guides or external trainers. By integrating audio, images and timers, this app ensures that users get a seamless exercise experience.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- KEY FEATURES -->

## Key Features
### Voice-Guided Workouts
- The app integrates Text-To-Speech (TTS) to provide verbal exercise instructions.
- Users can listen to instructions while focusing on the workout.

### Step-by-Step Exercise Demonstrations
- Each workout category includes high-quality images to guide users.
- Helps in understanding exercise form and technique.

### 30-Second Countdown Timer
- A built-in timer runs 30 seconds per exercise.
- Notifies the user when the time is up.

### User-Friendly Interface
- Simple layout designed for ease of use.
- Large buttons & clear navigation make the app accessible for all users.

### Workout Categories
Users can choose from three different fitness categories:
1. **Core Burner** – Focused on core and abdominal exercises.
2. **Weight Loss** – Includes cardio-based fat-burning exercises.
3. **Weight Gain** – Designed for muscle-building and strength training.

Each category has a dedicated screen where users can view the exercise details and start their workout.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- APP SCREEN AND UI DESIGN -->

## App Screens and UI Design

### **1️⃣ Home Screen**
- Serves as the main navigation hub.
- Users can select a workout category.
- Features a clean and structured layout.

<img src="assets/home.jpg" alt="Home Screen" width="500">

---
### 2️⃣ Exercise Category Screen
- Users choose between Core Burner, Weight Loss, or Weight Gain exercises.
- Large, easy-to-press category buttons.
- Displays preview images of exercises.

<img src="assets/categories.jpg" alt="Home Screen" width="500">

---
### 3️⃣ Workout Screens
- Displays selected exercises.
- Features step-by-step image guidance.
- Provides audio instructions via Text-To-Speech.
- Runs a 30-second countdown timer.
- Shows a completion message at the end of the workout.

<img src="assets/workout.jpg" alt="Core Burn Exercise Screen"width="500">
---
<img src="assets/workout-2.jpg" alt="Weight Loss Exercise Screen" width="500">
---
<img src="assets/workout-3.jpg" alt="Weight Gain Exercise Screen" width="500">



<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- CORE COMPONENT USED -->

## Core Components Used

### UI Components (Designer View)  
These are the visible components that make up the user interface of the Fitness Exercise App.

| **Component**              | **Name(s)**                             | **Purpose** |
|---------------------------|----------------------------------------|------------|
| **Screen**               | `Screen1`                               | The **main app screen** where all interactions occur. |
| **Labels**               | `Label1 - Label13`                      | Display **exercise instructions, countdown timers, and status messages**. |
| **Buttons**              | `Button1 - Button4`                     | Allow users to **navigate between screens** and **select exercises**. |
| **Images**               | `Image1 - Image9`                       | Provide **visual demonstrations** of exercises. |
| **TextBoxes**            | `TextBox2 - TextBox11`                  | Allow **users to input information** under images. |
| **Vertical Arrangements** | `VerticalArrangement1 - VerticalArrangement11` | **Organize UI elements** into structured sections. |

---

### **🔧 Non-Visible Components (Blocks)**  
These components are **not directly visible** but handle the app's logic and **functionalities**.

| **Component**               | **Name(s)**                           | **Purpose** |
|-----------------------------|--------------------------------------|------------|
| **Clock (9 Instances)**      | `Clock1 - Clock9`                    | **Handles countdown timers** for exercises. |
| **Text-To-Speech (3 Instances)** | `TextToSpeech1 - TextToSpeech3` | **Guides users through workouts** using voice instructions. |

---

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- CODE BLOCK SNAPSHOT -->

## **Code Block Snapshots**
### **1️⃣ Workout Selection Logic**
This MIT App Inventor block code ensures that users can select an exercise and navigate to the correct screen.

#### **Code Block Screenshot:**
<img src="assets/Screenshot-1.png" alt="Home Screen" width="500">

### **2️⃣ Core Burn Exercise Timer & Completion Logic**
This block controls the **Core Burn workout timer**, ensuring that:
- The exercise starts when selected.
- Starts a countdown timer for the exercise.
- The Text-To-Speech provides instructions.
- Provides alert before 3 seconds left
- A completion message appears after the timer finishes.
- Automatically switches to the next exercise after completion.
- After the completion of last exercise of Core Burn it returns to the landing page.

#### **Code Block Screenshot:**
<img src="assets/Screenshot-2.png" alt="Home Screen" width="500">

### **3️⃣ Weight Loss Exercise Timer & Completion Logic**
- The exercise starts when selected.
- Announces progress via voice prompts.
- A completion message appears after the timer finishes.
- Transitions to the next step smoothly.
- After the completion of last exercise of Weight Loss it returns to the landing page.

#### **Code Block Screenshot:**
<img src="assets/Screenshot-3.png" alt="Home Screen" width="500">

### **4️⃣ Weight Gain Exercise Timer & Completion Logic**
- Users can start the Weight Gain workout.
- The countdown begins as soon as the workout starts.
- Text-To-Speech guidance is given for the duration of the workout.
- The user is notified upon completion.
- After the completion of last exercise of Weight Gain it returns to the landing page.

#### **Code Block Screenshot:**
<img src="assets/Screenshot-4.png" alt="Home Screen" width="500">

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- DEVELOPMENT PROCESS -->

## **Development Process**
### **Challenges & Solutions**
### **1️⃣ Ensuring UI Simplicity & Readability**
Initially, the UI lacked proper structure, making navigation confusing.  
**Solution:**  
- Used Vertical Arrangements to group related components, ensuring a clean layout.  
- Ensured buttons were large, visible, and color-coded for quick identification.  
- Used consistent font sizes to maintain readability across different screen sizes.  

### **2️⃣ Synchronizing Timer & Text-To-Speech**
Initially, the Text-To-Speech component finished speaking before the countdown timer reached zero.  
**Solution:**  
- Adjusted timing logic so that the speech aligned with exercise durations.  
- Implemented a 3-second countdown warning before transitioning to the next exercise.  
- Used Text-To-Speech prompts at key moments (start, mid, and end of an exercise) for better guidance.  

### **3️⃣ Debugging Issues with Clock Component**
Encountered issues where timers overlapped, causing countdown inconsistencies.  
**Solution:**  
- Ensured only one clock timer runs at a time by disabling all others before starting a new exercise.  
- Used conditional checks to prevent negative countdown values.  
- Implemented reset logic so each timer restarts correctly at the beginning of a new workout.  

### **4️⃣ Fixing iOS Compatibility Issues (GIF Images)**
Initially, the app used GIF images for workout demonstrations, but iOS does not support GIF playback in MIT App Inventor.  
**Solution:**  
- Replaced GIFs with static images, ensuring compatibility across both Android and iOS.  
- Improved performance by reducing image file sizes, leading to a smoother user experience.  

### **5️⃣ Improving Code Efficiency (Reducing Repetitive Blocks)**
The first version of the app contained repetitive block structures for each workout timer.  
**Solution:**  
- Used procedures (custom functions) to eliminate duplicate code.  
- Implemented a universal timer function that handles any exercise category dynamically.  
- This change reduced block clutter and made debugging much easier.  

<!-- FINAL OUTCOME -->

## **Final Outcome**
- UI is simple, clear, and structured.  
- Timers and Text-To-Speech are synchronized for a seamless workout experience.  
- No more overlapping timers or negative countdown issues.  
- The app is fully compatible with both Android and iOS.  

<!-- FUTURE ENHANCEMENTS -->

## **Future Enhancements**
- Add a progress tracking feature to log completed workouts.  
- Allow users to set custom workout durations based on personal - preferences.  
- Introduce a Dark Mode UI for better accessibility.  
 
<p align="right">(<a href="#readme-top">Back to top</a>)</p>

<!-- ACKNOWLEDGMENTS -->

## **Acknowledgments**
This project was inspired by fitness training principles and uses MIT App Inventor features for a seamless workout experience.

- **[MIT App Inventor](https://appinventor.mit.edu/)** - The primary tool for developing the app.
- **[Text-to-Speech API](https://cloud.google.com/text-to-speech/)** - Used for voice-guided workouts.
- **[YouTube Fitness Workouts](https://youtu.be/OEEm7RFv_wQ?si=mi1ZLDB7RXdpfhwX)** - Referenced for exercise descriptions.


<p align="right">(<a href="#readme-top">back to top</a>)</p>








