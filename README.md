S.H.A.R.R.O.N. is an active, non-commercial, fully offline kitchen voice-timer project built on the **ESP32-S3-BOX-3B** using Espressif **ESP-SR**, **WakeNet**, and **MultiNet**.

The project is running on real hardware. The current temporary wake word will eventually be replaced by the requested custom wake phrase:

> **OK Sharron**

Pronunciation: **“oh-KAY SHARR-on”**  
IPA: **/oʊ ˈkeɪ ˈʃærən/**

## Current hardware

- ESP32-S3-BOX-3B
- Built-in microphone array
- Built-in speaker
- Built-in colour display
- USB-C power
- 3D-printed kitchen stand

## Current working firmware

The current production build uses:

- **ESP-IDF 5.3.6**
- **ESP-SR 1.6.1**
- **WakeNet9**
- **MultiNet6**
- Offline speech recognition on the ESP32-S3
- No cloud speech service required

A later ESP-IDF 6.1 / WakeNet10 / MultiNet7 build was also tested successfully on the same hardware, but the project returned to the ESP-IDF 5.3.6 / MultiNet6 production build because command recognition was more reliable for this application.

## Working features

S.H.A.R.R.O.N. currently provides:

- Local WakeNet wake-word detection
- Offline MultiNet command recognition
- Four simultaneous kitchen timers
- Spoken timer-start commands
- Timer cancellation by number
- Repeating timer alarm
- Bare **“Stop”** command while an alarm is sounding
- Audible acknowledgement through the BOX-3 speaker
- LVGL timer display
- Analogue idle clock
- Automatic display dimming and idle behaviour
- Entirely local operation after firmware is installed

## Example voice commands

Examples currently used by the working firmware include:

- “Timer ten minutes”
- “Set timer five minutes”
- “Cancel timer one”
- “Stop” while an alarm is sounding

## Custom wake-word request

The intended final wake phrase is **“OK Sharron”**.

Requested target:

- Language: English
- Target chip: ESP32-S3
- Target hardware: ESP32-S3-BOX-3B
- Preferred model: WakeNet9
- Preferred training pipeline: TTS Pipeline V3

The request is being tracked in Espressif's community wake-word thread:

https://github.com/espressif/esp-sr/issues/88

Original S.H.A.R.R.O.N. request:

https://github.com/espressif/esp-sr/issues/88#issuecomment-5925650192

Latest WakeNet9 update:

https://github.com/espressif/esp-sr/issues/88#issuecomment-6046050157

## Testing available

The physical prototype can be used to test a custom wake model for:

- First-attempt wake reliability
- Near-field and far-field activation
- Different speaking positions
- Quiet-room operation
- Normal kitchen background noise
- False activations
- Repeated wake cycles after long idle periods
- Interaction with offline MultiNet commands after wake

## Project status

**Active and running on physical hardware.**

This repository currently serves as the public project overview for the working S.H.A.R.R.O.N. prototype and its Espressif wake-word request. More technical notes, photographs and selected project files may be added as development continues.

---

Built around Espressif's ESP32-S3-BOX-3B and ESP-SR speech-recognition stack.
