# state-drills

Assignment
Your assignment for this checkpoint is to complete three drills. Make a new folder in your react-playground project, ./src/state-drills/ to put the component files for these drills in.

Requirements
Drill 1 - Hello World:
A component that changes its display according to buttons that update state. Utilising event handlers and state.
Make a component called HelloWorld inside the ./src/state-drills/ folder. Update your index.js to use the HelloWorld component to check that it works.
The component should render an outer div element. Inside the div there should be p element containing Hello, world. The word "world" should come from state in a property named who.
The component should also display 3 buttons, one for each: "World", "Friend" and "React".
When a user clicks on one of the 3 buttons, use state and an event handler to update the state property who so that the content in the p element changes.
If the user clicks the "Friend" button, the p displays Hello, friend!.
If the user clicks the "React" button, the p displays Hello, React!.
If the user clicks the "World" button, the p displays Hello, world!.

Drill 2 - Bomb:
A component that uses life-cycles, setInterval and state to alternate between rendering either "tick" or "tock" for a time and then rendering "BOOM!!!!".
Make a component called Bomb inside the ./src/state-drills/ folder. Update your index.js to use the Bomb component to check that it works.
The component should render a div element. Inside the div there should be a p that contains content of either "tick", "tock" or "BOOM!!!!".
The component will have an initial state with a property count of 0.
When the component mounts, register an interval that adds 1 to the count in state every second.
When the component unmounts, clear the interval.
When the count is divisible by 2, display the word "tick".
When the count isn't divisible by 2, display the word "tock".
If the count goes equal to or above 8, display "BOOM!!!!".
When the count goes above or equal to 8, also clear the interval!
Tips:

To check if a number is divisible by 2, you can use the modulo operator.
An interval will repeatedly invoke a callback as often as specified by the milliseconds argument.
You can create an interval by using let interval = setInterval(callback, timeInMs).
You can clear an interval by using clearInterval(interval).
Drill 3 - RouletteGun:

A component that combines state and props. The parent of this component will pass in a prop that the number of which chamber contains a bullet, and the number should be between 1 and 8. When a user clicks on a button, the component will choose a random chamber and pull the trigger! If the chamber with the bullet in is chosen, the component will render BANG!!!!

Make a component called RouletteGun inside the ./src/state-drills/ folder. Update your index.js to use the RouletteGun component to check that it works.
The component should render a div element.
Inside the div, there should be a p that contains the content of either:
spinning the chamber and pulling the trigger! ...
you're safe!
BANG!!!!
Inside the div, there should also be a button that contains Pull the trigger!.
The component will have an initial state with 2 properties, chamber that is initially set to null, and spinningTheChamber that is initially set to false.
The component will accept a prop called bulletInChamber that has a default value of 8.
When the user clicks the button, there should be a click event handler. The following steps should be in the handler:
The state should update spinningTheChamber to be true.
A timeout should be registered for 2 seconds.
Within the timeout, a random number between 1 and 8 should be generated.
Within the timeout, the state should be updated so that the generated random number is the new value for chamber and spinningTheChamber should be false.
The component should render the content of the p element according to the following rules:
If spinningTheChamber is true, render spinning the chamber and pulling the trigger! ....
If the chamber value in state is the same as the bulletInChamber value in props, render BANG!!!!.
Otherwise, render you're safe!!
If the component is to be unmounted, clear the timeout.
Tips:
To generate a random number between 1 and 8 you can use methods on the Math object like so: Math.ceil(Math.random() * 8).
A timeout will invoke a callback once after the time specified by the milliseconds argument.
You can create a timeout by using let timeout = setTimeout(callback, timeInMs).
You can clear a timeout by using clearTimeout(timeout).
