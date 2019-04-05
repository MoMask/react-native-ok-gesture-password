# react-native-ok-gesture-password
gesture password component,smooth easy and quick

base on  [react-native-smart-gesture-password][0]　More friendly to existing reactive native versions, adding moving callbacks


## Preview
![react-native-smart-gesture-password-demo][1]
## Installation

```
npm install react-native-ok-gesture-password --save
```
```js
import React, {Component} from 'react';
import {Platform, StyleSheet, Text, View, Alert} from 'react-native';
import OkGesturePassword from "./source/OkGesturePassword";

type
Props = {};
export default class App extends Component<Props> {

    state = {
        point1: "#FFFFFF",
        point2: "#FFFFFF",
        point3: "#FFFFFF",
        point4: "#FFFFFF",
        point5: "#FFFFFF",
        point6: "#FFFFFF",
        point7: "#FFFFFF",
        point8: "#FFFFFF",
        point9: "#FFFFFF",
    };

    render() {
        return (
            <View style={styles.container}>
                <View style={{height: 70, marginTop: 10}}>
                    <View style={styles.headContent}>
                        <View style={[styles.headCircle, {backgroundColor: this.state.point1}]}/>
                        <View style={[styles.headCircle, {backgroundColor: this.state.point2}]}/>
                        <View style={[styles.headCircle, {backgroundColor: this.state.point3}]}/>
                    </View>
                    <View style={styles.headContent}>
                        <View style={[styles.headCircle, {backgroundColor: this.state.point4}]}/>
                        <View style={[styles.headCircle, {backgroundColor: this.state.point5}]}/>
                        <View style={[styles.headCircle, {backgroundColor: this.state.point6}]}/>
                    </View>
                    <View style={styles.headContent}>
                        <View style={[styles.headCircle, {backgroundColor: this.state.point7}]}/>
                        <View style={[styles.headCircle, {backgroundColor: this.state.point8}]}/>
                        <View style={[styles.headCircle, {backgroundColor: this.state.point9}]}/>
                    </View>
                </View>
                <OkGesturePassword
                    style={styles.gesturePassword}
                    pointBackgroundColor={'white'}
                    showArrow={false}
                    color={'#1F67B9'}
                    activeColor={'#1F67B9'}
                    warningColor={'red'}
                    warningDuration={0}
                    allowCross={false}
                    onMove={(p) => {
                        console.log("onMove:" + p);
                        this._changeHeadPoint(p);
                    }}
                    onFinish={(password) => {
                        Alert.alert("密码",password);
                        this._resetHeadPoint();
                    }}
                />
            </View>
        );
    }

    _resetHeadPoint = () => {
        this.setState({
            point1: "#FFFFFF",
            point2: "#FFFFFF",
            point3: "#FFFFFF",
            point4: "#FFFFFF",
            point5: "#FFFFFF",
            point6: "#FFFFFF",
            point7: "#FFFFFF",
            point8: "#FFFFFF",
            point9: "#FFFFFF",
        });
    };

    _changeHeadPoint = (point) => {
        switch (point + 1) {
            case 1:
                this.setState({
                    point1: '#1F67B9'
                });
                break;
            case 2:
                this.setState({
                    point2: '#1F67B9'
                });
                break;
            case 3:
                this.setState({
                    point3: '#1F67B9'
                });
                break;
            case 4:
                this.setState({
                    point4: '#1F67B9'
                });
                break;
            case 5:
                this.setState({
                    point5: '#1F67B9'
                });
                break;
            case 6:
                this.setState({
                    point6: '#1F67B9'
                });
                break;
            case 7:
                this.setState({
                    point7: '#1F67B9'
                });
                break;
            case 8:
                this.setState({
                    point8: '#1F67B9'
                });
                break;
            case 9:
                this.setState({
                    point9: '#1F67B9'
                });
                break;

        }
    };

}

const styles = StyleSheet.create({
    gesturePassword: {
        backgroundColor: 'white',
    },
    headContent: {
        flex: 1, justifyContent: 'center', flexDirection: 'row'
    },
    headCircle: {
        borderRadius: 30,
        borderWidth: 1,
        borderColor: "#1F67B9",
        width: 15,
        height: 15,
        margin: 4,
    },
    container: {
        flex: 1,
        justifyContent: 'center',
        alignItems: 'center',
        backgroundColor: 'white',
    },
    welcome: {
        fontSize: 20,
        textAlign: 'center',
        margin: 10,
    },
    instructions: {
        textAlign: 'center',
        color: '#333333',
        marginBottom: 5,
    },
});
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


