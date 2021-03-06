## runSuite
Contributer: Ding Zhan Chia

## Description
It is a Bash script for program testing. As to fix bugs and refine code, it will be very often to rerun old tests, to check that existing bugs have been fixed, and to ensure that no new bugs have been introduced. 

## How to use it

The command is as followed: 
`./runSuite suite-file program`

The argument suite-file is the name of a file containing a list of filename stems (more details below), and the argument program is the name of the program to be run.

The **suite-file** contains a list of stems, from which we construct the names of les containing the input and expected output of each test. Stems will not contain spaces. For example, suppose our suite le is called suite.txt and contains the following entries:

```
test1
test2
test3
...
```

The test will use the file **test1.in** to hold its input, and **test2.out** to store its expected output. It will do the same jobs for the tests listed in suite-file.  

The sample run of runSuite is as follows:
`./runSuite suite.txt ./myprogram`

## Output
If the output of a given test case differs from the expected output, print the following to
standard output (assuming test test2 failed):
```
Test failed: test2
Input:
(contents of test2.in)
Expected:
(contents of test2.out)
Actual:
(contents of the actual program output)
```
with the (contents ...) lines replaced with actual file contents, as described.


