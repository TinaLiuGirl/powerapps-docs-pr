<properties
    pageTitle="Add picture control: reference | Microsoft PowerApps"
    description="Information, including properties and examples, about the Add picture control"
    services=""
    suite="powerapps"
    documentationCenter="na"
    authors="fikaradz"
    manager="anneta"
    editor=""
    tags=""/>

<tags
   ms.service="powerapps"
   ms.devlang="na"
   ms.topic="article"
   ms.tgt_pltfrm="na"
   ms.workload="na"
   ms.date="10/25/2016"
   ms.author="fikaradz"/>

# Add picture control in PowerApps #
Takes a photo or loads images from the local device.

## Description ##
With this control users can take photos or upload image files from their device and update the data source with this content. On a mobile device the user is presented with the device's choice dialog to choose between taking a photo or selecting one already available.

This control is a composite control, made up of two controls.  Press or tap once to select the outer control that shows the image that has been loaded.  Press or tap again to select the inner label control.

## Outer control properties ##

These properties apply to the outer control.

**[BorderColor](properties-color-border.md)** – The color of a control's border.

**[BorderStyle](properties-color-border.md)** – Whether a control's border is **Solid**, **Dashed**, **Dotted**, or **None**.

**[BorderThickness](properties-color-border.md)** – The thickness of a control's border.

**[DisplayMode](properties-core.md)** – Whether the control allows user input (**Edit**), only displays data (**View**), or is disabled (**Disabled**).

**[DisabledBorderColor](properties-color-border.md)** – The color of a control's border if the control's **[DisplayMode](properties-core.md)** property is set to **Disabled**.

**[DisabledFill](properties-color-border.md)** – The background color of a control if its **[DisplayMode](properties-core.md)** property is set to **Disabled**.

**Error** - If there is a problem uploading an image, this property will contain an appropriate error string.

**[Fill](properties-color-border.md)** – The background color of a control.

**[Height](properties-size-location.md)** – The distance between a control's top and bottom edges.

**[HoverBorderColor](properties-color-border.md)** – The color of a control's border when the user keeps the mouse pointer on that control.

**[HoverFill](properties-color-border.md)** – The background color of a control when the user keeps the mouse pointer on it.

**Media** – An identifier for the clip that an audio or video control plays.

**[OnSelect](properties-core.md)** – How the app responds when the user taps or clicks a control.

**[PressedBorderColor](properties-color-border.md)** – The color of a control's border when the user taps or clicks that control.

**[PressedFill](properties-color-border.md)** – The background color of a control when the user taps or clicks that control.

**[Visible](properties-core.md)** – Whether a control appears or is hidden.

**[Width](properties-size-location.md)** – The distance between a control's left and right edges.

**[X](properties-size-location.md)** – The distance between the left edge of a control and the left edge of its parent container (screen if no parent container).

**[Y](properties-size-location.md)** – The distance between the top edge of a control and the top edge of the parent container (screen if no parent container).

## Inner text properties ##

These properties apply to the inner label control that by default says "Tap or click to add a picture".  To select this inner control, press or tap the **Add picture** control once, and then again.

**[Align](properties-text.md)** – The location of text in relation to the horizontal center of its control.

**[Color](properties-color-border.md)** – The color of text in a control.

**[DisabledColor](properties-color-border.md)** – The color of text in a control if its **[DisplayMode](properties-core.md)** property is set to **Disabled**.

**[Font](properties-text.md)** – The name of the family of fonts in which text appears.

**[FontWeight](properties-text.md)** – The weight of the text in a control: **Bold**, **Semibold**, **Normal**, or **Lighter**.

**[HoverColor](properties-color-border.md)** – The color of the text in a control when the user keeps the mouse pointer on it.

**[Italic](properties-text.md)** – Whether the text in a control is italic.

**[OnChange](properties-core.md)** – How the app responds when the user changes the value of a control (for example, by adjusting a slider).

**[Padding](properties-size-location.md)** – The distance between the text on an import or export button and the edges of that button.

**[PressedColor](properties-color-border.md)** – The color of text in a control when the user taps or clicks that control.

**[Size](properties-text.md)** – The font size of the text that appears on a control.

**[Strikethrough](properties-text.md)** – Whether a line appears through the text that appears on a control.

**[Text](properties-core.md)** – Text that appears on a control or that the user types into a control.

**[Underline](properties-text.md)** – Whether a line appears under the text that appears on a control.

**[VerticalAlign](properties-text.md)** – The location of text on a control in relation to the vertical center of that control.

## Related functions ##

[**Patch**( *DataSource*, *BaseRecord*, *ChangeRecord* )](../functions/function-patch.md)

## Example ##
### Add images to an Image gallery control ###
1. Add an **Add picture** control, and then triple-click it.

	Don't know how to [add, name, and configure a control](../add-configure-controls.md)?

1. In the **Open** dialog box, click or tap an image file, and then click or tap **Open**.

1. Add a **[Button](control-button.md)** control, move it under the **Add picture** control, and set the **[OnSelect](properties-core.md)** property for the **[Button](control-button.md)** control to this formula:<br>
**Collect(MyPix, AddMediaButton1.Media)**

	Want more information about the **[Collect](../functions/function-clear-collect-clearcollect.md)** function or [other functions](../formula-reference.md)?

1. Add an **Image gallery** control, and set its **[Items](properties-core.md)** property to **MyPix**.

1. Press F5, and then click or tap the **[Button](control-button.md)** control.

	The image from the **Add picture** control appears in the **Image gallery** control. If your image doesn't have the same aspect ratio as the **[Image](control-image.md)** control in the **Image gallery** control, set the **[ImagePosition](properties-visual.md)** property of the **[Image](control-image.md)** control to **Fit**.

1. Click or tap the **Add picture** control, click or tap another image file, click or tap **Open**, and then click or tap the **[Button](control-button.md)** control that you added.

	The second image appears in the **Image gallery** control.

1. (optional) Repeat the previous step one or more times, and then return to the default workspace by pressing Esc.

Use the **[SaveData](../functions/function-savedata-loaddata.md)** function to save the images locally or the **[Patch](../functions/function-patch.md)** function to update a data source.
