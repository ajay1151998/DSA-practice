# DSA-practice

## Minimum Swap to sort a array

#### solution 


public class Solution {

    static void Swap(int[] arr,int i,int j){
        int temp=arr[i];
        arr[i]=arr[j];
        arr[j]=temp;
    }

static int minimumSwaps(int[] arr) {

        int count=0;
        int n=arr.length;
        for(int i=0;i<n;i++){
            if(arr[i]!=i+1){
                int j=arr[i]-1;
                Swap(arr,i,j);
                count++;
                i--;
            }
        }
        return count;
    }
}


#Exercise 1: Create a method to find the sum of the cubes of the digits of an n digit number

import java.util.*;

class GFG {
     public static int findCube(int n){
         int temp=n;
         int sum=0;
         while(temp>0){
             int k=temp%10;
             sum+=Math.pow(k,3);
             temp=temp/10;
         }
         return sum;
         
     }
	public static void main (String[] args) {
		Scanner sc=new Scanner(System.in);
		int n=sc.nextInt();
		System.out.println(findCube(n));
	}
}
