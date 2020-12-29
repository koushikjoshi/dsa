# Data Structures and Algorithms
This repository contains continually updated Data Structures and Algorithms questions and solutions solved by me, [Koushik Joshi](https://www.linkedin.com/in/koushik-joshi-b60b401b/).

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
    
    
2. 
    
