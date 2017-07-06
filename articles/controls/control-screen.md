<properties
    pageTitle="Screen control: reference | Microsoft PowerApps"
    description="Information, including properties and examples, about a Screen control"
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

# Screen control in PowerApps #
A UI element that contains one or more other controls in an app.

## Description ##
Most apps have multiple **Screen** controls that contain **[Label](control-text-box.md)** controls, **[Button](control-button.md)** controls, and other controls that show data and support navigation.

## Key properties ##

**[BackgroundImage](properties-visual.md)** – The name of an image file that appears in the background of a screen.

**[Fill](properties-color-border.md)** – The background color of a control.

## Additional properties ##

**[ImagePosition](properties-visual.md)** – The position (**Fill**, **Fit**, **Stretch**, **Tile**, or **Center**) of an image in a screen or a control if it isn't the same size as the image.

**OnHidden** – The behavior of an app when the user navigates away from a screen.

**OnVisible** – The behavior of an app when the user navigates to a screen.

**OnStart** – The behavior of the app when the user opens the app.

- The formula to which this property is set runs before the first screen of the app appears. Call the [**Navigate**](../functions/function-navigate.md) function to change which screen appears first when the app starts.

- You can't set [context variables](../workding-with-variables.md) with the [**UpdateContext**](../functions/function-updatecontext.md) function because no screen has appeared yet. However, you can pass context variables in the **Navigate** function and create and fill a [collection](../workding-with-variables.md) by using the [**Collect**](../functions/function-collect.md) function.

- When you update an app, the formula to which this property is set runs when the app is loaded into PowerApps Studio. To see the impact of changing this property, you'll need to save, close, and reload your app.

- The **OnStart** property is actually a property of the app, not the screen. For editing convenience, you view and modify it as a property on the first screen of your app. If you remove the first screen or reorder screens, this property may become hard to find. In this case, save, close, and reload your app, and the property will reappear as a property of the first screen.

## Related functions ##

[**Distinct**( *DataSource*, *ColumnName* )](../functions/function-distinct.md)

## Example ##
1. Add a **[Radio](control-radio.md)** control, name it **ScreenFills**, and set its **[Items](properties-core.md)** property to this value:<br>
**["Red", "Green"]**

	Don't know how to [add, name, and configure a control](../add-configure-controls.md)?

1. Name the default **Screen** control **Source**, add another **Screen** control, and name it **Target**.

1. On **Source**, add a **[Shape](control-shapes-icons.md)** control (such as an arrow), and set its **[OnSelect](properties-core.md)** property to this formula:<br>
**Navigate(Target, ScreenTransition.Fade)**

	Want more information about the **[Navigate](../functions/function-navigate.md)** function or [other functions](../formula-reference.md)?

1. In **Target**, add a **[Shape](control-shapes-icons.md)** control (such as an arrow), and set its **[OnSelect](properties-core.md)** property to this formula:<br>
**Navigate(Source, ScreenTransition.Fade)**

1. Set the **[Fill](properties-color-border.md)** property of **Target** to this formula:<br>
**If("Red" in ScreenFills.Selected.Value, RGBA(255, 0, 0, 1), RGBA(54, 176, 75, 1))**

1. From **Source**, press F5, click or tap either option in the **[Radio](control-radio.md)** control, and then click or tap the **[Shape](control-shapes-icons.md)** control.

	**Target** appears in the color that you chose.

1. On **Target**, click or tap the **[Shape](control-shapes-icons.md)** control to return to **Source**.

1. (optional) Click or tap the other option in the **[Radio](control-radio.md)** control, and then click or tap the **[Shape](control-shapes-icons.md)** control to confirm that **Target** appears in the other color.

1. To return to the default workspace, press Esc.
