# Arrays
//Chack frequency of array to chack who`s number come odd time
like[2,2,3,4,4] there ans is 3   */

import java.util.Arrays;
public class ChackFrequency {
    public static void main(String[] args) {
        int[] arr = {4,5,5,5,5, 6, 7, 7};
        Arrays.sort(arr);
        int n = arr.length;
        int i = 1;
        while(i<n){
            int cnt = 1;
            while (i<n&&arr[i - 1] == arr[i]) {
                cnt++;
                i++;
            }
            if (cnt %2 == 1) {
                System.out.println(arr[i - 1]);
            }
            i++;
        }
    }
}
//REMOVE DUPLICATE FROM ARRAY AND RETURN NEW ARRAY

import java.util.Scanner;

public class Duplicate {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n =sc.nextInt();
        int[] arr = new int[n];
        boolean [] keep = new boolean[n];
        int count=0;
        for(int i=0;i<n;i++) {
            arr[i] = sc.nextInt();
        }
        for(int i=0;i<n;i++) {
            keep[i] = true;
            for(int j=i+1;j<n;j++) {
                if(arr[i]==arr[j]) {
                    keep[i] = false;
                    break;
                }
            }
            if(keep[i]) {
                count++;
            }
        }
        System.out.println(count);
            for (int j = 0; j < arr.length; j++) {
                if (keep[j]) {
                    System.out.print(arr[j] + " ");
                }
            }
    }
}

//ADD EXTRA ELEMENT IN ARRAY
/*     4
       3
       1 2 3
       [1, 2, 5, 3]   */

       import java.util.Arrays;
import java.util.Scanner;

public class Patterns {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int cap = sc.nextInt();
                int n = sc.nextInt();
                int[] arr = new int[cap];
                for (int i = 0; i < n; i++) {
                    arr[i] = sc.nextInt();
                }
                for (int i = n; i>=2; i--) {
                    arr[i] = arr[i-1];
                }
                arr[2]=5;

                System.out.println( Arrays.toString(arr));

            }
        }

    //CREATE A CAP ARRAY OR DELET A ELEMENT AND THEN SHIFT THR REST OF THE LEFT.

    import java.util.Arrays;
import java.util.Scanner;
public class Shifting {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int cap = sc.nextInt();
        int n = sc.nextInt();
        int[] arr = new int[cap];
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }
        int res = 0;
        for (int i = 0; i < n; i++) {
            if (arr[i] == 4) {
                res = i;
                for (int j = res; j < n; j++) {
                    arr[j] = arr[j + 1];

                }
            }
        }
            System.out.println(Arrays.toString(arr));
    }
}

//CREAT A CAP ARRAY OR INSERT SOMTING DIFFERENT IN IT.

import java.util.Arrays;
import java.util.Scanner;
public class InsertValue {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int cap = sc.nextInt();
        int n = sc.nextInt();
        int[] arr = new int[cap];
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }
       arr[2]=4;
        arr[3]=5;
            System.out.println(Arrays.toString(arr));
    }
}
//FIND MIN NUMBER IN ARRAY
import java.util.Arrays;
import java.util.Scanner;
public class MinNum {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }
        int min = Integer.MAX_VALUE;
        for (int i = 0; i < n; i++) {
             min = Math.min(min, arr[i]);
            }
        
        System.out.println(min);
        System.out.println(Arrays.toString(arr));

    }
}
//FIND MAX NUM IN ARRAY.

import java.util.Arrays;
import java.util.Scanner;
public class MaxNum {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }
        int max = Integer.MIN_VALUE;
        for (int i = 0; i < n; i++) {
             max = Math.max(max, arr[i]);
            }

        System.out.println(max);
        System.out.println(Arrays.toString(arr));

    }
}

//FIND MAX AND SECOUND MAX IN ARRAY.

import java.util.Scanner;
public class MaxNum {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int arr[]=new int[n];
        for(int i=0;i<n;i++){
            arr[i]=sc.nextInt();
        }
        int maxm=Integer.MIN_VALUE;
        int secoundMaxm= Integer.MIN_VALUE;
       for(int i=0;i<n;i++){
           if(arr[i]>maxm){
               maxm=arr[i];
           }
       }
       for(int i=0;i<n;i++) {
           if (secoundMaxm < arr[i]&&arr[i]<maxm) {
               secoundMaxm = arr[i];
           }
       }
        System.out.println(maxm);
       System.out.println(secoundMaxm);
    }
    }
