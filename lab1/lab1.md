First, let us take a look at the change directory command.

Psst. Why are wine experts called sommeliers? Because they suh-mell-uh-the-air

1. ![Image](screenshots/Lab1A.PNG)  

   Here, we used the `cd` command with no arguments. This resulted in us leaving the directory. The working directory changed from `/home/lecture1` to `/home`. 
3. ![Image](screenshots/Lab1B.PNG)  
  Here we used the `cd` command with a path to a directory. This resulted in us entering that directory. The working directory changed from `/home` to `/home/lecture1`.
4. ![Image](screenshots/Lab1C.PNG)  
   Here, we used the `cd` command with a path to file. This was not very smart of us since the `cd` feels about paths to files the same way i feel about midterms(not good). Thus, it resulted in an error. The working directory was `/home/lecture1` when running this command, which did not change the working directory.

Now let's move onto the `ls` command(I always read this as 1s).

1. ![Image](screenshots/Lab1D.PNG)  
  I was using "Here" too much, so in this image we have `ls` with no argument. This resulted in the terminal returning a list of available directories. The working directory was `/home` when the command was run.
2. ![Image](screenshots/Lab1E.PNG)  
   In this image, we used the `ls` command with an argument passed. The argument passed in this instance was a directory, so the ls command returned a list of contents in the directory. The working directory was `/home` when the command was run.
3. ![Image](screenshots/Lab1F.PNG)  
   In this image, we used the `ls` command with the argument passed being a file. Consquently, the ls command just returned the file name of the file I referenced since that is the only file in the file. The working directory was `/home/lecture1` when run.

Finally, let's move onto the `cat` command - not the fun cat.

1. ![Image](screenshots/Lab1G.PNG)  
   We gotta change up the starting phrase one more time, so let's go with As shown above. As shown above, I used the `cat` statement with no arguments passed. This then prompted me to enter any string I wanted and it would return the same string. The working directory was `/home` when run.
2. ![Image](screenshots/Lab1H.PNG)  
   As shown above, I tried running the `cat` command with a reference to a directory. It told me that the directory I gave it was indeed a directory. Riveting. The working directory was `/home` when run.
3. ![Image](screenshots/Lab1I.PNG)  
   As shown above, I ran the `cat` command with a reference to a file. It returned the code in the file. This was actually riveting(no it wasn't). The working directory was `/home/lecture1` when run.

Thank you for grading my lab a second time. Yours truly,
    Rishi Gupta
