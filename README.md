# FocusHelper widget

A helper tool that can set the focus on a form-control triggered by logic such as a microflow, nanoflow or pageload.

## Contributing

For more information on contributing to this repository visit [Contributing to a GitHub repository](https://world.mendix.com/display/howto50/Contributing+to+a+GitHub+repository)!

## Description

The custom widget is linked to the formfield you wish to add focus on when specific events happen via Microflows, Nanoflows or even the starting of a page. All you need to do is create an attribute in the context object to trigger the focus on and the widget will take care of the rest. You can even trigger a microflow after the focus has been set for e.g. resetting the attribute that causes the trigger.

## Implementation steps

1. Give the formfield that you need to trigger a focus on a unique name.
2. Add the custom widget after the formfield and enter the name of the formfield in its settings.
3. Select the context object and it's attribute you want to trigger the focus on.
4. Optionally add a microflow to trigger after the focus has been set.
5. Run the project.

## Notes

The custom widget itself is a very simple widget but the behaviour with Mendix logic can make it a powerful tool. It just needs modeling some logic. E.g. adding focus on the message input field after clicking on the "add message" button.

At the moment, the widget does check for a readonly state and if the formfield is in fact readonly, it will not trigger a focus on the formfield. However, this mechanism is not compatible with conditional editability - as it is not possible for the custom widget to detect the current state. This is not really a problem as the triggering of the focus event is not harmful in any way. However, if you did model more complex logic to be performed after the focus event, it might be good to check the readonly state in that microflow to avoid errors in business logic.

## Release Notes

Appstore 1.0.1 release:

- Merge fixes from @tieniber
- Verify working in Mendix 8.0 and 9.0
  Appstore 1.0.0 release:
- initial version of the widget
