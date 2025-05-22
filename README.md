# Arrays
//Chack frequency of array to chack who`s number come odd time
like[2,2,3,4,4] there ans is 3   */

import java.util.Arrays;
public class Codeforces {
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

public class Codeforces {
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

public class Code1 {
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
