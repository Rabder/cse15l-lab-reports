# Lab Report 5

## Student question on EdStem

>> **_What environment are you using (computer, operating system, web browser, terminal/editor, and so on)?_**  <br />
 Computer and operating system: Windows on my personal laptop. Editor: VSCode. Browser: Google Chrome. <br /> <br />
>>**_Detail the symptom you're seeing. Be specific; include both what you're seeing and what you expected to see instead. Screenshots are great, copy-pasted terminal output is also great. Avoid saying “it doesn't work”._**<br />
>>The output of grade.sh shows that every test out of the four tests passed, when three are meant to fail. <br />
>>Expected output: <br />
>>```
>>... some output ...
>>Out of 4 tests, you failed 3 :
>>1) testAlwaysFail(TestListExamples)
>>2) testAlwaysFail1(TestListExamples)        
>>3) testAlwaysFail2(TestListExamples)        
>>Your score is 25 out of 100
>>```
>>Actual output:<br />
>>![Student screenshot](student_screenshot.png)
>>**_Detail the failure-inducing input and context. That might mean any or all of the command you're running, a test case, command-line arguments, working directory, even the last few commands you ran. Do your best to provide as much context as you can._** <br />
>>I'm running grade.sh with one of the sample student repositories that has bugs in it: (https://github.com/ucsd-cse15l-f22/list-methods-corrected). TestListExmples.java 
>>has 4 tests: 3 are meant to always fail and 1 is meant to always pass. My script is meant to extract the number of failing tests and the number of passing tests.
>>I'm expecting to get a message that prints that the code failed three of the tests and that the code got a score of 25 out of 100 (1/4 tests passed). 


## TA Response 
>> Hi there!
>> Based on the screenshot you provided, your issue could be related with how you parse your JUnit tests. 
>> It seems that you are storing the JUnit output in the ```junit.txt``` file. Try opening that file or running ```cat <path of junit.txt>``` to see whether the test results are being stored correctly in the file. 
 
 
## Student follow-up question
>> Ok this is what ```junit.txt``` looks like.
>>![Student follow-up](student_followup.png)
>> I think the issue could be the way I'm checking whether the code failed any test. Instead of 
 
