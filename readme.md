# fork版本

```
修改了android/build.gradle兼容和react-native-amap3d同时使用时候的构建错误
https://github.com/qiuxiang/react-native-amap3d/issues/787
dependencies {
    compileOnly 'com.facebook.react:react-native:+'
    implementation 'com.amap.api:3dmap:9.6.0'
}
```

# react-native-amap-geolocation-chef [![][version-badge]][npm] [![][build-badge]][build]

**注意：该项目目前只维护，不加新功能。**

React Native 高德地图定位模块，支持 Android + iOS，提供尽可能完善的原生接口，
同时提供符合 Web 标准的 Geolocation API。

<img src="https://user-images.githubusercontent.com/1709072/57276743-12f67f00-70d5-11e9-9fe9-94e37abc1e0b.png" width=360>

## 用法

```javascript
import { PermissionsAndroid } from "react-native";
import { init, Geolocation } from "react-native-amap-geolocation-chef";

await PermissionsAndroid.requestMultiple([
  PermissionsAndroid.PERMISSIONS.ACCESS_FINE_LOCATION,
  PermissionsAndroid.PERMISSIONS.ACCESS_COARSE_LOCATION,
]);

await init({
  ios: "9bd6c82e77583020a73ef1af59d0c759",
  android: "043b24fe18785f33c491705ffe5b6935",
});

Geolocation.getCurrentPosition(({ coords }) => {
  console.log(coords);
});
```

## 文档

- [使用指南](https://qiuxiang.github.io/react-native-amap-geolocation)
- [接口文档](https://qiuxiang.github.io/react-native-amap-geolocation/api/)

[npm]: https://www.npmjs.com/package/react-native-amap-geolocation
[version-badge]: https://badge.fury.io/js/react-native-amap-geolocation.svg
[build-badge]: https://github.com/qiuxiang/react-native-amap-geolocation/actions/workflows/build.yml/badge.svg
[build]: https://github.com/qiuxiang/react-native-amap-geolocation/actions/workflows/build.yml
