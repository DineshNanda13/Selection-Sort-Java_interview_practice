# Selection-Sort-Java_interview_practice
In selection sort algorithm, we search for the lowest element and arrange it to the proper location. We swap the current element with the next lowest number.

package com.selectionSort;

/**
 *
 * @author Dinesh Nanda
 */

public class SelectionSort {

    public static void main(String[] args) {
        
        int arr[] = {9,14,3,2,43,11,58,22};
       
        int iteration_number = 0;
        
        for(int i = 0; i < arr.length; i++){
            int lowest = arr[i];
            for(int j = i; j < arr.length - 1; j++){
                
                if(lowest > arr[j+1]){
                    
                    lowest = arr[j+1];
                    iteration_number = j+1;
                }
            }
            int temp = arr[i];
            arr[i] = lowest;
            arr[iteration_number] = temp;
        }
        for(int i = 0; i < arr.length; i++){
            System.out.print(arr[i]+" ");
        }
    }
}
