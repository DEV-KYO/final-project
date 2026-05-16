# User Manual & README
### EagleNav Project
**Team:** Moh's Eagles  
**Date:** May 15, 2026  

---

## Jira Sprint Board
**Link:** [EagleNav Jira Board](https://calstatela-cs3338-eaglenav.atlassian.net/jira/software/projects/KAN/boards/

## Formal Objective Breakdown
EagleNav is an accessible, augmented reality campus navigation platform. The primary objectives are:
1. Provide highly accurate, closest-entrance pedestrian routing for the CSULA campus.
2. Deliver multimodal guidance (audio, haptic, visual) to support students with visual or physical impairments.
3. Integrate real-time campus events and spatial awareness features.
4. Operate with strict data privacy, keeping computations and location data on-device where possible.

## Why This Software Matters
Standard navigation apps like Google Maps route users to the "centroid" or middle of a building, often leaving visually impaired students stranded in parking lots or facing inaccessible staircases. EagleNav matters because it utilizes high-precision local data to route users specifically to ADA-accessible doors, removing physical barriers to education and fostering campus independence.

## Installation & Access Instructions

### Prerequisites
* Docker and Docker Compose installed on your host machine.
* Flutter SDK (v3.0+) and Dart installed for the mobile client.
* Android Studio (for Android emulation) or Xcode (for iOS emulation).

### Backend Setup (Docker)
1. Clone the GitHub repository to your local machine.
2. Open a terminal or developer command prompt in the root directory.
3. Run the command: `docker-compose up -d`
4. The Valhalla routing engine will initialize on port 8002, and the simulated Node.js API will initialize on port 3000.

### Frontend Setup (Mobile App)
1. Navigate to the `/mobile` directory in the repository.
2. Run `flutter pub get` to install all required dependencies (e.g., flutter_map, tflite).
3. Connect a physical mobile device or launch an emulator.
4. Run `flutter run` to build and launch the application.
