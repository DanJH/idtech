# Python Review
<i>Created by Scrappy
Summer 2019</i>
## Data
### Naming variables:
- Name must start with a Latin letter
- No symbols besides `_` allowed
- Must be one word
- Try to choose names that represent what they do
### Datatypes
- Strings - made up of characters and words, must have quotations or apostrophe marks around them
`variable = "Hello world"`
- Integers - made up of whole numbers
`variable = 1234`
- Floats - otherwise known as floating point numbers, they contain numbers with decimals
`variable = 12.345`
- Booleans - a variable with two states, either `True` or `False`
`variable = True`

## Input and Output
### Output
- Use `print()` function to print to console
- Note that in order to print a string, quotation marks must be used
`print("string")`
`print(variable)`
### Input
- Use `input()` function to intake data from the keyboard
- Python will wait until something is typed and entered before moving on from the block of code
`variable = input()`
## Boolean Logic
### Intro
- Based on idea that a computer has two states: `1` and `0`
- Boolean has two states either `True` or `False`
- All Boolean must be ask-able
	- Ask *Can this either be true or false?*
### Boolean operators
- AND / `and` - Combines two booleans and both must be true in order for the statement to be true, if one is false, then the entire statement is false
- OR / `or` - Combines two booleans, if one is true then all is true, both must be false in order for the statement to be false
- NOT / `not` - Negates the boolean, i.e. changes true to false or false to true
- `==` - checks if is equal, i.e. will be true if two things are the same and false if differs
- `!=` - checks that variables are unequal and differ, i.e. returns true if two variables differ
- `>` - returns true if left variable is greater than the right
- `<` - returns true if right variable is greater than the left 
### If-Then-Else Statements
- `if` checks a conditional (a Boolean statement) and will run the indented block of code underneath if true, otherwise the indented code underneath will be skipped
- If the `if` is false than it will skip the indented code under `if` and `else` will be ran
- `elif` is another if statement
`if boolean:`
>> `# stuff to do if true`
- `else:`
>>`# stuff to do if false`

## Functions
- Used to reduce replicated code
- Rather than calling the same code over and over, you can just call a function
- Functions can return values, which will then substitute for the name
- `def functionName(input):`
>>`#do stuff`
>`return input #substitues the function name`

## Using LEDs and Buttons
### Introduction
- In order to use LEDs and Buttons we must tell Python what they are
	- To do this we import LEDs and/or buttons:
	- `from gpiozero import LED, button`
	- This must be done in the beginning of the file in order for everything underneath it to recognize it
### Making connections
- In order to connect and control circuts, we must connect to the proper ports
- [Click here](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/24018065367/original/ProtoPlus.pdf?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAJ2JSYZ7O3I4JO6DA%2F20190624%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20190624T160700Z&X-Amz-Expires=300&X-Amz-Signature=971f2e146e7af306eac7a21120987a67e3cc60dcf380d84ca76af3baee96aa5e&X-Amz-SignedHeaders=Host&response-content-type=application%2Fpdf) for a list of ports on the Proto Plus board
- In order to create a light or a button we use:
- `newButton = Button(PIN)`
- or
- `newLED = LED(PIN)`
### Controlling circuits
- Once the buttons or lights have been set up, we can use commands to control them:
#### LED Specific
- To turn on/off:
>>`newLED.on()`
> > `newLED.off()`
> >`newLED.toggle() #does opposite of current state`
- To blink
>>`newLED.blink(timeOn, timeOff, [howManyRepeats]) # Note that [] refers to optional`
#### Button Specific:
- To make the computer wait until a button has been pressed/released:
>>`newButton.wait_for_press()`
>>`newButton.wait_for_release()`
- Various variables are attached to the button as well:
	- `newButton.held_time` returns the time the button is being held
	- `newButton.hold_time` is the amount of time needed to hold in order to activate
	- `newButton.is_held` returns true when the button is held for long enough (hold_time), otherwise false
	- `newButton.is_pressed` returns true if currently pressed, otherwise false

## Sonic Pi and Various Other Libraries
- To use Sonic Pi, it must be imported:
> `from ptprotoplus import psonic`
- Other libraries are imported similarly
> `from ptprotoplus import adc`
> `from time import sleep`
### Time functions
- We used
- `time()` returns the current time in seconds
- `sleep(x)` pauses the code for a desired time, the time is changeable by changing `x`
### Sonic Pi Functions
- `psonic.play(note)` replace note with a value and it will play the note
- `psonic.load_sample('sample name', <sample directory>)` In order to play a sample, it must be loaded and told where it is located
- `psonic.play_sample('sample name')` This will play the sample given by the name
### Sensors
- `adc = adc.ADCProbe()` This will activate ADCProbe and set it to a variable
- `adc.get_reading(port)` Replace the port with the port connected

# Thank you for being amazing students!
## Hope to see you next year!
