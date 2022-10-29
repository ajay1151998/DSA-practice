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
