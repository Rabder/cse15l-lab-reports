# Lab Report 5

## Student question on EdStem

>> **_What environment are you using (computer, operating system, web browser, terminal/editor, and so on)?_**  <br />
 Computer and operating system: Windows on my personal laptop. Editor: VSCode. Browser: Google Chrome. <br /> <br />
>>**_Detail the symptom you're seeing. Be specific; include both what you're seeing and what you expected to see instead. Screenshots are great, copy-pasted terminal output is also great. Avoid saying “it doesn't work”._**<br />
>>The output of grade.sh shows that every test out of the four tests passed, when three are meant to fail. <br />
>>Expected output:
>>```Out of 4 tests, you failed 3 :
>>1) testAlwaysFail(TestListExamples)
>>2) testAlwaysFail1(TestListExamples)        
>>3) testAlwaysFail2(TestListExamples)        
>>Your score is 25 out of 100
>>>```
Actual output:
![Student screenshot](student_screenshot.png)

>>**_Detail the failure-inducing input and context. That might mean any or all of the command you're running, a test case, command-line arguments, working directory, even the last few commands you ran. Do your best to provide as much context as you can._**
>>I'm running grade.sh with one of the sample student repositories that has bugs in it. TestListExmples.java 
has 4 tests: 3 are meant to always fail and 1 is meant to always pass.
I'm expecting to get a message that prints that the code failed three of the tests and that the code got a score of 25 out of 100 (1/4 tests passed). 



