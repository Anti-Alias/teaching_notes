# Project Summary 
We're going to be creating an HTML form from scratch. No training wheels! You're free to ask me questions as you work.
Once the HTML form looks right, we'll hook it up with JavaScript and have
the form respond to when the user clicks "submit" at the bottom.
I've included relevant guides that you can consult. 
Part of being a software dev is researching. That never stops, no matter how experienced you become.
You may use Chat-GPT for research as well, but I expect you to:
1) Verify its claims through Google (W3Schools and MDN are good resources)
2) Type out your own code. Try to avoid copying-and-pasting.
3) Suffer. If I had to, then so do you.

## Non Goals
The form need not be pretty or centered, though if you want to go above and beyond, style away!
Prioritize functionality.

## Requirements 

### HTML
* Page should have a header (\<h1> element) with the title "Sign Up".
    - Note: Honestly, call it whatever you want.
* Form must have the following \<input> fields:
    - Username
        * Make input type "text" with no special validations.
    - Email
        * Make input type "email", which gives it built-in email validation.
    - Password 
        * Make input type "password", which hides the characters being typed.
    - Date of Birth
        * Make input type "date", which presents the user with a native date-picker.
    - Submit
        * Make input type "submit", which transforms the input into a submit button.

Once you've written your HTML, try clicking the submit button.
You should see some built-in validation at play, assuming you left your fields empty.
Be sure to remember to refresh the page whenever you make changes to your HTML file!

### JavaScript
* Hook up your own JavaScript file to your HTML file with the \<script> element.
  and verify that it's being called with a `console.log('testing')` or `window.alert('testing')`.
* Create a function that gets run (called, invoked, etc) when you hit the submit button.
  Hint: You'll need to use these built-functions:
    - *getElementById* to get a "reference" to the form element.
    - *addEventListener* to tell the form "call my function when the user clicks on the submit button". 
* Write validation code that ensures that the username is:
    - Not empty. Hint: You'll need an "if statement" that checks if the string is "truthy". See docs at bottom.
    - Does not include dashes (Hint: You'll need an "if statement", and the "contains" function)
    - If validation fails, the UI should display an error message at the bottom of the form stating what went wrong.

## Documentation
* [HTML Basics](https://www.freecodecamp.org/news/introduction-to-html-basics/)
* [HTML Form Basics](https://www.freecodecamp.org/news/how-to-use-html-forms/)
* [W3Schools Docs on Forms](https://www.w3schools.com/tags/tag_form.asp)
* [Guide on How To Have JS React to Form Submission](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest_API/Using_FormData_Objects)
* [Docs on Truthiness (Yes, it's really called that...)](https://developer.mozilla.org/en-US/docs/Glossary/Truthy)