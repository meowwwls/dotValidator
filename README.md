# dotValidator


dotValidator is a group of HTML/CSS/JavaScript Inputs with on the fly validation.  You can see a live demo [at this location].

##User validation requirements

###Search

Requires at least three characters

###Email

Checks for an @ symbol that is neither the start or end of the address

- This could be improved

###Phone Number

- Checks for nine digits
- Does not include hyphens in the count
	- 555-555-5555 is valid
- Allows 10 digits if the first digit is "1"
	- 1-555-555-5555 is valid
	
###Generic Number

Checks user input is a number.  Forced in HTML5.

###Date of Birth

Checks for a valid date

Forced in HTML5

###Age

Not an actual input.  The data will be automatically pulled from Date of Birth.  Compares todays today and calculates the age.

If age is 18 or older, age validated.

###Password

- Check for a minimum length of 12 characters
- Check for at least one symbol

Note that the password requirements are based on recent security research from [Microsoft](https://www.semperis.com/microsoft-upends-traditional-password-recommendations-with-significant-new-guidance/) and [Symnatec](https://www.technologyreview.com/s/542576/youve-been-misled-about-what-makes-a-good-password/)

###Username

- Checks for minimum of five characters
- Checks input is alphanumeric

###Zipcode

- Must be numerical
- Must be five or 9 digits
- 10 digits allowed for one hyphen
	- 12345-9806 is valid
- Hyphen not allowed if exactly six digits
	- 12345- is not valid
	
##Usage

###General Usage

Link to the stylesheet.css and dotValid.js

Copy and paste the code from the html file for any inputs you wish to import.

###Turning on and off the dotValidator

The inputs have an attribute:

	data-dotvalid="true"
	
Remove attribute or set to false if you don't want a specific input to have the validator.

###Changing the size of the validator dot

In the stylesheet, find class "validation-dot."

You can change the width and height here.  If you want to keep the dot circular keep both width and height equal.  Be aware you may also have to change the border-radius.

###Changing the input size

The inputs will adjust the the size of their container.  In most cases, you don't want to modify an input size directly.

Modifying the container div, ideally by adding a new class.

If you want to modifying the size of all inputs change values of class "ui-input-container."

For the age pseudo-input, the size is controlled by id "dot-valid-age".

###Changing the dot validation colors

By default, the validation colors for the dots are:

- No User Input
	- \#F2617A
 
 - Invalid Input
 	- \#EDBE69
 	
 - Valid Input
 	- \##31E96B
 	
 These three variables are at the very top of the dotValid.js file.
 
 Changing the values here will change them for every input.
 
 *Also be aware:*
 
 The dot color on page load is defined in the CSS class "validation-dot" via the background-color.
 
 By default it is equal to the "no user input" color.
 
 If you change that, and you want the default color to be equal to the no input color, you'll have to change that value in CSS as well.
 
## ToDo:

- Create a "Vanilla" version without the prestyling.