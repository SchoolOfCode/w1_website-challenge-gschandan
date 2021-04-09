# Website Challenge

## Client Brief
- a single web profile page describing the client
- no specific design directives - creative freedom

## Design
### Theme
Windows 95 era BSOD combined with some elements from traditional BIOS interfaces to incorporate interactive elements.  
![alt text](https://github.com/SchoolOfCode/w1_website-challenge-gschandan/blob/main/images/windows_bsod.jpg "Example image of windows blue screen of death")
![alt text](https://github.com/SchoolOfCode/w1_website-challenge-gschandan/blob/main/images/windows_bios.jpg "Example image of a windows BIOS interface")

The other potential related theme was a fallout-4 style terminal, which may form a potential future direction for development.  

![alt text](https://github.com/SchoolOfCode/w1_website-challenge-gschandan/blob/main/images/fallout_terminal.jpg "Example image of a fallout(game) terminal interface")

### Inspiration
The design idea was inspired by the line-commander exercise from week one, and the goal was to imitate a command line interface to fetch the content.
The theme was chosen for nostalgic reasons, and the font was chosen to inspire a more terminal/command-line like environement.
The idea was for a clean, single page layout which would present an instantly familiar environement, which would be easy and simple to navigate.
A fail-safe for people who are not familiar with CLI's would be the navigation bar which would lead to the same content.

In retrospect, perhaps choosing an error message/failure page may not be the best way to _represent_ the client, which is why, if I were to repeat this, I would probably opt for a fallout style terminal design or just a simple BIOS style design, if I was going to continue on this theme.

### Challenges 
The main challenge was in creating a way for the content to be displayed or hidden on command.
The only way I could find to do this was to use javascript utilising HTML DOM API, to change the CSS style from `display: none;` to `display: flex;`.
I created a form in-line with the path (autofocus to draw attention to it, and show that it was ready for input), and when the contents of the form were changed (or focus changed), the value in the text field would be submitted as a variable to a function I made in JS, to change the CSS style. I couldn't use `hidden` as I did not want there to be a large gap in the page, instead I wanted it to mimic what might be seen in a command line interface, with content being generated.
I suspect there may be a way to do this without javascript, by utilising CSS variables, keyframes and animations; a task for the future I suspect.
Once I had figured out how to show/hide content, then I could utilise the same function in the navbar, to essentially submit the same value it was listening for to load the content.

## Client Feedback
The client was pleased and amused with the design, and made some feedback suggestions which were implemented.
- The skill/proficiency bars were converted to a flex layout to allow stacking and wrapping, for resizing
- The footer was made sticky
- The profile information content was reviewed and further updated

## Directions for Further Work
1. Use CSS transitions to simulate the scrolling of a terminal for the text content, i.e. it will scroll upwards line by line
2. Attempt the changing of content with no JS
3. Add a contact area or perhaps a messgae area
4. Add links (in the navbar or footer) for git-hub and linked in
5. Further BEM implementation in the HTML code
