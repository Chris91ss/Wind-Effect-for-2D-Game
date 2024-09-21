# Wind Effect for 2D Game

## Overview

This script applies a dynamic wind effect to a 2D game. It simulates changing wind directions and strengths that influence the player’s movement when airborne. The wind periodically shifts direction, and particle effects are used to visually represent the wind's force.

---

## How to Use

### Step-by-Step Implementation:

1. **Setup GameObject:**
   - Add the `WindEffect` script to a 2D trigger collider that defines the area where the wind effect is active.
   - Assign the player’s `Rigidbody2D` and `PlayerMovement` scripts in the inspector to allow the wind to affect the player.

2. **Wind Effect:**
   - The wind will apply force to the player when they are inside the trigger area and not grounded.
   - Wind force changes over time with configurable variables such as `windMultiplier`, `windPower`, and `windDirection`.

3. **Particle System:**
   - Add a particle system as a child to the trigger area to simulate wind visually.
   - Attach the particle system to the `WindEffect` script in the inspector for synchronized movement.

---

## Customizable Variables

- **Wind Variables:**
  - `windValue`: The current value of the wind's strength.
  - `windDirection`: The direction of the wind. It periodically changes between positive and negative values.
  - `windMultiplier`: Multiplies the wind strength for more dramatic effects.
  - `windPower`: Exponent for fine-tuning wind force.
  - `windDivider`: Controls how quickly the wind strength changes.

- **Wind Direction Timer:**
  - `timerAmount`: Time before wind direction changes.
  - `startTimer`: Tracks the time elapsed since the last direction change.
  
- **No Wind Timer:**
  - `noWindTimerAmount`: The time before wind resumes after stopping.
  - `noWindStartTimer`: Timer for wind pause duration.

- **Particle System Control:**
  - `lerpTimer`: Controls how quickly particles adjust to the wind direction change.
  - `xVelocityValue`: The maximum speed of particle movement.

---

## Code Overview

### Key Methods:

- **ApplyWind():** Applies wind force to the player when in the air and inside the wind trigger.
- **ChangeWindDirection():** Handles periodic changes in wind direction, pausing for a brief moment before switching direction.
- **Lerp():** Smoothly interpolates the particle system’s velocity to reflect wind direction changes.

---

## Example Usage

1. Set up a 2D platformer scene.
2. Create a trigger area (e.g., for a specific level section) and add the `WindEffect` script.
3. Attach the player’s `Rigidbody2D` and `PlayerMovement` scripts.
4. Configure wind settings in the inspector to customize the effect’s strength, duration, and visual representation.
  
---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

---
