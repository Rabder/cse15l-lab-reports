# Lab 2 Report

## 1. StringServer
Code for `StringServer.java` <br />
![Code for StringServer.java](stringserver_code.png) <br />

- Output for `add-message?s=How are you doing today?`
![How are you doing today?](stringserver_output1.png) 
1. For this command, we are calling the `handleRequest` method, which takes an object of type `URI` called `url`. In this case, `url` holds `http://localhost:1024/add-message?s=How%20are%20you%20doing%20today?`.
2. We initialize a `String` called `s1` which is initially empty (set to `""`) and an `ArrayList<String>` called `stringlst`.
3. Since we are giving `add-message` as a path, the code in the `else` statement of the method runs. It checks that the path contains `/add-message` and picks the `String` that comes after `s=` by splitting the query component of `url` using `"="` as a delimiter. These strings are stored in a `String` array called `parameters`, which has two elements: `{"s", "How are you doing today?"}`. We add the element of `parameters` at index 1 to `stringlst`.
4. Then, we loop through every element of `stringlst` to concatenate each element to `s1`. Finally, run `String.format(s1)`, which prints the string we added and everything in `stringlst` at that point in a nice format. 


- Output for `add-message?s=I'm feeling fine today`
![I'm feeling fine today](output2.png) <br />
The code that runs for this command is very similar to the one that ran for the previous command. 
Here are the differences:
1. `stringlst` still has our first `String` (`"How are you doing today"?`).
2. `url` holds `http://localhost:1024/add-message?s=I%27m%20feeling%20fine%20today`.
3. `parameters` now stores the following elements: `{"s", "I'm feeling fine today"}`. We still add the element at index 0 to `stringlst`.
4. We concatenate every element of `stringlst` to `s1` and print the newly added string along with any other strings in the list. 


##  2. Bugs
### Test that induces a failure
``` Java
@Test 
  public void firstElementReverse() { 
    int[] input = {1, 2, 3}; 
    assertEquals(input[input.length-1], ArrayExamples.reversed(input)[0]); 
  }
  ```
### Test that doesn't induce a failure
``` Java
  @Test
  public void testReversed() {
    int[] input1 = { };
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
  }
  ```
  ### Symptoms
  ![Bug output](bug_output.png)
  
### Fix
- Before <br />
  ```Java
   // Returns a *new* array with all the elements of the input array in reversed
   // order
   static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
  ```
- After <br />
  ```Java
  // Returns a *new* array with all the elements of the input array in reversed
  // order
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length / 2; i++) {
      newArray[arr.length - i - 1] = arr[i];
    }
    return newArray;
  }
  ```
