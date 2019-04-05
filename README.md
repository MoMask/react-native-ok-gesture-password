# react-native-ok-gesture-password
gesture password component,smooth easy and quick

base on  [react-native-smart-gesture-password][0]　More friendly to existing reactive native versions, adding moving callbacks


## Preview
![react-native-smart-gesture-password-demo][1]
## Installation

```
npm install react-native-ok-gesture-password --save
```

## Props

Prop                 | Type    | Optional | Default      | Description
-------------------- | ------- | -------- | ------------ | -----------
pointBackgroundColor | string  | Yes      | 'transparent'| determine bgcolor of gesture point
gestureAreaLength    | number  | Yes      | 222          | determine width and height of gesture area
color                | string  | Yes      | '#A9A9A9'    | determine color of normal gesture point
activeColor          | string  | Yes      | '#00AAEF'    | determine color of active gesture point
warningColor         | string  | Yes      | 'red'        | determine color of warning gesture point
lineColor            | string  | Yes      |              | determine color of line, if does not set this, the color of line will be the same as gesture point
lineWidth            | string  | Yes      | 1            | determine width of line
warningDuration      | number  | Yes      | 1500         | determine duration when gesture status is warning
topComponent         | element | Yes      |              | determine the presentation above gesture area
bottomCompont        | element | Yes      |              | determine the presentation below gesture area
isWarning            | bool    | Yes      | false        | determine gesture warning status
showArrow            | bool    | Yes      | true         | determine whether show arrow in point
allowCross           | bool    | Yes      | true         | determine whether allow a line cross a point
onStart              | func    | Yes      |              | determine the listener which is called before gesture is granted
onMove               | func    | Yes      |              | determine the listener which is called after gesture is moved
onReset              | func    | Yes      |              | determine the listener which is called after gesture is reseted
onFinish             | func    | Yes      |              | determine the listener which is called after gesture actions is finished

[0]: https://github.com/react-native-component/react-native-smart-gesture-password
[1]: https://github.com/MoMask/react-native-ok-gesture-password/blob/master/screehost/demo.gif


