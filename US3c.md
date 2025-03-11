# US3C: Manually Advance Time by 15 Seconds

## Description
This PR implements **User Story 3C: Manually Advance Time by 15 Seconds**, allowing testers to manually advance the elapsed routine time by **15 seconds per tap**. This ensures that routines and individual tasks are allocated the correct amount of time and that time-tracking functions correctly.

## Changes
- Implemented a **manual time advance button** on the routine screen.
- Each tap **advances the elapsed time by 15 seconds**.
- Ensured UI updates correctly when advancing time multiple times.
- Integrated this feature into **Mock Mode** for controlled testing.

## Issues Addressed
Closes **#119 #120 #121 #122**.

## Type of Change
- [x] New feature (non-breaking change that adds functionality)
- [ ] Bug fix (non-breaking change that fixes an issue)
- [ ] Breaking change (fix or feature that would cause existing functionality to not work as expected)
- [ ] Other (explain below)

## Testing
### [x] **Espresso UI Tests**
- Implemented **Espresso test case (`US3C.java`)**:
  - **Verifies elapsed time starts at `0m`.**
  - **Taps "Mock Mode" to enable manual time control.**
  - **Advances time multiple times and verifies correct updates.**
  - **Ensures total time updates properly after 4 taps = 1 min.**
  - **Edge case handling for multiple presses.**

## Checklist
### [x] Code meets the specification
- [x] Implements the features described by the user story.
- [x] Considers edge cases and user experience.
- [x] Follows project guidelines and Piazza clarifications.

### [x] Code is understandable
- [x] Follows formatting conventions (spacing, indents, etc.).
- [x] Uses clear, descriptive variable/method names.
- [x] Well-documented with inline comments and README updates.

### [x] Code is well-structured
- [x] Organized into logical components.
- [x] Follows SRP
- [x] Uses meaningful component names and well-defined class responsibilities.

