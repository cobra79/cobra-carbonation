[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/cobra79/cobra-carbonation)

# cobra-carbonation
Polymer element to calculate necessary sugar/wort to get the right carbonation in handcrafted beer
## Installation
bower install cobra-carbonation --save
## Usage
Set the attributes 

volume: Batch size or bottle size - simply the volume of beer for that you want to do the calculation
temperature: Max. temperature (in degrees Celsius) during the fermentation - This determines how much CO2 is already dissolved in the beer
co2: The desired amount of CO2 in gram/liter

If you want to use wort for the carbonation you need to specify: 
originalWort: degree Plato before fermentation (how much sugar is the the wort you are using)
residualWort: degree Plato after fermentation 

## Demo
<!--
```
<custom-element-demo>
  <template>
    <link rel="import" href="cobra-carbonation.html">
    <next-code-block></next-code-block>
  </template>
</custom-element-demo>
```
-->
```html
 <template>
          <dom-bind>
            <template>
              <paper-input label="CO2" value="{{co2}}"></paper-input>
              <paper-input label="Temperature" value="{{temperature}}"></paper-input>
              <paper-input label="Volume" value="{{volume}}"></paper-input>
              <paper-input label="Original wort" value="{{originalWort}}"></paper-input>
              <paper-input label="Residual Wort" value="{{residualWort}}"></paper-input>
              <cobra-carbonation
                      volume="{{volume}}"
                      co2="{{co2}}"
                      temperature="{{temperature}}"
                      sugar="{{sugar}}"
                      dextrose="{{dextrose}}"
                      wort="{{wort}}"
                      original-wort="{{originalWort}}"
                      residual-wort="{{residualWort}}"
              ></cobra-carbonation>
              <h2>Sugar:[[sugar]]</h2>
              <h2>Dextrose:[[dextrose]]</h2>
              <h2>Wort:[[wort]]</h2>
            </template>
          </dom-bind>
        </template>
```



## License
MIT

