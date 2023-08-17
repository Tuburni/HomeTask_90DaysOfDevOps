Question 1: What is Shell Scripting for DevOps?
Shell scripting is like telling your computer what to do by giving it a list of things to follow. It's a bit like making a recipe for a robot. In DevOps, which is like computer teamwork, we use shell scripting to make our computers do jobs automatically, like setting up websites or managing big groups of computers.

Question 2: What is #!/bin/bash? Can we write #!/bin/sh as well?
Imagine you have a magic book that can talk to the computer. When it sees #!/bin/bash at the start, it knows to talk to the computer using a special language called "bash." But if it's #!/bin/sh, it talks in a different way. So, yes, you can use either of them, but they might speak to the computer a bit differently.

Question 3: Write a Shell Script which prints "I will complete #90DaysOfDevOps challenge"
Sure, here's how the magic recipe might look in the computer language:
>  <sub> _copy and past this comand to terminal_ </sub>
```bash
#!/bin/bash
echo "I will complete #90DaysOfDevOps challenge"
```

Question 4: Write a Shell Script to take user input, input from arguments, and print the variables.
Okay, here's the recipe for that:
>  <sub> _copy and past this comand to terminal_ </sub>
```bash
#!/bin/bash
echo "Tell me something:"
read userInput

echo "You said: $userInput"

echo "Argument 1: $1"
echo "Argument 2: $2"
```

Question 5: Write an Example of If-Else in Shell Scripting by comparing two numbers
Imagine you're deciding what game to play based on how many friends you have. Here's how you might do it with the computer:
>  <sub> _copy and past this comand to terminal_ </sub>
```bash
#!/bin/bash
numFriends=5
if [ $numFriends - > 3 ]; then
    echo "Let's play a big group game!"
else
    echo "Let's play a small group game."
fi

```