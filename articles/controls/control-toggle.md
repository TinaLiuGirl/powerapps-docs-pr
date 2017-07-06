<properties
    pageTitle="Toggle control: reference | Microsoft PowerApps"
    description="Information, including properties and examples, about the toggle control"
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

# Toggle control in PowerApps #
A control that the user can turn on or off by moving its handle.

## Description ##
A toggle is designed for recent GUIs but behaves the same way as a check box.

## Key properties ##

**[Default](properties-core.md)** – The initial value of a control before it is changed by the user.

**[Value](properties-core.md)** – The value of an input control.

## Additional properties ##
**[BorderColor](properties-color-border.md)** – The color of a control's border.

**[BorderStyle](properties-color-border.md)** – Whether a control's border is **Solid**, **Dashed**, **Dotted**, or **None**.

**[BorderThickness](properties-color-border.md)** – The thickness of a control's border.

**[FocusedBorderThickness](properties-color-border.md)** – The thickness of the control's border when it has keyboard focus.

**[DisplayMode](properties-core.md)** – Whether the control allows user input (**Edit**), only displays data (**View**), or is disabled (**Disabled**).

**[DisabledBorderColor](properties-color-border.md)** – The color of a control's border if the control's **[DisplayMode](properties-core.md)** property is set to **Disabled**.

**[Fill](properties-color-border.md)** – The background color of a control.

**[Height](properties-size-location.md)** – The distance between a control's top and bottom edges.

**[HoverBorderColor](properties-color-border.md)** – The color of a control's border when the user keeps the mouse pointer on that control.

**[OnChange](properties-core.md)** – How the app responds when the user changes the value of a control (for example, by adjusting a slider).

**OnCheck** – How an app responds when the value of a checkbox or a toggle changes to **true**.

**[OnSelect](properties-core.md)** – How the app responds when the user taps or clicks a control.

**OnUncheck** – How an app responds when the value of a checkbox or a toggle changes to **false**.

**[PressedBorderColor](properties-color-border.md)** – The color of a control's border when the user taps or clicks that control.

**RailFill** – The background color of the rectangle in a toggle control when its value is **false** or the color of the line to the right of the handle in a slider control.

**RailHoverFill** – When you hover on a toggle control or a slider, the background color of the rectangle in a toggle control when its value is **false** or the color of the line to the right of the handle in a slider control.

**[Reset](properties-core.md)** – Whether a control reverts to its default value.

**[TabIndex](properties-accessibility.md)** – Customizes the tab order of controls at runtime when set to a non-zero value.

**[Tooltip](properties-core.md)** – Explanatory text that appears when the user hovers over a control.

**ValueFill** – The background color of the rectangle in a toggle control when its value is **true** or the color of the line to the left of the handle in a slider control.

**ValueHoverFill** – When you keep the mouse pointer on a toggle control or a slider, the background color of the rectangle in a toggle control when its value is **true** or the color of the line to the left of the handle in a slider control.

**[Visible](properties-core.md)** – Whether a control appears or is hidden.

**[Width](properties-size-location.md)** – The distance between a control's left and right edges.

**[X](properties-size-location.md)** – The distance between the left edge of a control and the left edge of its parent container (screen if no parent container).

**[Y](properties-size-location.md)** – The distance between the top edge of a control and the top edge of the parent container (screen if no parent container).

## Related functions ##

[**If**( *Condition*, *Result* )](../functions/function-if.md)

## Example ##
1. Add a toggle, and name it **MemberDiscount**.

	Don't know how to [add, name, and configure a control](../add-configure-controls.md)?

1. Add a label, and set its **[Text](properties-core.md)** property to this formula:
<br>**If(MemberDiscount.Value = true, "Price: $75", "Price: $100")**

	Want more information about the **[If](../functions/function-if.md)** function or [other functions](../formula-reference.md)?

1. Press F5, and change the value of **MemberDiscount**.

	The label shows a different price, depending on whether **MemberDiscount** is on or off.

1. To return to the default workspace, press Esc.
