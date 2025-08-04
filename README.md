# Remove-duplicate

import java.util.Arrays;

public class RemoveDuplicatesClean {
    public static void main(String[] args) {
        int[] arr = {1, 2, 2, 3, 4, 4, 5};
        Arrays.sort(arr);

        int index = 0;
        for (int i = 0; i < arr.length; i++) {
            if (i == 0 || arr[i] != arr[i - 1]) {
                arr[index++] = arr[i];
            }
        }

        System.out.print("Unique elements: ");
        for (int i = 0; i < index; i++) {
            System.out.print(arr[i] + " ");
        }
    }
}
