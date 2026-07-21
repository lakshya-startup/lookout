### 1. Visa Countdown Feature
*   Build a quick visual placeholder box for the countdown timer.

### 2. The New Architecture 
The visa countdown UI transitions through three dynamic operational stages:

*   **Stage 1 (7% Peek):** A tiny pill-shaped component at the top of the screen displaying only the visa date.
*   **Stage 2 (35% Loading):** Tapping the Stage 1 pill expands it downward into a wider interface showing a loading progress bar. If ignored for 10 seconds, it automatically shrinks back to Stage 1.
*   **Stage 3 (100% Floating Interface):** Tapping the pill during either Stage 1 or Stage 2 triggers a custom Bottom Sheet. It slides up from the bottom, anchoring perfectly to leave exactly 15% open space at the top and 5% open space at the bottom.

### 3. The TV 