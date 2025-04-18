# Custom-Alert

Hello Everyone i created this Custom Alert package that can easily integrate with your website.

## How to Use:

### Step1:-
First install using this command: ```npm i @pranshupatel/custom-alert```

### Step2:-
Import the function by adding below line in the top of your script file.
```js
import {customAlert, Position, Alerttype} from './node_modules/@pranshupatel/custom-alert/script.js';
```

Also add ```type='module'``` in your script declaration in HTML.
```HTML
<script defer type="module" src="./script.js"></script>
```
### Step3:-
Call the customAlert function in your script.

Here,
- first property in object is type of the message (success,error).
- second property in object is position of the message (top-left,top-center,top-right,bottom-left,bottom-center,bottom-right);
- third property in object is the message you want to show.
- fourth property in object is the timer which is optional by default it is of 3000ms(3 seconds).

Ex:- Showing success message at top-right position
```js
customAlert({
    type:Alerttype.Success,
    position: Position.Top_Right,
    message: "Success message"
});
```

Ex:- Showing error message at top-right position
```js
customAlert({
    type:Alerttype.Error,
    position: Position.Top_Right,
    message: "Error message"
});
```

Ex:- Showing success message at top-right position till time( in ms ) provided 
```js
customAlert({
    type: Alerttype.Success,
    position: Position.Top_Right,
    message: "Success message",
    timer: 5000
})
```