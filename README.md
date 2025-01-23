# Expo CLI Development Server Failure: Port Conflicts and Misconfigurations

This repository demonstrates a common issue encountered when using the Expo CLI: the development server failing to start due to port conflicts or misconfigurations within the project settings. This problem often presents as cryptic error messages related to network connections or port usage.

The `expoBug.js` file simulates the scenario where a project improperly configures its port, resulting in a conflict. The solution, found in `expoBugSolution.js`, demonstrates the correct method for resolving the issue.  The solution focuses on identifying and resolving port conflicts, and adjusting Expo's configuration to avoid them.

## Reproduction Steps

1. Clone this repository.
2. Run `npm install` to install dependencies (if any).
3. Attempt to start the development server using `expo start` in the `expoBug` directory.  Observe the error.
4. Navigate to the `expoBugSolution` directory.
5. Execute `expo start`. The development server should launch successfully.

## Solution

The core solution lies in verifying that the port specified in the Expo project's configuration (`app.json` or `expo.json`) is available. If another process is using that port, change it to an unused one. This often involves adjusting the `--port` flag in the Expo start command.  Correctly configured Expo settings and avoiding port collisions are crucial for a smooth development experience.