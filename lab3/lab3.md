Hi! It's time for lab 3 so cool. Let's get on with it.

Psst. This one is halloween edition. What's a vampire's favorite fruit? (Answer at the bottom).

Part 1 - Bugs Bzzzzzzz

I chose the bug from the `averageWithoutLowest` from `ArrayExamples.java`. The problem was that if there were multiple instances of the lowest number in the inputted list, they were excluded from the sum, but not from the total number of counted numbers. This resulted in the averages being a lot lower than they should have been. Below, I have a test that exposes the bug.

  ```java
  @Test
  public void testAverageWithoutLowest1() {
    double[] input1 = {4, 4, 5, 6};
    assertEquals(5.0, ArrayExamples.averageWithoutLowest(input1), .005);
  }
```

Since this problem only arises when multiple values are tied for the lowest, a list with all unique values would not result in an error. Below is a faulty test that does not expose the bug.

  ```java
  @Test
  public void testAverageWithoutLowest2() {
    double[] input1 = {3, 4, 5, 6};
    assertEquals(5.0, ArrayExamples.averageWithoutLowest(input1), .005);
  }
```

INSERT SCREENSHOT OF TEST

Below is the problematic code that's failing these easy tests(can't relate). 

  ```java
  static double averageWithoutLowest(double[] arr) {
    if(arr.length < 2) { return 0.0; }
    double lowest = arr[0];
    for(double num: arr) {
      if(num < lowest) { lowest = num; }
    }
    double sum = 0;
    for(double num: arr) {
      if(num != lowest) { sum += num; }
    }
    return sum / (arr.length - 1);
  }
```

Below is the super cool code that aces all the tests, no matter how difficult(manifesting the same for myself).

  ```java
  static double averageWithoutLowest(double[] arr) {
    if(arr.length < 2) { return 0.0; }
    double lowest = arr[0];
    for(double num: arr) {
      if(num < lowest) { lowest = num; }
    }
    double sum = 0;
    for(double num: arr) {
      sum += num; 
    }
    sum -= lowest;
    return sum / (arr.length - 1);
  }
```

The old method would just skip any value that was equal to lowest. The new method would not skip any values, but instead manually remove the value of the lowest from the sum a total of one time. Ok now we're done with bugs, bzzzzzzzzzz. 

Part 2 - Researching Commands

I get to use chatgpt on this part, so it's my favorite out of the two. I did use chatgpt for my research regarding each of the commands in this section and I have cited the inputs and outputs used at the bottom of this page. 

I feel like grep seems like a really useful command, so we are going to explore that for today. Let's go straight into it.

1. `-i`

 ```
  $ grep -i "why" technical/911report/chapter-7.txt

  Why Hazmi and Mihdhar came to California, we do not know for certain. Khalid Sheikh
                mid-July conversation, he denies knowing exactly why he received this
                credible evidence explaining why, on this occasion and others, the operatives flew
                after the 9/11 attacks, "I knew they were going to do something, that is why I got
  ```  

Here, all the lines containing "why" were returned including the line that included "Why" rather than "why". This is useful when we are looking for certain words or phrases, but do not care about capitalization. 

  ```
  $ grep -i "EXCEssiVE" technical/government/Alcohol_Problems/Session3-PDF.txt

  Excessive alcohol consumption plays an important role in many of
  and patient plans to address excessive drinking. Prototypic
  for excessive drinkers: the need for caution. Alcohol Alcohol
  excessively. Second, the ED is a fast-paced environment in which
  ```

Again, we see that the inclusion of `-i` allows for case-sensitive searching when using `grep`. This feels like a staple to almost always include when using `grep`.

2.`-v`
      
  ```
  $ grep -v "a" technical/government/Media/Abuse_penalties.txt

  $100 fine.
  fine.
  "In most of the counties surrounding Schuylkill County, the
  counter-productive."
  meetings without some sort of outside supervision."
  these problems.
  be spent include:
  serve PFAs during nonscheduled work hours, ensuring more expedient
  ```
`-v` returns all of the lines without the pattern being searched. In this example, we see that our command returned all of the lines without the letter "a". I feel like there might be fewer uses for `-v`, but there certainly are times when it would be helpful.

  ```
  $ grep -v "e" technical/government/Alcohol_Problems/Session2-PDF.txt

  drinks on an occasion.4
  drinks).
  subgroups.
  protocol.
  1995. NIH Publication No. 95-3769.
  trauma. JAMA 1993;270:51-6.
  intoxication in alcoholics. J Consult Clin Psychol
  1979;47:205-6.
  1992;53:197-202.
  1991;52:33-6.
  1998;46:328-35.
  JAMA. 1984;252: 1905-7.
  1974;131:1121-3.
  1972;129:342-8.
  1971;127:1653-8.
  1975;36:117-26.
  1991;15:155-7.
  With Harmful Alcohol Consumption, I. Addiction 1993;88:349-62.
  (AUDIT). Addiction 1993;88:791-804.
  1989;160:863-70.
  2000;160:1977-89.
  1995;19:628-34.
  Alcohol 1995;56:695-700.
  Psychiatry 1972;129:127-35.
  Alcohol. 1998;33:304-9.
  1996;11:426-30.
  1994;15:303-10.
  1987;35:864-9.
  1999;36:33-9.
  ```
