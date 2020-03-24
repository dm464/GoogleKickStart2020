import java.util.*;
import java.io.*;

class Solution {
    public static void main(String[] args) {
        Scanner scan = new Scanner(new BufferedReader(new InputStreamReader(System.in)));
        int t = scan.nextInt();
        for (int i = 0; i < t; i++) {
            int number = scan.nextInt();
            int budget = scan.nextInt();
            int[] houses = new int[number];
            for (int j = 0; j < number; j++) {
                houses[j] = scan.nextInt();
            }
            System.out.println("Case #" + (i + 1) + ": " + solve(houses, budget));
        }
    }

    static int solve(int[] arr, int budget) {
      countSort(arr);
      int y = 0, sum = 0;
      for (int j = 0; j < arr.length; j++) {
        sum += arr[j];
        if (sum > budget) {
          break;
          }
        y++;
      }
      return y;
    }
    
    static void countSort(int[] arr) {
        int[] count = new int[1000];
        for (int i = 0; i < arr.length; i++) {
            count[arr[i]]++;
        }
        for (int i = 1; i < 1000; i++) {
            count[i] += count[i - 1];
        }
        int[] out = new int[arr.length];
        for (int i = 0; i < out.length; i++) {
            out[count[arr[i]] - 1] = arr[i];
            count[arr[i]]--;
        }
        for (int i = 0; i < arr.length; i ++) {
            arr[i] = out[i];
        }
    }
}
