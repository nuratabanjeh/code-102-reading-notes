# class09

## HTML Forms:

The HTML form is used to collect user input. The user input can then be sent to a server for processing.

![HTML FORMS](https://mobile.htmlgoodies.com/imagesvr_ce/1902/HTML%20Form.PNG)

## The form Element:

The HTML `<form>` element defines a form that is used to collect user input:

`<form>`

form elements

`</form>`

### How does an HTML form work?

A web form has two parts: the HTML ‘front end’ and a back end form processor. The HTML front end part handles the presentation while the back end handles the form submissions (like saving the form submissions, sending emails etc). The back end form processor script is usually written in languages like PHP, ASP or Perl.

1. A visitor visits a web page that contains a form.

2. The web browser displays the HTML form.

3. The visitor fills in the form and submits.

4. The browser sends the submitted form data to the web server.

5. A form processor script running on the web server processes the form data.

6. A response page is sent back to the browser.

## The `<input>` Element :

The `<input>` element is the most important form element.The `<input>` element is displayed in several ways, depending on the type attribute.

## Text Fields:

`<input type="text">` defines a single-line input field for text input.

## The `<label>` Element :

Notice the use of the `<label>` element in the example above.

The `<label>` tag defines a label for many form elements.

The `<label>` element is useful for screen-reader users, because the screen-reader will read out loud the label when the user is focused on the input element.

The `<label>` element also help users who have difficulty clicking on very small regions (such as radio buttons or checkboxes) - because when the user clicks the text within the `<label>` element, it toggles the radio button/checkbox.

The for attribute of the `<label>` tag should be equal to the id attribute of the `<input>` element to bind them together.

## The Submit Button:

`<input type="submit">` defines a button for submitting the form data to a form-handler.

The form-handler is typically a page on the server with a script for processing input data.

The form-handler is specified in the form's action attribute.

## The Action Attribute:

The action attribute defines the action to be performed when the form is submitted. Usually, the form data is sent to a page on the server when the user clicks on the submit button. In the example above, the form data is sent to a page on the server called "/action_page.php". This page contains a server-side script that handles the form data:

`<form action="/action_page.php">`

## The Target Attribute:

The target attribute specifies if the submitted result will open in a new browser tab, a frame, or in the current window The default value is _self which means the form will be submitted in the current window. To make the form result open in a new browser tab, use the value _blank.

## HTML Input Types:

Here are the different input types you can use in HTML:

`<input type="button">`

`<input type="checkbox">`

`<input type="color">`

`<input type="date">`

`<input type="datetime-local">`

`<input type="email">`

`<input type="file">`

`<input type="hidden">`

`<input type="image">`

`<input type="month">`

`<input type="number">`

`<input type="password">`

`<input type="radio">`

`<input type="range">`

`<input type="reset">`

`<input type="search">`

`<input type="submit">`

`<input type="tel">`

`<input type="text">`

`<input type="time">`

`<input type="url">`

`<input type="week">`

## JavaScript Events

HTML events are "things" that happen to HTML elements. When JavaScript is used in HTML pages, JavaScript can "react" on these events.

## HTML Events :

An HTML event can be something the browser does, or something a user does.

Here are some examples of HTML events:

* An HTML web page has finished loading

* An HTML input field was changed

* An HTML button was clicked

Often, when events happen, you may want to do something.

JavaScript lets you execute code when events are detected.

HTML allows event handler attributes, with JavaScript code, to be added to HTML elements.

* With single quotes:

`<element event='some JavaScript'>`

* With double quotes:

`<element event="some JavaScript">`

In the following example, an onclick attribute (with code), is added to a element:

Example : `<button onclick="document.getElementById('demo').innerHTML = Date()">The time is?</button>` In the example above, the JavaScript code changes the content of the element with id="demo".

In the next example, the code changes the content of its own element (using this.innerHTML):

Example : `<button onclick="this.innerHTML = Date()">The time is? </button>` JavaScript code is often several lines long. It is more common to see event attributes calling functions:

Example : `<button onclick="displayDate()">The time is?</button>`

## What can JavaScript Do?

Event handlers can be used to handle, and verify, user input, user actions, and browser actions:

* Things that should be done every time a page loads

* Things that should be done when the page is closed

* Action that should be performed when a user clicks a button

* Content that should be verified when a user inputs data

* And more 

## Many different methods can be used to let JavaScript work with events:

* HTML event attributes can execute JavaScript code directly

* HTML event attributes can call JavaScript functions

* You can assign your own event handler functions to HTML elements

* You can prevent events from being sent or being handled

**Thankyou**