# Vue.js BMI Calculator

A simple BMI calculator built with Vue.js

Live version: [https://ravk.nl/bmi](https://ravk.nl/bmi)

## Units

Currently this calculator supports the following units for weight:

* Kilogram (kg)
* Pound (lb)

Length units:

* Centimeter (cm)
* Feet + inches (us)

## 3rd Party Components

This project includes the following outside components:

* Vue.js
* Bootstrap CSS
* Bootstrap-vue.js
* Bootstrap-vue.css
* Babel Polyfill
* Animate.css (```.fadeInUp```)
* Google Fonts 'Poppins'

All content in the img/favicons folder, with the exception of favicon.svg, was generated using [realfavicongenerator.net](https://realfavicongenerator.net). The icon used is part of the ionicons icon pack available at [ionicons.com](http://ionicons.com/) under the MIT license.

## DOM Structure

The mark up in index.html has the following basic structure:

```
#background
#app
├── #row-title
├── #row-input
└── #row-result
```

# Javascript Functions

## ```round(value, precision)```

Round decimal value to given number of decimal places (precision).

```javascript
round(3.54687, 1); // returns: 3.5
round(3.54687, 2); // returns: 3.55
round(3.54687, 3); // returns: 3.547
```

## ```lbToKg(lb)```

Converts pounds (lb) to kilograms (kg).

```javascript
lbToKg(1); // returns: 0.45359237
```

## ```kgToLb(kg)```

Converts kilograms (kg) to pounds (lb).

```javascript
kgToLb(1); // returns: 2.20462262185
```

## ```imperialToCm(feet, inches)```

Converts imperial feet + inches (us) to centimeters (cm).

```javascript
imperialToCm(5,11); // returns: 180.34
```

## ```cmToImperial(cm)```

Converts centimeters (cm) to imperial feet + inches (us) and returns an object containing feet and inches.

```javascript
cmToImperial(180);
```

returns:

```javascript
{ feet: 5, inches: 11 }
```

## ```calculateBMI(kg, cm)```

Calculates Body Mass Index based on weight (kg) and height (cm).

```javascript
round(calculateBMI(75, 180), 1); // returns: 23.1
```

## ```getWeightGroup(bmi)```

Returns weight class name of the given BMI as a string.

```javascript
getWeightGroup(23); // returns: "Healthy Weight"
```