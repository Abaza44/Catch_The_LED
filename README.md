# Catch the LED Game

![Project Status](https://img.shields.io/badge/status-complete-green)  
**A Digital Logic Design Project by Zagazig University, Faculty of Engineering, Electronics and Communication Department**

## Overview

**Catch the LED** is a two-player interactive game built using fundamental digital logic components. Players compete to press their buttons when a green LED (LED 5) lights up in a back-and-forth sequence of 8 LEDs. The system employs sequential logic circuits, including a 555 timer, flip-flops, and logic gates, to manage LED animations, player inputs, score tracking, and winner detection. This project, developed for the Digital Logic Design course at Zagazig University, demonstrates finite state machines, combinational logic, and timing circuits in a practical, engaging application.

All project details, including circuit designs, state diagrams, logic equations, testing results, and implementation notes, are documented in the provided report: [Catch_the_LED_Report.pdf](docs/Catch_the_LED_Report.pdf).

## Project Objectives

- Design a sequential circuit for a back-and-forth LED animation across 8 LEDs.
- Implement direction control to reverse the sequence at LED 0 and LED 7.
- Detect player inputs for successful "catches" when the green LED is lit.
- Track scores up to 3 points per player and detect the winner.
- Integrate subsystems into a cohesive game with manual and automatic reset.
- Use only basic digital logic components (e.g., flip-flops, gates).
- Apply digital logic theory to a functional system.

## Game Rules

1. **LED Animation**: 8 LEDs light up sequentially (LED 0 → LED 7 → LED 0), reversing at endpoints.
2. **Player Actions**: Each player presses a button when the green LED (LED 5) is lit to score a "catch."
3. **Scoring**: Scores range from 0 to 3 per player; the game ends when one or both reach 3 points.
4. **Reset**: Manual reset button or automatic reset when both players reach 3 points.

For full rules and operation, see [Section 4 of the report](docs/Catch_the_LED_Report.pdf#page=5).

## Components and Tools

### Hardware
- 8 LEDs (LED 5 is green)
- 555 Timer IC (astable mode, 1-2 Hz)
- D and T Flip-Flops
- 3-to-8 Decoder IC
- Logic Gates (AND, OR, NOT, XOR)
- Push Buttons (two for players, one for reset)
- Resistors, Capacitors, 5V Power Supply

### Tools
- Digital Logic Circuit Simulator
- Circuit Schematic Design Software
- Logic Analyzer

See [Section 3 of the report](docs/Catch_the_LED_Report.pdf#page=4) for details.

## System Design

The system integrates:
1. **Clock Generator**: 555 Timer for timing pulses.
2. **LED Sequence Controller**: Finite state machine with 16 states using D flip-flops.
3. **Direction Control**: T flip-flop toggles direction at endpoints.
4. **Player Input Detection**: AND gates and debounce circuits for button presses.
5. **Score Counter**: T flip-flops track scores (0-3).
6. **LED Display Decoder**: 3-to-8 decoder for score visualization.
7. **Winner Detection**: NOR/NOT gates light a blue (Player 1) or red (Player 2) LED at score 3.

Detailed designs, state tables, and logic equations are in [Section 5 of the report](docs/Catch_the_LED_Report.pdf#page=6).

## Testing and Results

- **Subsystem Tests**: Verified clock stability, LED sequence, direction changes, input detection, and scoring.
- **Integrated Tests**: Confirmed gameplay, edge cases (e.g., simultaneous presses), and reset functionality.
- **Results**: Reliable LED patterns, accurate scoring, and consistent resets.

See [Section 7 of the report](docs/Catch_the_LED_Report.pdf#page=17) and the timing diagram in [Section 8](docs/Catch_the_LED_Report.pdf#page=18).

## Challenges and Solutions

- **Button Debouncing**: Used RC circuits to eliminate multiple signals.
- **Synchronization**: Added clock-edge sampling for input timing.
- **State Machine**: Verified state tables rigorously.
- **Power Distribution**: Employed decoupling capacitors.

Details in [Section 8 of the report](docs/Catch_the_LED_Report.pdf#page=19).

## Future Improvements

- Adjustable clock speeds for difficulty levels.
- Audio feedback for catches and game end.
- Seven-segment displays for scores.
- Alternative LED patterns or game modes.

See [Section 9 of the report](docs/Catch_the_LED_Report.pdf#page=20).

## Repository Structure
