angular-confirm-click
=====================

An AngularJS directive which will display a confirmation message when a user clicks on a button, all inline.

The buttons text will be replaced with the confirmation message on first click, then the subsequent click will 
perform the action. There are also css animations which will increase and decrease the size of the button elegantly.

install
-------

```
bower install angular-confirm-click
```

usage
-----

Make sure you include the module in your application config

```
angular.module('myApp', [
  'confirmClick',
  ...
]);
```

Use the directive on a clickable element, like a button.

```
<button confirm-click="delete(item);" confirm-message="Are you sure?">Delete</button>
```

The text in the button is as expected
```
angular.element('button').text() === 'Delete';
```

When the user clicks on the button, the text will change in the button

```
angular.element('button').text() === 'Are you sure?';
```

When the user clicks again, the action `delete(item);` will be performed

If the user does not confirm, the text reverts back to `Delete` after 1500ms
