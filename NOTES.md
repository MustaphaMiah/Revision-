# revision-
Revising HTML, CSS &amp; JavaScript

                                                                                          

Notes:

The div element, also known as a division element, is a general purpose container for other elements.

In addition to pixels, you can also specify the border-radius using a percentage.

In addition to classes, each HTML element can also have an id attribute.
There are several benefits to using id attributes: You can use an id to style a single element and later you'll learn that you can use them to select and modify specific elements with JavaScript.

Instead of specifying an element's padding-top, padding-right, padding-bottom, and padding-left properties individually, you can specify them all in one line, like this:
padding: 10px 20px 10px 20px;

The two main types of length units are absolute and relative. Absolute units tie to physical units of length. For example, in and mm refer to inches and millimeters, respectively. Absolute length units approximate the actual measurement on a screen, but there are some differences depending on a screen's resolution.

Relative units, such as em or rem, are relative to another length value. For example, em is based on the size of an element's font. If you use it to set the font-size property itself, it's relative to the parent's font-size.

06/12/19

The box-shadow property applies one or more shadows to an element.
The box-shadow property takes values for

* offset-x (how far to push the shadow horizontally from the element),
* offset-y (how far to push the shadow vertically from the element),
* blur-radius,
* spread-radius and
* color, in that order.

The blur-radius and spread-radius values are optional.
Multiple box-shadows can be created by using commas to separate properties of each box-shadow element.
Here's an example of the CSS to create multiple shadows with some blur, at mostly-transparent black colors:

The text-transform property in CSS is used to change the appearance of text. It's a convenient way to make sure text on a webpage appears consistently, without having to change the text content of the actual HTML elements.
The following table shows how the different text-transformvalues change the example text "Transform me".

Value	Result
lowercase	"transform me"
uppercase	"TRANSFORM ME"
capitalize	"Transform Me"
initial	Use the default value
inherit	Use the text-transform value from the parent element
none	Default: Use the original text

CSS treats each HTML element as its own box, which is usually referred to as the CSS Box Model. Block-level items automatically start on a new line (think headings, paragraphs, and divs) while inline items sit within surrounding content (like images or spans). The default layout of elements in this way is called the normal flow of a document, but CSS offers the position property to override it.

26/12/19

Applying a color on HTML elements is not limited to one flat hue. CSS provides the ability to use color transitions, otherwise known as gradients, on elements. This is accessed through the background property's linear-gradient() function. Here is the general syntax:
background: linear-gradient(gradient_direction, color 1, color 2, color 3, ...);
The first argument specifies the direction from which color transition starts - it can be stated as a degree, where 90deg makes a vertical gradient and 45deg is angled like a backslash. The following arguments specify the order of colors used in the gradient.
Example:
background: linear-gradient(90deg, red, yellow, rgb(204, 204, 255));

03/01/20

By manipulating different selectors and properties, you can make interesting shapes. One of the easier ones to try is a crescent moon shape. For this challenge you need to work with the box-shadow property that sets the shadow of an element, along with the border-radius property that controls the roundness of the element's corners.

You may recall from an earlier challenge that the box-shadow property takes values for offset-x, offset-y, blur-radius, spread-radius and a color value in that order. The blur-radius and spread-radius values are optional.

To animate an element, you need to know about the animation properties and the @keyframes rule. The animation properties control how the animation should behave and the @keyframes rule controls what happens during that animation. There are eight animation properties in total. This challenge will keep it simple and cover the two most important ones first:

animation-name sets the name of the animation, which is later used by @keyframes to tell CSS which rules go with which animations.

animation-duration sets the length of time for the animation.

@keyframes is how to specify exactly what happens within the animation over the duration. This is done by giving CSS properties for specific "frames" during the animation, with percentages ranging from 0% to 100%. If you compare this to a movie, the CSS properties for 0% is how the element displays in the opening scene. The CSS properties for 100% is how the element appears at the end, right before the credits roll. Then CSS applies the magic to transition the element over the given duration to act out the scene.

``` <style>
  div {
    height: 40px;
    width: 70%;
    background: black;
    margin: 50px auto;
    border-radius: 5px;
  }

  #rect {
    animation-name: rainbow; 
    animation-duration: 4s;  
  }

  @keyframes rainbow {
    0% {
      background-color: blue; 
    }
    50% {
      background-color: green;
    }
    100% {
      background-color: yellow;
    }
  }
  }

</style>
<div id="rect"></div>
```
