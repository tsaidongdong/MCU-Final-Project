# MCU-Final-Project
# Morse Code Game Machine (摩斯密碼遊戲機)

This is a hardware-software integrated project developed using the **PIC18F4520** microcontroller. It serves as an interactive educational tool that translates Morse code button inputs into alphanumeric characters, triggering synchronized visual effects through an LCD and LEDs.

## Key Features
* [cite_start]**Dual-Button Input System**: Utilizes one button for Morse code signal input (dots/dashes) and another for character confirmation[cite: 30, 43, 45].
* [cite_start]**Real-time Translation**: Interprets Morse code sequences into text displayed on an **LCD1602A** screen[cite: 33, 47, 78].
* [cite_start]**Dynamic Visual Effects**: Includes multiple LED response modes, such as specific blinking patterns and **PWM-controlled breathing lights**[cite: 34, 48, 63].
* [cite_start]**Command-Based Interaction**: Supports specific string commands (e.g., `br` for breathing light, `la` to `ld` for specific LEDs, and `end` to reset) to trigger different hardware states[cite: 57, 58, 59, 60, 61, 62].

## System Architecture & Logic
The application relies on precise timing and interrupt handling to process signals:
* [cite_start]**Signal Detection**: Uses software delays to differentiate between "dots" (short press) and "dashes" (long press) based on input duration[cite: 30, 86, 87].
* [cite_start]**Interrupt Handling**: Implements **Interrupt Service Routines (ISR)** with priority levels to manage concurrent input (High Priority) and output tasks (Low Priority)[cite: 75].
* **Peripheral Control**:
    * [cite_start]**LCD**: Driven via an **8-bit parallel bus** for stable data transmission[cite: 78, 79].
    * [cite_start]**LEDs**: Managed through **Timer2** and **PWM** modules to achieve smooth "breathing" brightness transitions[cite: 48, 75].

## Technical Stack
* [cite_start]**Microcontroller**: PIC18F4520[cite: 49, 73].
* [cite_start]**Development Environment**: MPLAB X IDE & MPLAB-PICkit-4[cite: 73].
* [cite_start]**Language**: C (XC8 Compiler).
* [cite_start]**Key Techniques**: Interrupts with priority, Timer2, PWM, and hardware circuit soldering[cite: 75, 76].

## Project Structure
* [cite_start]`main.c`: Core logic for Morse translation, PWM initialization, and LCD control[cite: 13].
* [cite_start]`test.c`: Configuration bit settings and basic interrupt testing[cite: 1].
* [cite_start]`Makefile`: Build configuration for the MPLAB project.
* [cite_start]`微算機期末專題35組.pdf`: Detailed project report and system documentation[cite: 15].
