# Chocobo Date Range Picker - The Date Range Picker easier to use in angular.  [![chocobo2.png](https://s23.postimg.org/9ihipgoej/chocobo2.png "Chocobo Icon")](https://postimg.org/image/k5bbuvwjr)

[![dtChocobo.gif](https://s30.postimg.org/qkccdu5xt/dt_Chocobo.gif "Using Date Range Picker GIF")](https://postimg.org/image/607ifcq6l/)

## Try it yourself.
[click here](https://chocobo-date-range-picker.herokuapp.com/)

# How to install

```shell
bower install chocoborangepicker
```

# How to use

##### Import to your project the chocobo-range-picker.min.js and chocobo-range-picker.min.css files in bower_components folder
```html
 <link href="/bower_components/chocoborangepicker/dist/css/chocobo-range-picker.min.css" rel="stylesheet">
 <script type="text/javascript" src="/bower_components/chocoborangepicker/dist/js/chocobo-range-picker.min.js"></script>
```

 Then refer to your module
```javascript
 angular.module('yourModule', ['chocoboRangePicker']);
```

##### In your controller use the code below

```javascript
  // Here is your property that you want to be populated with date range.
  $scope.demo = { searchDate: null };  

  $scope.options = {
    txtDateInit: 'Demo: Date',
    buttons: {
      btnYear: { txt: 'Demo: Year', tooltip: "Choose Year" },
      btnSemester: { txt: 'Demo: Semester', tooltip: "Choose Semester" },
      btnTrimester: { txt: 'Demo: Trimester', tooltip: "Choose Trimester" },
      btnMonth: { txt: 'Demo: Month', tooltip: "Choose Month" },
      btnWeek: { txt: 'Demo: Week', tooltip: "Choose Week" },
      btnToday: { txt: 'Demo: Today', tooltip: "Choose Today" },
      btnLastDay: { txt: 'Demo: Last Day', tooltip: "Choose Last Day" }
    },
    inputConfig: {
      showIcon: true,
      iconPath: "http://www.racedepartment.com/images/rd_calext/calendar.png"
    }
  };
```


### $scope.options

* **txtDateInit** - Label of input text that will show the date interval. If you remove this property it will not shown. This property is optional;
* **buttons** - Where you will configure a buttons properties. This property is required;
* **buttons: {btnYear}** - Where you will configure a each button properties. This property is optional,but if you do not use this property the related button will not be displayed;
* **buttons: {btnYear.txt}** - Text that will apear in button. This property is optional;
* **buttons: {btnYear.tooltip}** - Tooltip that will appear when user mouseover on button. This property is optional;
* **inputConfig** - Input text settings. Optional. Without this property the default icon will be displayed;
* **inputConfig: {showIcon}** - This property indicate if you want show icon. his property is required. If the property is false, the icon will not be displayed;
* **inputConfig: {iconPath}** - This property indicate if you want show icon. This property is optional, This property indicate the path to his own icon;
* **minDate**(optional): Indicates the minimun possible date for a user to select;
* **maxDate**(optional): Indicates the maximum possible date for a user to select.

##### In your page use

```html
  <chocobo-Range-Picker bindRange='false'
                        blockWeekDay='0,6'
                        locale='pt-BR'
                        options='options'
                        ng-model="demo.searchDate">
  </chocobo-Range-Picker>
```


### chocobo-Range-Picker

* **bindRange**
  * *true*: All date in the range will be assigned to the model;
  * *false*: The first and last date will be assigned to the template.

* **blockWeekDay**(optional)\*: Property that represent a weekday to be blocked (`0-6`), where:
  * "Sunday": 0;
  * "Monday": 1;
  * "Tuesday": 2;
  * "Wednesday": 3;
  * "Thursday": 4;
  * "Friday": 5;
  * "Saturday": 6.

#### Attention these locales have been tested.

* **Spain**: `es-ES`
* **Brazil**: `pt-BR`
* **United States**: `en-US`
* **Great Britain**: `en-GB`
* **Germany**: `de-DE`

#### Used versions

* **Angular**
  * version: `1.2.32`

***

### License

It is available under the MIT license.
[License](https://opensource.org/licenses/mit-license.php)