//CHACK ARRAY IS SORTADE OR NOT.


import java.util.Scanner;
public class SortedArray {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int arr[]=new int[n];
        boolean isSortad=true;
        for(int i=0;i<n;i++){
            arr[i]=sc.nextInt();
        }
        for(int i = 1; i < n; i++) {
            if(arr[i] < arr[i - 1]) {
                isSortad = false;
                break;
           }
           }
       if(isSortad) {
           System.out.println("YAS");
       }else{
           System.out.println("NO");
       }
       sc.close();
    }
    }
//PRINT BENEFITE AFTER SELLING.

import java.util.Scanner;
public class Benefite {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int arr[]=new int[n];
        int sell=0;
        for(int i=0;i<n;i++){
            arr[i]=sc.nextInt();
        }
        for(int i = 1; i < n; i++) {
            int benefit = arr[i] - arr[i-1];
            if ((benefit >0) ){
                    sell += benefit;

            }
        }
//return first unick num example 4 3 5 4 3 return 4

import java.util.Scanner;
public class FirstSameNum {
 public static int sameNUM(int arr[]) {
     int n=arr.length;
        for (int i = 0; i < n; i++) {
            for (int j = i + 1; j < n; j++) {
                if (arr[i] == arr[j]) {
                   return arr[i];
                }
            }
        }
        return -1;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter the number of elements : ");
        int n = sc.nextInt();
        System.out.print("Enter the elements : ");
        int[] arr = new int[n];
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }
        System.out.println(sameNUM(arr));
    }
}
           System.out.println(sell);

       sc.close();
    }
    }
//reverse arr

public class ReverseArray {
    public static void swap(int[] arr, int left, int right) {
        int temp = arr[left];
        arr[left] = arr[right];
        arr[right] = temp;
    }
    public static int[] reverse(int[] arr) {
        int left = 0;
        int right = arr.length - 1;
        while (left < right) {
            swap(arr, left, right);
            left++;
            right--;
        }
        return arr;
    }
    static void printArray(int[] arr) {
        int[] ans = reverse(arr);
        for (int i = 0; i < ans.length; i++) {
            System.out.print(ans[i] + " ");
        }
        System.out.println();
    }
    public static void main(String[] args) {
        int[] arr = {1,2,3,4,5,6,7,8,9,8,11};
        int n = arr.length;
      printArray(arr);
        reverse(arr);

    }
}
//ROTATE THE ARRAY KTH TIME.
import java.util.Scanner;
public class Permutation {

    public static int[] reverse(int[] arr,int k) {
        int n = arr.length;
         k=k%n;
        int []ans = new int[n];
        int j=0;
        for(int i=n-k;i<n;i++) {
            ans[j++] = arr[i];
        }
            for(int i=0;i<n-k;i++) {
                ans[j++] = arr[i];
        }
        return ans;
    }
    public static void printArray(int[] arr) {
        for (int j : arr) {
            System.out.print(j + " ");
        }
    }
    public static void main(String[] args) {
     Scanner scanner=new Scanner(System.in);
     System.out.println("Enter the size of the array");
    int n=scanner.nextInt();
    System.out.println("Enter the elements of the array");
    int[] arr=new int[n];
    for(int i=0;i<n;i++){
        arr[i]=scanner.nextInt();
    }
    System.out.println("Enter the value of k:");
    int k=scanner.nextInt();
    int[] ans=reverse(arr,k);
    printArray(ans);
    }
}
//PRINT ARRAY USING TWO POINTERS (FIRSTLY EVEN NUMBER AND SEOCUND ODD NUMBER)
import java.util.Scanner;
public class SortedArray {
    static void sortedArray(int[] arr) {
        int n = arr.length;
       int left=0;
       int right=n-1;
       while(left<right) {
           if(arr[left]%2==1) {
               left++;
           }else if(arr[right]%2==0) {
               right--;
           }else{
               swap(arr,left,right);
               left++;
               right--;
           }
       }
    }
    static void printArray(int[] arr) {
        for (int j : arr) {
            System.out.print(j + " ");
        }
        System.out.println();
    }
    static void swap(int[] arr, int i, int j) {
        int temp = arr[i];
        arr[i] = arr[j];
        arr[j] = temp;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the size of the array");
        int n = sc.nextInt();
        System.out.println("Enter the elements of the array");
        int[] arr = new int[n];
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        sortedArray(arr);
        printArray(arr);
    }
}
