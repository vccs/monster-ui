title: dialog()

# monster.ui.dialog()
The `monster.ui.dialog()` method generates a dialog window with the look and feel of Monster UI.

## Syntax
```javascript
monster.ui.dialog([content, options]);
```

### Parameters
Key | Description | Type | Default | Required
:-: | --- | :-: | :-: | :-:
`content` | Either a string representation or a jQuery object that will be inserted inside the dialog widget. | `String`, `jQuery` | | `true`
`options` | Let you override default options that can be found on the [jQuery UI Dialog Widget][dialog_widget] page. The only options that cannot be overridden are `show`, `hide` and the `close` method. | `Object` | | `false`

### Return
A jQuery object representing the dialog widget.

## Description
The dialog widget generated by the `monster.ui.dialog()` method contains a bar with a title and an `x` icon on the top right to close it. The section below the title bar is were the HTML template, specified as the `content` parameter, will be rendered.

This method use the [jQuery UI Dialog Widget][dialog_widget] to generate the dialog widget and then applies CSS styles specific to Monster UI.

## Examples
### Create a dialog widget
```javascript
var template = $(app.getTemplate({
  name: 'dialog-failover'
}));

monster.ui.dialog(template, {
    title: app.i18n.active().dialog.failover.title,
    width: '540px'
});
```

![Image showing a simple Monster-UI popup](http://i.imgur.com/bEdqrcJ.png)

As shown in the example above, the method only generates the part inside the red rectangle and the template's container.

[dialog_widget]: http://api.jqueryui.com/dialog/
