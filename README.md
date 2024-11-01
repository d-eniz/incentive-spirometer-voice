# Arduino-Enabled Incentive Spirometer with Voice Feedback

This project is an Arduino-enabled incentive spirometer designed specifically for partially sighted users. It utilizes an ultrasonic sensor and the Talkie speech synthesis library to provide real-time voice feedback, making it accessible for individuals who cannot read the device. The system measures the user's inhalation speed and provides audio instructions to encourage effective use.

## Features

- Measures inhalation speed using an ultrasonic sensor.
- Provides voice feedback:
  - **"Safe Speed"** when the inhalation rate is stable.
  - **"Slow Down"** if the inhalation is too fast.
  - **"Speed Up"** if the inhalation is too slow.
- Easy-to-read documentation and making instructions included.

## Hardware Requirements

- Arduino board
- Ultrasonic sensor (HC-SR04 or similar)
- Button (for triggering measurements)
- Speaker (for voice output)
- Talkie library (included in the code for voice synthesis)

Detailed hardware requirements can be found in the [making instructions](./documentation/Making%20Instructions.pdf).

## Installation

1. Clone or download the repository to your local machine.
2. Ensure you have the [Talkie](https://github.com/going-digital/Talkie) library installed in your Arduino IDE.
3. Connect the components as follows:
   - **Trigger Pin**: Digital pin 11
   - **Echo Pin**: Digital pin 12
   - **Switch Pin**: Digital pin 2 (configured with internal pull-up)
4. Upload the code to your Arduino board.

## Usage

1. Press the button connected to `switchPin` to start the spirometer.
2. The system will begin measuring inhalation speed and providing verbal feedback.
3. Based on the inhalation speed, the system will announce:
   - "Safe Speed" when the inhalation is at an appropriate rate.
   - "Slow Down" if the inhalation is too fast.
   - "Speed Up" if the inhalation is too slow.

4. View additional information in the included easy-read guide and follow the audio user instructions for further assistance.

## Documentation

Comprehensive documentation is available, including:
- [Making instructions](./documentation/Making%20Instructions.pdf) for assembly and setup.
- An [easy-read guide](./documentation/Easy%20Read%20guide.pdf) for understanding the device and its use.
- [Audio user instructions](./documentation/Audio%20User%20instructions.mp3) for hands-on support.
