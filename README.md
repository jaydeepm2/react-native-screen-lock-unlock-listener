# react-native-screen-lock-unlock-listener

## Getting started

`yarn add react-native-screen-lock-unlock-listener`

or

`$ npm install react-native-screen-lock-unlock-listener --save`

## Usage

## at the top

```javascript
import { NativeEventEmitter, NativeModules } from "react-native";
import PhoneLocked from "react-native-screen-lock-unlock-listener";

const App: () => React$Node = () => {
  // inside function //
  const eventEmitter = new NativeEventEmitter(NativeModules.PhoneLocked);

  eventEmitter.addListener("EventReminder", (res) => {
    // listen here for screen on or off action
    console.log(res.action); // ACTION_USER_PRESENT || ACTION_SCREEN_OFF || ACTION_SCREEN_ON
  });

  return <></>;
};
```
