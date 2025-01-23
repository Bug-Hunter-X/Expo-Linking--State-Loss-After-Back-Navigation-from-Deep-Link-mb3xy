# Expo Linking State Loss Bug

This repository demonstrates a bug related to state restoration in Expo applications launched via deep links.  When the app is opened using a deep link and the user navigates away from the initial screen, pressing the back button may not correctly restore the app's state, resulting in data inconsistencies or unexpected behavior.

## Bug Description
The core issue lies in the interaction between the Expo `Linking` API, which handles deep links, and navigation libraries like `react-navigation`. After opening the app from a deep link, navigating to another screen, and then pressing the back button, the state associated with the original deep link is not properly restored.

## Reproduction
1. Clone this repository.
2. Install dependencies: `npm install`
3. Run the app: `expo start`
4. Open a deep link (e.g., provided in the `App.js` file).
5. Navigate to another screen within the app.
6. Press the back button. Observe the inconsistent or incorrect state.

## Solution
The provided solution (`bugSolution.js`) demonstrates techniques to mitigate the issue using appropriate state management and navigation handling.