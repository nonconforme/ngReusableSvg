I'd like to extend credit to Matan Zohar for the replacement trick. For further info, see [my blog](http://omriaharon.blogspot.co.il/).

## ngReusableSvg - Reuse SVG Files with CSS Modifications
Creates a reusable SVG component out of an external SVG file. This lets you control your SVGs using CSS.

More specifically, you will be able to change the fill color of the SVG, meaning you can change its color via CSS.

## Dependencies

* AngularJS v1.3
* Previous versions might work too, but haven't been tested.

## How to get it?

### Manual Download

Download from [here](http://omriaharon.github.io/ngReusableSvg/)

### NPM

    npm install --save ng-reusable-svg

### Bower

    bower install ngReusableSvg

### Usage

1. Add `ngReusableSvg.js` to your main file (index.html). 

2. Set `ngReusableSvg` as a dependency in your module

        var myApp = angular.module('myApp', ['ngReusableSvg'])

3. Add `oa-reusable-svg` onto an `<object>` tag:

        <object oa-reusable-svg
                id="my-svg"
                data="my_icon.svg"
                type="image/svg+xml"
                class="svg-class"
                height="30"
                width="30">
        </object>

4. **Important!** Make sure your SVG file itself does not specify its own height & width, otherwise this will not work properly. 

### ngReusableSvg Attributes

* **ngClick** - an action to be performed when the SVG image is clicked.

* **ngClass** - an action to be performed to determine the class.

* **notifyReady** - a boolean (needs to be initialized as false) that will be set to true when the switch has been performed. Useful if you need to know when the image is ready, for instance, when cloning the element.

* **float** - Accepts only "false" value that turns off the default "float: left;" to the element. 
