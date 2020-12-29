# Data Structures and Algorithms
This repository contains continually updated Data Structures and Algorithms questions and solutions solved by me, [Koushik Joshi](https://www.linkedin.com/in/koushik-joshi-b60b401b/). <br />
The question set was created by [Love Babbar](https://www.youtube.com/channel/UCQHLxxBFrbfdrk1jF0moTpw) and I wholeheartedly thank him this.

# Problems (including categories and code)
## Language of code:
Java
### Arrays:
1. [Reverse an array](https://www.geeksforgeeks.org/write-a-program-to-reverse-an-array-or-string/) <br />
Code:
```
/* Function to reverse arr[] from 
    start to end*/
    static void rvereseArray(int arr[],
                    int start, int end)
    {
        int temp;
          
        while (start < end)
        {
            temp = arr[start]; 
            arr[start] = arr[end];
            arr[end] = temp;
            start++;
            end--;
        } 
    }     
      
    /* Utility that prints out an
    array on a line */
    static void printArray(int arr[], 
                            int size)
    {
        for (int i = 0; i < size; i++)
             System.out.print(arr[i] + " ");
          
         System.out.println();
    } 
 
    // Driver code
    public static void main(String args[]) {
         
        int arr[] = {1, 2, 3, 4, 5, 6};
        printArray(arr, 6);
        rvereseArray(arr, 0, 5);
        System.out.print("Reversed array is \n");
        printArray(arr, 6); 
        
    } 
```
    
    
2. [Find the maximum and minimum element in an array](https://www.geeksforgeeks.org/maximum-and-minimum-in-an-array/) <br />
Code:

```
public class GetMaxMin{
/* Class Pair is used to return two values from getMinMax() */
    static class Pair {
 
        int min;
        int max;
    }
 
    static Pair getMinMax(int arr[], int n) {
        Pair minmax = new  Pair();
        int i;
 
        /*If there is only one element then return it as min and max both*/
        if (n == 1) {
            minmax.max = arr[0];
            minmax.min = arr[0];
            return minmax;
        }
 
        /* If there are more than one elements, then initialize min 
    and max*/
        if (arr[0] > arr[1]) {
            minmax.max = arr[0];
            minmax.min = arr[1];
        } else {
            minmax.max = arr[1];
            minmax.min = arr[0];
        }
 
        for (i = 2; i < n; i++) {
            if (arr[i] > minmax.max) {
                minmax.max = arr[i];
            } else if (arr[i] < minmax.min) {
                minmax.min = arr[i];
            }
        }
 
        return minmax;
    }
 
    /* Driver program to test above function */
    public static void main(String args[]) {
        int arr[] = {1000, 11, 445, 1, 330, 3000};
        int arr_size = 6;
        Pair minmax = getMinMax(arr, arr_size);
        System.out.printf("\nMinimum element is %d", minmax.min);
        System.out.printf("\nMaximum element is %d", minmax.max);
 
    }
 
}
```
    
3. 