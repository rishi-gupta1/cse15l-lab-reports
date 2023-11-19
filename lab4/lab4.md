oh my gosh I'm so excited, it's time for lab 4! Hold on to your seat because this is going to be a super exhilerating(not really) lab report for the both of us!

But before all that, we of course have to do the joke of the day. Well, today it's more of a sad insight into my life rather than a joke.

I was doing my ece 45 homework in an elevator today. It was wrong on so many levels...

Ok now time for the super fun lab that's not at all annoying to write the report on.


For the lab report this week, reproduce the task from above on your own. For each numbered step starting right after the timer (so steps 4-9), take a screenshot, and write down exactly which keys you pressed to get to that step. For special characters like <enter> or <tab>, write them in angle brackets with code formatting. Then, summarize the commands you ran and what the effect of those keypresses were.

For example, when you run the tests, you might want to use the up arrow or Ctrl-R to access your bash history rather than typing in the full command with classpath, etc. You might say something like this accompanying the screenshot for running the tests:

Keys pressed: <up><up><up><up><enter>, <up><up><up><up><enter> The javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java command was 4 up in the search history, so I used up arrow to access it. Then the java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ... command was 4 up in the history, so I accessed and ran it in the same way.

4. [INSERT SCREENSHOT]

Keys pressed: `<up><enter>`. The command `$ ssh cs15lfa23qk@ieng6.ucsd.edu` was one up in the command history, so I used an up arrow to access it. This resulted in me being logged into my ieng account.

5. [INSERT SCREENSHOT]

Keys pressed: `git clone <control + c>`. I had copied the ssh clone link from my github repository, so I just had to paste it in rather than type it out. This resulted in the repository being cloned.

6. [INSERT SCREENSHOT]

Keys pressed: `ls`,  `cd lab7`,  `ls`,  `bash test.sh`. Here, there were not really any shortcuts that I took. Technically, I could have looked at the repository to see the path and immediately ran the bash file in one line if I really wanted, but I think what I did was fine. By running `$ ls`, I saw what was in the active directory. Then by runnning `$ cd lab7`, I changed my active directory to `lab7` since that contained the bash file that would run the tests. 

7. [INSERT SCREENSHOT]

Keys pressed: `vim ListExamples.java`, `i`,  `<down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><right><right><right><right><right><right><right><right><right><right><right><right><backspace>2<esc>`, `:wq`. By using `vim`, I was able to access the code through terminal. The command `i` allowed me to edit the code. All of the downs and rights were to move my cursor to where the bug was. Then, the sequence of deleting and adding a 2 was fixing the bug. Escaping ended my editing of the code. Finally, using the command `:wq` allowed me to save and exit the `vim` view. 

8. [INSERT SCREENSHOT]

Keys pressed: `<up><up><enter>`. I had already run the bash file that runs the tests earlier, so it was in my command history. Thus, the command `$ bash test.sh` autopopulated for me. Running the bash file ran the tests again, which now both passed.

9. [INSERT SCREENSHOT]

Keys pressed: `git stage ListExamples.java`, `git commit -m fix`, `git push`, `<my password>`. First, I staged `ListExamples.java` to prepare it for the commit. Then, I made the commit with the message "fix". Then, I pushed my commit onto github. It asked for my password, so I entered my password.

Wowee that was a roller coaster. So fun. I really enjoyed doing this. Thank you for grading this, goodbye.

Best,
  Rishi Gupta