In this example, we see all the lines without the letter "e". I feel like there could be more use cases than I am displaying here, but I do not want the outputs to be too long and all of these text files are very long. (I say that and this output was super long, sorry)

3. `-r`

  ```
  $ grep -r "crazy" technical

  technical/911report/chapter-13.4.txt:                "ambitious, but not crazy."
  technical/911report/chapter-3.txt:                "a wince." Schroen recalled Massoud's response as "You guys are crazy-you haven't
  technical/biomed/1472-6882-1-10.txt:          become temporarily crazy. Based on experiences like
  technical/government/Media/Assuring_Underprivileged.txt:fair to both sides. It sounds crazy, but that's not always how it
  technical/government/Media/Politician_Practices.txt:Georgia governors. I was never crazy about Jimmy Carter while he
  technical/plos/journal.pbio.0020101.txt:        look at you as if you are crazy. They see an idyllic, sentimental movie, with beautiful
  ```
(crazy? I was crazy once)
Above, we see how using `-r` allowed us to search a pattern across an entire directory rather than just one file. This saves a lot of time when having multiple files to search through and seems like another staple when using `grep`.

  ```
  $ grep -r "rubber" technical/plos

  technical/plos/journal.pbio.0030050.txt:        fill human fossil skulls with vulcanised rubber and once it has set, we pull it out of the
  technical/plos/journal.pbio.0030050.txt:        large hole at the base of the skull and the rubber snaps back into the shape of the skull”,
  ```
(a rubber room)
Again we see that `-r` allows to check all of the files in a directory. Looking through directories for key information is a lot easier since it can look through groups of text files rather than searching through them one by one. 

4. `-l`

  ```
  $ grep -rl "           rats." technical

  technical/biomed/1471-2156-2-12.txt
  technical/biomed/1471-2202-2-20.txt
  technical/biomed/1472-6793-2-11.txt
  technical/biomed/1476-511X-1-2.txt
  ```
  (a rubber room with rats)
Funnily enough, I used `-r` in conjunction with `-l` to search the whole directory. `-l` returns the name of the file containing the line that matches the pattern rather than the line itself. This can be useful to see which files contain some key pattern if seeing the pattern is not necessary, which it often is not.

  ```
  $ grep -l "crazy" technical/911report/Chapter-1.txt technical/911report/Chapter-2.txt technical/911report/Chapter-3.txt

  technical/911report/Chapter-3.txt
  ```
(crazy?)
Again, using `-l` returns all the files that match the pattern. If we are not using `-r`, we have to list out each file to check individually, which can be quite annoying. `-l` seems like another staple when using `grep`, but generally to be used with `-r` rather than listing all the files.

And that was 4 different modifiers to `grep`. Wow time flies, huh? Well, this concludes my third lab. As always, sorry for the terrible jokes and I hope you have a great day!

Best,

  Rishi Gupta

Back to the riddle, what's a vampire's favorite fruit?

A necktarine!

  Works Cited(Chatgpt inputs and outputs)

  Input: "Consider the commands less, find, and grep. For each of them, give me 4 interesting command-line options or alternate ways to use the command you chose. 

  Output: "Certainly! Let's delve into some interesting command-line options for less, find, and grep.

1. less:

-N: Displays line numbers at the beginning of each line.
-i: Enables case-insensitive searching. When this flag is used, searches will ignore the case of the characters.
-R: Interprets raw control characters. This option is useful for viewing files with ANSI color codes.
-g: Highlights only the last used search pattern. If you use this option, when you search for multiple patterns in the file, only the most recent match will be highlighted.
2. find:

-iname: This option allows case-insensitive searching for filenames. For example, find . -iname "example.txt" will match example.txt, Example.txt, EXAMPLE.TXT, etc.
-type: Filters the search based on the type of the file. For instance, -type f matches only regular files, while -type d matches only directories.
-exec: Allows you to execute a specific command on each file found. For example, to delete all .bak files, you could use: find . -name "*.bak" -exec rm {} \;.
-mtime: Searches for files based on their modification time. For example, find . -mtime -7 would find files modified within the last 7 days.
3. grep:

-i: Ignores the case of characters when searching. For example, grep -i "example" file.txt will match both "example" and "Example".
-v: Inverts the match. This means it will display the lines that do not match the given pattern.
-r or -R: Recursively searches directories. Given a pattern and a directory, grep -r "pattern" directory/ will search for the pattern in all files in the directory and its sub-directories.
-l: Only displays the names of the files that contain the given pattern, not the matching lines themselves.
These are just a handful of options available for each command. Each command has its own man page (e.g., man grep) which provides an in-depth look at all available options and their uses."

