## Exercise_4-UiPath-Flow-sequence-or-Flow-chart-using-Repeat-While-and-Do-While-loops

## Aim:

To demonstrate the use of loops in a Flow Sequence or Flow Chart using Repeat, While, and Do-While activities in UiPath.

## Equipment Required:

UiPath Studio (installed on a compatible system).<br>
Computer with:<br>
Minimum 4 GB RAM.<br>
Minimum 2.0 GHz CPU.<br>
Windows operating system.<br>
.NET Framework 4.6.1 or later.

## Procedure:

### Create a New Project:

Open UiPath Studio and create a new project by selecting Process under the New Project tab.<br>
Name the process (e.g., Looping Demo) and click Create.

### Add a Flowchart or Flow Sequence:

In the Activities panel, search for either Flowchart or Sequence and drag it into the main workflow area.<br>
For this demonstration, you can use either structure. However, a Flowchart allows more visual branching, while a Sequence focuses on linear execution.

### Initialize Variables:

Add variables to control the loop. For example:<br>
counter (of type Int32): This will serve as the iteration counter.<br>
maxCount (of type Int32): The maximum number of times the loop should execute.

### Add a Repeat Loop:

In a Flowchart:<br>

Drag a Flow Decision activity and configure a condition such as counter < maxCount.<br>
In the True branch, add a Sequence that contains the looped actions.<br>
Drag a Assign activity into the True branch to increment the counter variable (counter = counter + 1).<br>
Link it back to the Flow Decision for repeated execution.<br>
<br>
In a Flow Sequence:<br>

Search for the Repeat activity in the Activities panel.<br>
Set the Condition as counter < maxCount.<br>
Inside the loop, add actions (e.g., increment counter and display the value using Write Line).

### Add a While Loop:

Drag the While activity from the Activities panel into the workflow.<br>
Set the Condition as counter < maxCount.<br>
Inside the Do section, increment the counter and perform any actions such as logging or output.<br>
Example: Use Write Line to display the current value of counter.

### Add a Do-While Loop:

Drag the Do While activity from the Activities panel.<br>
Set the Condition to check if the counter is less than maxCount (counter < maxCount).<br>
Inside the Body section, add an action such as incrementing counter and using Write Line to output the value.<br>

## Example Workflow:

### Initialize Variables:

counter = 0<br>
maxCount = 5

### Repeat Loop:

Condition: counter < maxCount<br>
Inside the loop:<br>
Increment counter: counter = counter + 1<br>
Write Line: "Repeat Loop, Counter: " + counter.ToString

### While Loop:

Condition: counter < maxCount<br>
Inside the loop:<br>
Increment counter: counter = counter + 1<br>
Write Line: "While Loop, Counter: " + counter.ToString

### Do-While Loop:

Inside the loop:<br>
Increment counter: counter = counter + 1<br>
Write Line: "Do-While Loop, Counter: " + counter.ToString<br>
Condition: counter < maxCount

## UiPath WorkFlow:

![alt text](<img/Screenshot 2024-09-30 223845.png>)
![alt text](<img/Screenshot 2024-09-30 223902.png>)
![alt text](<img/Screenshot 2024-09-30 223942.png>)
![alt text](<img/Screenshot 2024-09-30 224113.png>)
![alt text](<img/Screenshot 2024-09-30 224214.png>)
![alt text](<img/Screenshot 2024-09-30 224339.png>)
![alt text](<img/Screenshot 2024-09-30 224411.png>)
![alt text](<img/Screenshot 2024-09-30 224530.png>)
![alt text](<img/Screenshot 2024-09-30 224624.png>)
![alt text](<img/Screenshot 2024-09-30 224638.png>)

## Result:

After running the workflow, the loops will execute as follows:<br>

The Repeat loop executes the block of code until the condition becomes False.<br>
The While loop checks the condition before each iteration and only runs if the condition is True.<br>
The Do-While loop always executes at least once before checking the condition.<br>
