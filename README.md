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
    
3. [Find the "Kth" max and min element of an array](https://practice.geeksforgeeks.org/problems/kth-smallest-element5635/1) <br />
Code:
```
public static int kthSmallest(int[] arr, int l, int r, int k) 
{ 
    //Your code here
    
    int n = arr.length; 
    PriorityQueue<Integer> pq = new PriorityQueue<Integer>();
    for(int i = 0; i<n; i++){
        pq.add(arr[i]);
    }
    for(int i=0; i<k-1; i++){
        pq.poll();
    }
    return(pq.peek());
}
```

4. [Given an array which consists of only 0, 1 and 2. Sort the array without using any sorting algo](https://practice.geeksforgeeks.org/problems/sort-an-array-of-0s-1s-and-2s4231/1)
Code:
```
public static void sort012(int a[], int n){
    // code here 
    int zero = 0;
    int one = 0;
    int two = 0;
    for(int i=0; i<n; i++){
        switch(a[i]){
            case 0:
                zero++;
                break;
            case 1:
                one++;
                break;
            case 2:
                two++;
                break;
        }
        }
    int i=0;
    while(zero>0){
        a[i++]=0;
        zero--;
    }
    while(one>0){
        a[i++]=1;
        one--;
    }
    while(two>0){
        a[i++]=2;
        two--;
    }
}
```

5. [Move all the negative elements to one side of the array](https://www.geeksforgeeks.org/move-negative-numbers-beginning-positive-end-constant-extra-space/) <br />
Code:
```
import java.io.*;
import java.util.*;

public class GFG {
	public static void main (String[] args) {
		Scanner sc=new Scanner(System.in);
		int a[] = new int[100];
		int n = sc.nextInt();
		for(int i=0; i<n; i++){
		    a[i] = sc.nextInt();
		}
		GFG g = new GFG();
		g.partition(a, n);
	}
	public void partition(int a[], int n){
        int j = 0, temp;
        for(int i =0; i<n; i++){
            if(a[i]<0){
                if(i!=j){
                    temp = a[i];
                    a[i] = a[j];
                    a[j] = temp;
                }
                j++;
            }
        }
        for(int i = 0; i<n; i++){
            System.out.print(a[i]+" ");
        }
}
}
```

6. 