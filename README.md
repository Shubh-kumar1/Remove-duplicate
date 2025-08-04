# Remove-duplicate

import java.util.*;

public class BrokenDuplicateRemover {
    public static void main(String[] args) {
        int[] arr = {1, 2, 2, 3, 4, 4, 5};
        Arrays.sort(arr);

        // Incorrect logic: tries to remove duplicates using random index swapping
        for (int i = 0; i < arr.length; i++) {
            if (arr[i] == arr[i + 1]) {
                arr[i] = -1; // Marking duplicate with -1 (bad idea if -1 is a valid value)
                arr[i + 1] = arr[i]; // overwriting next value blindly
            }
        }

        // Wrong filtering: prints all values except -1
        for (int i = 0; i < arr.length; i++) {
            if (arr[i] != -1) {
                System.out.print(arr[i] + " ");
            }
        }
    }
}
