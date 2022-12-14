# **Lab Report 3**

## **Researching Commands**
### `grep -w`
This command is used to limit the search to only find full words within the file or directory. Substrings of words are left out of the search. This command is useful if a user wants to search only for exact mentions of the term they are searching for.

Example 1

In this example, the string "urgently" is being searched for in all of the files within the 911report directory. It outputs the names of each file and the lines in these files that contain the full string.
```
$ grep -w urgently technical/911report/*

technical/911report/chapter-13.4.txt:                underlining of the word urgently in original). Clarke's staff called on other
technical/911report/chapter-6.txt:                paper." We urgently need . . . a Principals level review on the al Qida network,"
technical/911report/chapter-9.txt:                urgently had they known of the South Tower's complete collapse. Other firefighters
technical/911report/chapter-9.txt:                leave the complex urgently but calmly. It is impossible to measure how many more
```

Example 2

In this example, the string "cardiac" is searched for in the cc2160.txt file. All lines which contain the full string are printed in the output.
```
$ grep -w cardiac technical/biomed/cc2160.txt

drug-induced long QT interval and cardiac arrhythmias. In a
drugs that prolong cardiac repolarization [ 9 16 ] .
repolarization (e.g. sex-related differences in cardiac
block cardiac potassium channels, especially the rapid
monitoring is needed to detect critical cardiac arrhythmias
focusing on the detection of critical cardiac arrhythmias
prolongation on the occurrence of critical cardiac
to detect critical cardiac arrhythmias as soon as possible,
```

Example 3

In this example, the string "million" is being searched for within the BusinessWire.txt file. All lines which contain the word million are included in the output.
```
$ grep -w million technical/government/Media/BusinessWire.txt

million in federal funding and $600,000 in state funding to provide
Current federal funds of nearly $10.7 million from the Legal
Services Corporation (LSC) will drop to $8.7 million for next year,
an estimated 1.2 million in 1990 to an estimated 968,000 in
currently $7.5 million in 2002 to $6.9 million when the Michigan
appropriated $329 million to LSC to distribute to local programs
According to the U.S Census Bureau, 33.6 million persons in the
million in 2000.
poor both rose in 2001, to 11.7 percent and 32.9 million, up
11.3 percent and 31.6 million," states Poverty in the United
```


### `grep -i`
This command is used to search for all matching strings regardless of the case of the given search term. This command is useful because some strings may occur at the beginning of sentences, and if they are capitalized they are normally not included in the output.

Example 1

In this example, the string "communication" is searched for within the og98019.txt file. All lines that include this string are included in the output, regardless of the case and whether it is a substring.
```
$ grep -i communication technical/government/Gen_Account_Office/og98019.txt

Subject: Federal Communications Commission: Foreign
Participation in the U.S. Telecommunications Market
Communications Commission (FCC), entitled "Foreign Participation in
the U.S. Telecommunications Market" (IB Docket No. 97-142; FCC
in the United States telecommunications market in light of the
markets for basic telecommunications services to competition from
Federal Communications Commission is John Anderson, Director of
Records Management Federal Communications Commission
ISSUED BY THE FEDERAL COMMUNICATIONS COMMISSION ENTITLED "FOREIGN
PARTICIPATION IN THE U.S. TELECOMMUNICATIONS MARKET" (IB Docket No.
Communications Act of 1934. 47 U.S.C. ???? 151, 152, 154(i), 201,
```

Example 2

In this example, the string "creat" is searched for within the journal.pbio.0020047.txt file. All lines that include this as a substring or full string, regardless of case, are included in the output.
```
$ grep -i creat technical/plos/journal.pbio.0020047.txt

Creative human beings are the torch-bearers of civilization. How does their creativity
create the richest literary treasure in the English language. We wonder how Michelangelo???a
influences shaped their brains to create???and to create these very specific wondrous things?
The Midnight Disease: The Drive to Write, Writer's Block, and the Creative
knowledge???the workings of the brain and the nature of creativity. Its author, a neurologist
many thoughtful people for more than two millennia. What is the nature of creativity? What
is the difference between skill and creativity? What is the relation between mental illness
and creativity? Is creativity inhibited when mental illnesses are treated? What is the
Are these problems always pathological, or do they sometimes enhance creativity? Does that
that affect the brain enhance creativity?
about the nature of creativity, its origins in the mind/brain and in the human genome, and
```

Example 3

In this example, "camp" is searched for within the 1471-2105-3-38.txt file. Although the strings appear as "cAMP" in the file, they are included in output because case is ignored.
```
$ grep -i camp technical/biomed/1471-2105-3-38.txt

monophosphate (cAMP) oscillations observed in fields of
the spontaneous oscillations in cAMP observed during the
5 = [Internal cAMP], 
6 = [External cAMP] and 
Fig. 5. The activity of internal cAMP ( 
variation of each parameter. We use internal cAMP in the
oscillatory behaviour in cAMP signalling observed in the
```


### `grep -c`
This command is used to output the count of how many times the search term is found in the given file or directory. This command is useful if the user is interested in determining how many times a string appears in a file or directory, rather than what lines they appear in.

Example 1

In this example, the string "million" is searched within the Redacted_Study.txt file and the number of occurrences within the file is outputted.
```
$ grep -c million technical/government/Post_Rate_Comm/Redacted_Study.txt

30
```

Example 2

In this example, the term "September" is searched for within the 911report directory. All the file names and the counts of string appearances in each file are included in the output.
```
$ grep -c September technical/911report/*

technical/911report/chapter-1.txt:7
technical/911report/chapter-10.txt:29
technical/911report/chapter-11.txt:5
technical/911report/chapter-12.txt:4
technical/911report/chapter-13.1.txt:0
technical/911report/chapter-13.2.txt:71
technical/911report/chapter-13.3.txt:12
technical/911report/chapter-13.4.txt:37
technical/911report/chapter-13.5.txt:71
technical/911report/chapter-2.txt:1
technical/911report/chapter-3.txt:15
technical/911report/chapter-5.txt:5
technical/911report/chapter-6.txt:14
technical/911report/chapter-7.txt:35
technical/911report/chapter-8.txt:17
technical/911report/chapter-9.txt:26
technical/911report/preface.txt:4
```

Example 3

In this example, the "disease" string is searched for within two files in the plos directory. The names of those two files and the number of occurrences are included in the output.
```
$ grep -c disease technical/plos/pmed.0020148.txt technical/plos/pmed.0020149.txt

technical/plos/pmed.0020148.txt:5
technical/plos/pmed.0020149.txt:1
```