# Befunge Interpreter Prototype

## Resources

- Documentation: https://github.com/catseye/Befunge-93/blob/master/doc/Befunge-93.markdown
- Wikipedia Entry: https://en.wikipedia.org/wiki/Befunge
- Befunge Source Code Tester: http://www.quirkster.com/iano/js/befunge.html

```
v >$>  v <>0v
4>|v?v#?#^?8v
4!8123    9 1
g-4>>>># >>1v
:**v <4>5^v<+
84-p 4^?6^\9:
>^&& 4 >7^%58
v:<< ^+*  <^<
>." si",,,-:v
v"correct!"<!
8>"wol ",,v|<
2|,,,"too"  <
9 >:#,_@#:<`!
\> "hgih "^>^
>#^/#p*#44#4_
```

## Instructions

Write a Befunge-93 interpreter `createBefungeApplication` in JavaScript that will, given an initial string of Befunge source code, return a function that will run the Befunge code every time it is called, with the parameters acting as the program's input.

```
function createBefungeApplication(originalSourceCode){ /* ... */ }

const guessingGameSource = 'v >$>  v <>0v\n4>|v?v#?#^?8v\n4!8123    9 1\ng-4>>>># >>1v\n:**v <4>5^v<+\n84-p 4^?6^\9:\n>^&& 4 >7^%58\nv:<< ^+*  <^<\n>." si",,,-:v\nv"correct!"<!\n8>"wol ",,v|<\n2|,,,"too"  <\n9 >:#,_@#:<`!\n\> "hgih "^>^\n>#^/#p*#44#4_';

const makeGuess = createBefungeApplication(guessingGameSource);

console.log(makeGuess(5)); // 5 is too low
console.log(makeGuess(8)); // 8 is too high
console.log(makeGuess(7)); // 7 is correct!

console.log(makeGuess(7)); // 7 is too high
console.log(makeGuess(3)); // 7 is too high
console.log(makeGuess(1)); // 7 is correct!

//  ... and so on

```
