# Plants

Cabbage plants are simply groups of widgets that are bound to a parent widget. All widgets contained within a plant have top and left positions which are relative the the top left position of the parent. Resizing the plant will in turn resize all the widgets contained within. As of Cabbage version 2, plants can now be placed within plants, but note that dynamically resizing plants within plants using the GUI editor may lead to unpredictable behaviour.  

Plants are created by enclosing a group of widgets within curly brackets. In the code below an image is set up as a plant, or parent widget. The plant has three child sliders, which all use relative coordinates. For example, the first checkbox will appear 20 pixels from the rightmost edge of the image, and 4 pixels from the topmost edge. 

```csharp
image bounds(6, 0, 300, 200), colour(255, 0, 0, 255)
{
checkbox bounds(20, 4, 121, 38), channel("mute1"), text("Mute Channel 1")
checkbox bounds(20, 44, 119, 38), channel("mute2"), text("Mute Channel 2")
combobox bounds(20, 100, 155, 30), channel("waveform"), value(2), text("Sine", "Square", "Sawtooth") 
}
``` 

The major advantage in using plants is that you can easily move and resize all widgets in one action. You can also save your plants and recall them later from a plant repository. Plants are intended to be reused across instruments so users do not have to keep rebuilding GUIs from scratch. Looks through the examples provided with Cabbage to see how plants are used there.  

> Note: Plants have to be created manually. Opening brackets must appear on either the same line as the plant widget, or the following line. Plants cannot be declared inline, meaning they must be spread over a number of lines. 

For more advanced uses of plants, see [Custom plant imports](./custom_plant_imports.md)
![Plants](images/plants.gif)