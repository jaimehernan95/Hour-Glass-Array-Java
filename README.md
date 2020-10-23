# HourGlass Array 

## 2D Arrays
Also known as multidimensional arrays, they are very similar to the regular 1D Array data structure we've already discussed.

Consider the following code:

```
int rowSize = 2;
int colSize = 4;
int[][] myArray = new int[rowSize][colSize];
```

this creates a 2  x 4   matrix where each element i, j , can be graphically represented as follows:

(0, 0) (0, 1) (0, 2) (0, 3) 
(1, 0) (1, 1) (1, 2) (1, 3) 

You may find it helpful to think of these  elements in terms of real-world structures such as the cells in a spreadsheet table.

To fill the array's cells with values, you can use a nested loop. The outer loop represents the matrix's rows and uses i  as its variable, and the inner loop represents the matrix's columns and uses  j as its variable. 

The code below assigns the value of  count to each element in the 2D array we declared previously:

```
int count = 0;

for(int i = 0; i < rowSize; i++) {

    for(int j = 0; j < colSize; j++, count++) {
        myArray[i][j] = count;
    }
}
```
If we print the contents of each row:

```
for(int i = 0; i < rowSize; i++) {

    // print the row of space-separated values
    for(int j = 0; j < colSize; j++) {
        System.out.print(myArray[i][j] + " ");
    }
    // end of row is reached, print newline
    System.out.println();
}
```

we'll see the following output:

0 1 2 3 
4 5 6 7 

#### > source:  https://www.hackerrank.com/challenges/30-2d-arrays/tutorial

## Task

<img width="964" alt="Explanation" src="https://github.com/jaimehernan95/hourGlass-Array-Java/blob/master/images/hourglass.png">

<img width="964" alt="Explanation" src="https://github.com/jaimehernan95/hourGlass-Array-Java/blob/master/images/hourglass1.jpg">

## Array hour glass Explanation

<img width="964" alt="Explanation" src="https://github.com/jaimehernan95/hourGlass-Array-Java/blob/master/images/hourglassexplanation.png">

### Solution

<img width="964" alt="Solution" src="https://github.com/jaimehernan95/hourGlass-Array-Java/blob/master/images/result.png">


```
import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.regex.*;

public class Solution {



    private static final Scanner scanner = new Scanner(System.in);

    public static void main(String[] args) {
        int[][] arr = new int[6][6];

        for (int i = 0; i < 6; i++) {
            String[] arrRowItems = scanner.nextLine().split(" ");
            scanner.skip("(\r\n|[\n\r\u2028\u2029\u0085])?");

            for (int j = 0; j < 6; j++) {
                int arrItem = Integer.parseInt(arrRowItems[j]);
                arr[i][j] = arrItem;
            }
        }

        scanner.close();
    }
}

```
