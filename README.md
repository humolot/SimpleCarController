# SimpleCarController

## Overview
`SimpleCarController` is a Unity script designed for simple 3D car control. It provides features such as:

- Basic car movement (acceleration, deceleration, turning, and braking).
- Camera follow system.
- Brake lights, reverse lights, and turn signals.
- Engine audio effects.
- Fuel consumption system.

> **Note**: This script does not include physics-based car mechanics but focuses on lightweight, straightforward functionality.

### Unity Version
The script is compatible with Unity 2022 or newer.

---

## Features
- **Movement Settings**: Customize max speed, acceleration, deceleration, and turning speed.
- **Camera System**: Smooth following camera with adjustable offset.
- **Lighting**: Brake lights, reverse lights, and turn signals.
- **Engine Audio**: Includes idle, acceleration, and braking sounds.
- **Fuel System**: Tracks fuel consumption with visual representation via a UI bar.

---

## Setup Instructions
Follow these steps to integrate the `SimpleCarController` into your Unity project.

### Step 1: Add the Script
1. Create a `Car` GameObject in your scene.
2. Attach the `SimpleCarController` script to the `Car` GameObject.

### Step 2: Configure Wheels
1. Create or assign wheel objects as child GameObjects of the `Car`.
2. In the `Wheel Settings` section of the script, drag and drop the wheel Transforms into the `Wheels` array.

### Step 3: Configure Lights
1. Create or assign light GameObjects for:
   - Brake lights (e.g., rear lights).
   - Reverse lights.
   - Turn signals (left and right).
2. In the `Car Lights` section, drag and drop the respective Light components into the corresponding fields.
3. Customize light colors and intensity as needed.

### Step 4: Configure Camera
1. Assign the `Camera` Transform to the `Camera Settings` > `Camera Transform` field.
2. Adjust the `Camera Offset` to position the camera relative to the car.
3. Tweak the `Camera Smooth` value for smoother transitions.

### Step 5: Configure Audio
1. Create or assign `AudioSource` components to the car.
2. Drag and drop the `AudioSource` components into the following fields:
   - `Engine Audio Source`
   - `Engine Accel Source`
   - `Brake Audio Source`
3. Assign appropriate audio clips (e.g., idle loop, acceleration loop, and braking sound).

### Step 6: Configure Fuel System
1. Create a UI `Image` element for the fuel bar.
2. Drag and drop the UI element into the `Gasoline Settings` > `Fuel Bar` field.
3. Adjust `Max Fuel` and `Fuel Consumption Rate` as needed.

---

## How to Use
- **Start Engine**: Press `E` to toggle the car engine on or off.
- **Accelerate/Brake**: Use the `Vertical` axis (default: W/S keys) to accelerate or decelerate.
- **Steering**: Use the `Horizontal` axis (default: A/D keys) to steer the car.
- **Braking**: Press `Space` to brake and activate brake lights.
- **Turn Signals**: The turn signals blink automatically during turning.
- **Fuel Refueling**: Call the `Refuel(float amount)` method to refuel the car.

---

## Script Details
### Serialized Fields
- **Movement Settings**:
  - `maxSpeed`: Maximum car speed.
  - `acceleration`: Rate of acceleration.
  - `deceleration`: Rate of deceleration.
  - `turnSpeed`: Turning speed.
  - `brakingForce`: Force applied when braking.

- **Wheel Settings**:
  - `wheels`: Array of wheel Transforms for rotation animation.
  - `wheelRotationSpeed`: Speed of wheel rotation.

- **Camera Settings**:
  - `cameraTransform`: Transform of the camera following the car.
  - `cameraOffset`: Offset position of the camera relative to the car.
  - `cameraSmooth`: Smoothness of the camera movement.

- **Car Lights**:
  - `leftBrakeLight`, `rightBrakeLight`: Rear lights activated during braking.
  - `leftTurnLight`, `rightTurnLight`: Turn signal lights.
  - `turnLightBlinkInterval`: Interval for turn signal blinking.
  - `turnLightColor`, `brakeLightColor`: Colors of the lights.
  - `lightIntensity`: Intensity of the lights.

- **Audio Settings**:
  - `engineStartSound`, `engineStopSound`: Audio clips for engine start/stop.
  - `engineIdleLoop`, `engineAccelLoop`: Looping audio clips for idle and acceleration.
  - `minEnginePitch`, `maxEnginePitch`: Pitch variation for engine sounds.

- **Fuel System**:
  - `fuelBar`: UI element for fuel representation.
  - `maxFuel`: Maximum fuel capacity.
  - `fuelConsumptionRate`: Rate of fuel consumption.

---

## Limitations
- This script does not include advanced physics-based car mechanics.
- Suitable for simple arcade-style car control, not simulation.

---

## Version History
### v0.0.1
- Initial release with basic car movement, lighting, audio, and fuel system.

---

## Credits
Created by **Humolot**

GBX Studios
