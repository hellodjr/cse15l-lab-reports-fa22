Command:grep
 
first command option:
=
```
-c
```
 First example
 -
```
(base) jrd@Jiajies-MBP-3 911report % grep -c "chapter" chapter-2.txt 
```
```
2
```
- explaination:

The -c command line options printsa count of the lines that match a pattern inside the quotation mark. Here, it prints out a count of "chapter" inside chapter-2 text file, and it found 2 lines that match with "chapter"

Second example:
-
```
(base) jrd@Jiajies-MBP-3 911report % grep -c "chapter" chapter-2.txt chapter-3.txt chapter-5.txt
```
```
chapter-2.txt:2
chapter-3.txt:6
chapter-5.txt:4
```
- Explanation:
This one does the exact same thing as the first example, the only difference is that it prints a count of the lines for multiple files at once.

Third example:
-
```
(base) jrd@Jiajies-MBP-3 911report % grep -v -c "chapter" chapter-2.txt chapter-13.3.txt
```
```
chapter-2.txt:946
chapter-13.3.txt:1717
```
- Explanation:
This one is slightly different from last two, by adding -v in front of -c command option, it prints out a count of lines that doesn't contain any pattern as "chapter"

Second command option:
=
```
-A
```

first example:
-
```
(base) jrd@Jiajies-MBP-3 911report % grep -A 3 "for interagency" chapter-3.txt
```
```
for interagency consideration before 9/11. As 1999 came to a close, the CIA had a new strategic plan in place for capturing Bin Ladin, but no option was rated as having more than a 15 percent chance of achieving that objective.
```
- Explanation:
-A option is used to print the line after specified N line, here I specify the 3 lines after "for inteagency", it only prints out 3 line after this in chapter-3 text file.

second example:
-
```
base) jrd@Jiajies-MBP-3 911report % grep -A 3 -i "For interagency" chapter-3.txt
```
```
for interagency consideration before 9/11. As 1999 came to a close, the CIA had a new strategic plan in place for capturing Bin Ladin, but no option was rated as having more than a 15 percent chance of achieving that objective.
```
- Explanation: the second example does the exact same thing as last one, however, by using -i commond in between, it will ignore the case for matching.Therefore, it prints out the same lines as last even though the matching pattern is upper case in which doesn't match the text.

Third example:
-
```
(base) jrd@Jiajies-MBP-3 911report % grep -A 1 -i "interagency" chapter-3.txt chapter-5.txt
```
```
chapter-3.txt:                represented the department on the interagency committee concerned with
chapter-3.txt-                counterterrorism. By the end of President Clinton's first term, this official had
--
chapter-3.txt:                was overseen by a high-level interagency committee chaired by the deputy national
chapter-3.txt-                security adviser. But the Reagan administration closed with a major scandal that
--
chapter-3.txt:                the president worked their way through interagency committees usually composed of
chapter-3.txt-                departmental representatives at the assistant secretary level or just below it. The
chapter-3.txt:                NSC staff had senior directors who would sit on these interagency committees, often
chapter-3.txt-                as chair, to facilitate agreement and to represent the wider interests of the
--
chapter-3.txt:                coordinating counterterrorism. Before long, he would chair a midlevel interagency
chapter-3.txt-                committee eventually titled the Counterterrorism Security Group (CSG). We will later
--
chapter-3.txt:                regarding budgets and to "coordinate the development of interagency agreed
chapter-3.txt-                guidelines" for action.
--
chapter-3.txt:                on his issues-a highly unusual step for a White House staffer. His interagency body,
chapter-3.txt-                the CSG, ordinarily reported to the Deputies Committee of subcabinet officials,
--
chapter-3.txt:                counterterrorism efforts, through Richard Clarke and his interagency
chapter-3.txt-                Counterterrorism Security Group (CSG). Spotlighting new concerns about
--
chapter-3.txt:                had elevated accordingly. The CSG, unlike most standing interagency committees, did
chapter-3.txt-                not have to report through the Deputies Committee. Although such a reporting
--
chapter-3.txt:                    family." One result was two NSC-led interagency trips
chapter-3.txt-                to Persian Gulf states in 1999 and 2000. During these trips the NSC, Treasury, and
--
chapter-3.txt:                never turned into an interagency policy paper.
chapter-3.txt-            The same was true for the option of using ground units from the Special Operations
--
chapter-3.txt:                memorandum of this conversation that the call had been approved at an interagency
chapter-3.txt-                meeting and cleared with the CIA.
--
chapter-3.txt:                for interagency consideration before 9/11. As 1999 came to a close, the CIA had a
chapter-3.txt-                new strategic plan in place for capturing Bin Ladin, but no option was rated as
--
chapter-6.txt:                the creation of an NSC-led interagency committee on terrorist financing. On its
chapter-6.txt-                recommendation, the President had designated Bin Ladin and al Qaeda as subject to
--
chapter-6.txt:                picture of Bin Ladin's finances. A U.S. interagency group traveled to Saudi Arabia
chapter-6.txt-                twice, in 1999 and 2000, to get information from the Saudis about their
--
chapter-6.txt:                creating an interagency center to target illegal entry and human traffickers;
chapter-6.txt-                imposing tighter controls on student visas;
--
chapter-6.txt:                groups than to executive branch interagency committees. The changes sought by the
chapter-6.txt-                principals in March 2000 were only beginning to occur before 9/11.
--
chapter-6.txt:            There was no interagency consideration of just what military action might have looked
chapter-6.txt-                like in practice-either the Pentagon's new "phased campaign" concept or a prolonged
--
chapter-6.txt:                policymaking, she felt, that Clarke's interagency committee-like all others-report
chapter-6.txt-                to the principals through the deputies.
```
- Explanation:
The third example does the same thing as second example, however, it prints three lines after the mathcing pattern "interagency" for chapter-3 and chapter-6 files.

Third command line option:
=
```
-win
```

First example:
-
```
(base) jrd@Jiajies-MBP-3 911report % grep  -win "The law requires the NSA" chapter-3.txt 
```
```
728:            The law requires the NSA to not deliberately collect data on U.S. citizens or on
```
- Explanation:
-win command option prints the number of line that contains the matching pattern in the text. Here, "The law requires the NSA" shows up in line 728 for the chapter 3 file.

Second example:
-
```
(base) jrd@Jiajies-MBP-3 911report % grep  -win -B 4 "The law requires the NSA" chapter-3.txt
```
```
724-                economies of scale. Modern adversaries are skilled users of communications
725-                technologies. The NSA's challenges, and its opportunities, increased exponentially
726-                in "volume, variety, and velocity."
727-            
728:            The law requires the NSA to not deliberately collect data on U.S. citizens or on
```
- Explanation:
With the help of -B command option, it prints 4 lines of leading context before the matching lines from the example 1.

Third example:
-
```
(base) jrd@Jiajies-MBP-3 911report % grep  -win "The law requires" ./*
```
```
./chapter-3.txt:728:            The law requires the NSA to not deliberately collect data on U.S. citizens or on
```
- Explanation:
For this example, it prints the exact same thing as first exaple,however, it prints out the directory followed by matching line for "The law requires".
