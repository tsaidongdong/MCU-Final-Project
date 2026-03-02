# MCU-Final-Project
# Morse Code Game Machine (摩斯密碼遊戲機)

This is a hardware-software integrated project developed using the **PIC18F4520** microcontroller. It serves as an interactive educational tool that translates Morse code button inputs into alphanumeric characters, triggering synchronized visual effects through an LCD and LEDs.

## Key Features
* **Dual-Button Input System**: Utilizes one button for Morse code signal input (dots/dashes) and another for character confirmation.
* **Real-time Translation**: Interprets Morse code sequences into text displayed on an **LCD1602A** screen.
* **Dynamic Visual Effects**: Includes multiple LED response modes, such as specific blinking patterns and **PWM-controlled breathing lights.
* **Command-Based Interaction**: Supports specific string commands (e.g., `br` for breathing light, `la` to `ld` for specific LEDs, and `end` to reset) to trigger different hardware states.

## System Architecture & Logic
The application relies on precise timing and interrupt handling to process signals:
**Signal Detection**: Uses software delays to differentiate between "dots" (short press) and "dashes" (long press) based on input duration.
**Interrupt Handling**: Implements **Interrupt Service Routines (ISR)** with priority levels to manage concurrent input (High Priority) and output tasks (Low Priority).
* **Peripheral Control**:
    **LCD**: Driven via an **8-bit parallel bus** for stable data transmission.
    **LEDs**: Managed through **Timer2** and **PWM** modules to achieve smooth "breathing" brightness transitions.

## Technical Stack
* Microcontroller: PIC18F4520.
* Development Environment: MPLAB X IDE & MPLAB-PICkit-4.
* Language: C (XC8 Compiler).
* Key Techniques: Interrupts with priority, Timer2, PWM, and hardware circuit soldering.

## Project Structure
* `main.c`: Core logic for Morse translation, PWM initialization, and LCD control.
* `test.c`: Configuration bit settings and basic interrupt testing.
* `Makefile`: Build configuration for the MPLAB project.
* `微算機期末專題35組.pdf`: Detailed project report and system documentation.
