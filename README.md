# @tapston/react-native-styles
## Make your styles very similar for any device screen 📱

### Installation

`yarn add @tapston/react-native-styles`

### Usage
- Import
```js
import RNStyles from '@tapston/react-native-styles';
```
- Initialize you config for RNStyles in index.js
```js
// If you need your own config:
RNStyles.init({
  designWidth: 428, // default value is 428
  designHeight: 926, // default value is 926
  minimalFactor: 1, // default value is 1
});

// designWidth - Width of your design. Default value is 414 (iPhone 12 Pro Max).
// designHeight - Height of your design. Default value is 896 (iPhone 12 Pro Max).
// minimalFactor - Factor is the value all numeric styles are multiplied by. The default minimal factor is 1.
```
- Create your styles
```js
const myStyles = RNStyles.create({
  // Get a rectangle if the screen of your device is not square
  container: {
    width: 100,
    height: 100,
  },
  // Square with average relativity to width and height
  squareContainer: {
    square: 100,
  },
});
```
- If you want your style's values to be static, use a string value instead of a number
```js
{
  width: '100', // Width will be equal to 100 on all devices
  height: 100, //  Height will depend on the size of a device
}
```
- If you want to change all the sizes of the entire project, change minimalFactor in the constructor
```js
{
  ...,
  minimalFactor: 1.2, // To increase the size of all elements by 20%
}
```
