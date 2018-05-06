# 02 Scope Exercise
### Joshua Fredrickson


Questions:

1. When this code is run in Node, e.g. node index.js, what are the two stages of execution for this file called, and which order do they happen in?
 - Node executes code with the first stage of compilation (via the compiler) and completes with the execution stage (via the engine).

2. Write an explanation, using as much space as you need, relating to how the first stage of execution for this file operates.
 - the compiler grabs all of the variables (NOT the values of those variables!) and determines the scope of those variables.
 In this code example here are the following variables and scope that are grabbed.
  - Global Scope:  
  foo on line 3
  function bar on line 5
  
  - Scoped within the function bar: 
  foo on line 6
  function baz on line 8
  
  - Scoped within the function baz:
  foo on line 10
  bam on line 11                        
 

3. Write an explanation, using as much space as you need, relating to how the second stage of execution for this file operates.
For example, identify the high level steps in a line by line overview and then define what each of those steps are accomplishing.
starting from line 1
foo = 'bar'

function bar is being preformed on line 16.  foo is now = to baz.  function baz is being performed with foo as a parameter. foo is now equal to bam and bam is now equal to yay.

foo is being called on line 17 and foo is now equal to bar due to global scope.
bam in line 18 is undefined due to it being inside the function bar
baz in line 19 is undefined due to it being inside the function bar



4. During the second stage of execution how many scopes have been registered by the engine?
The execution stage connects values to the variables from the compiler with the engine and performs the operations.
Which segments of the code do they belong to?
Please identify any variables/refs and which scope each belongs to?

  - Global Scope:  
  foo on line 3
  function bar on line 5
  
  - Scoped within the function bar: 
  foo on line 6
  function baz on line 8
  
  - Scoped within the function baz:
  foo on line 10
  bam on line 11 
  
  
starting from line 1
foo = 'bar'

function bar is being preformed on line 16.  foo is now = to baz.  function baz is being performed with foo as a parameter. foo is now equal to bam and bam is now equal to yay.

foo is being called on line 17 and foo is now equal to bar due to global scope.  
bam in line 18 is undefined due to it being inside the function bar
baz in line 19 is undefined due to it being inside the function bar


5. When line 13 invokes the baz function, which foo will be assigned a value of bam? More specifically, bam will be assigned to the foo in ??? scope. Give a brief description in your own words to support your conclusion.
bam is not defined due to scope of "use strict".

6. Which scope, if any, will the variable bam on line 11 be registered to when the first stage of execution occurs on this file? Provide a brief description in your own words to support your conclusion.
Bam is not defined due to the reference Error.

7. For each line, 16 through 19, what is the return value for each?
function bar is being preformed on line 16.  foo is now = to baz.  function baz is being performed with foo as a parameter. foo is now equal to bam and bam is now equal to yay.
foo is being called on line 17 and foo is now equal to bar due to global scope.  
bam in line 18 is undefined due to it being inside the function bar
baz in line 19 is undefined due to it being inside the function bar


