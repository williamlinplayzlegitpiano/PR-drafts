# **US17: 5-Second Completed Task Times & US3C: Manually Advance Time by 15 Seconds**

## **Description**
This PR primarily implements **User Story 17: 5-Second Completed Task Times**, improving the accuracy of task duration tracking by displaying **tasks completed in under a minute** in **5-second increments** instead of rounding to whole minutes. This enhances usability and provides more granular insights into short task durations.

Additionally, **User Story 3C: Manually Advance Time by 15 Seconds** introduces a **manual time advance feature** that allows testers to **increment elapsed routine time by 15 seconds per tap**, ensuring better control over time tracking in testing scenarios.

## **Changes**
### **US17: 5-Second Completed Task Times**
- Enhanced **task completion time formatting**:
  - If a task takes **less than 60 seconds**, it is now displayed in **5-second intervals** (e.g., `5s`, `10s`, `15s`).
  - Tasks **over 60 seconds** continue to be displayed in **minutes**.
- Updated **UI timer logic** to support **dynamic time formatting** based on duration.
- Ensured the **timer updates correctly** as tasks are completed.
- **Implemented Espresso UI tests** to verify correct behavior.

### **US3C: Manually Advance Time by 15 Seconds**
- Added a **manual time advance button** on the routine screen.
- Each tap **increases elapsed time by 15 seconds**.
- Integrated this feature into **Mock Mode** for controlled testing.
- Ensured the UI updates correctly when time is manually advanced.

## **Issues Addressed**
Closes **#139 #140 #141 #142 #119 #120 #121 #122**.

## **Type of Change**
- [x] New feature (non-breaking change that adds functionality)
- [ ] Bug fix (non-breaking change that fixes an issue)
- [ ] Breaking change (fix or feature that would cause existing functionality to not work as expected)
- [ ] Other (explain below)

## **Testing**
### **Espresso UI Tests**
#### ✅ **US17: 5-Second Completed Task Times**
- **Tasks under 60 seconds display time in 5-second increments**.
- **Tasks over 60 seconds display in minutes**.
- **Timer updates dynamically** as tasks are completed.
- **All tests are passing**.

#### ✅ **US3C: Manually Advance Time by 15 Seconds**
- **Verifies elapsed time starts at `0m`**.
- **Taps "Mock Mode" to enable manual time control**.
- **Advances time multiple times and verifies correct updates**.
- **Ensures total time updates properly after 4 taps = 1 min**.
- **Handles edge cases for multiple presses**.

## **Checklist**
### ✅ **Code meets the specification**
- [x] Implements the features described by the user stories.
- [x] Considers edge cases and user experience.
- [x] Follows project guidelines and Piazza clarifications.

### ✅ **Code is understandable**
- [x] Follows formatting conventions (spacing, indents, etc.).
- [x] Uses clear, descriptive variable/method names.
- [x] Well-documented with inline comments and README updates.

### ✅ **Code is well-structured**
- [x] Organized into logical components.
- [x] Follows SRP.
- [x] Uses meaningful component names and well-defined class responsibilities.
