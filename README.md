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
