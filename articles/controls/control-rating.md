<properties
    pageTitle="Rating control: reference | Microsoft PowerApps"
    description="Information, including properties and examples, about the Rating control"
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

# Rating control in PowerApps #
A control with which users can indicate a value between 1 and a maximum number that you specify.

## Description ##
In this control, the user can indicate, for example, how much they liked something by selecting a certain number of stars.

## Key properties ##

**[Default](properties-core.md)** – The initial value of a control before it is changed by the user.

**Max** – The maximum value to which the user can set a slider or a rating.

## Additional properties ##

**[BorderColor](properties-color-border.md)** – The color of a control's border.

**[BorderStyle](properties-color-border.md)** – Whether a control's border is **Solid**, **Dashed**, **Dotted**, or **None**.

**[BorderThickness](properties-color-border.md)** – The thickness of a control's border.

**[FocusedBorderThickness](properties-color-border.md)** – The thickness of the control's border when it has keyboard focus.

**[DisplayMode](properties-core.md)** – Whether the control allows user input (**Edit**), only displays data (**View**), or is disabled (**Disabled**).

**[Fill](properties-color-border.md)** – The background color of a control.

**[Height](properties-size-location.md)** – The distance between a control's top and bottom edges.

**[OnChange](properties-core.md)** – How the app responds when the user changes the value of a control (for example, by adjusting a slider).

**[OnSelect](properties-core.md)** – How the app responds when the user taps or clicks a control.

**RatingFill** – The color of the stars in a rating control.

**ReadOnly** – Whether a user can change the value of a slider or rating control.

**[Reset](properties-core.md)** – Whether a control reverts to its default value.

**ShowValue** – Whether a slider's or rating's value appears as the user changes that value or hovers over the control.

**[TabIndex](properties-accessibility.md)** – Customizes the tab order of controls at runtime when set to a non-zero value.

**[Tooltip](properties-core.md)** – Explanatory text that appears when the user hovers over a control.

**[Visible](properties-core.md)** – Whether a control appears or is hidden.

**[Width](properties-size-location.md)** – The distance between a control's left and right edges.

**[X](properties-size-location.md)** – The distance between the left edge of a control and the left edge of its parent container (screen if no parent container).

**[Y](properties-size-location.md)** – The distance between the top edge of a control and the top edge of the parent container (screen if no parent container).

## Related functions ##

[**Average**( *Value1*, *Value2,* ... )](../functions/function-aggregates.md)

## Example ##
1. Add a **Rating** control, and name it **Quantitative**.

	Don't know how to [add, name, and configure a control](../add-configure-controls.md)?

1. Add a **[Text input](control-text-input.md)** control, name it **Qualitative**, and move it below the **Rating** control.

1. Set the **[Default](properties-core.md)** property of the **[Text input](control-text-input.md)** control to **""**, and set its **HintText** to this formula:
<br>**If(Quantitative.Value > 3, "What did you especially like?", "How might we do better?")**

	Want more information about the **[If](../functions/function-if.md)** function or [other functions](../formula-reference.md)?

1. Press F5, and then click or tap either four or five stars in the **Rating** control.

	The hint text in the **[Text input](control-text-input.md)** control changes to reflect the high rating.

1. Click or tap fewer than four stars in **Quantitative**.

	The hint text in the **[Text input](control-text-input.md)** control changes to reflect the low rating.

1. To return to the default workspace, press Esc.
