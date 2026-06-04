# Ex14 Tracking the First Unique Number in a Stream using LinkedHashMap
## AIM:
To implement a program that tracks the first unique (non-repeating) number in a stream of integers using a LinkedHashMap.

## Algorithm
1. Start the program.
2. Initialize a LinkedHashMap<Integer, Integer> to store numbers and their frequency count.
3. For each number in the stream, update its count in the map (increment if it already exists).
4. Traverse the map entries to find the first element with a count of 1, which represents the first unique number.
5. Display the first unique number after processing the stream.
6. Stop the program.


## Program:
```
/*
Program to tracks the first unique (non-repeating) number in a stream of integers using a LinkedHashMap.
Developed by:T MOUNISH
RegisterNumber:  212223240098
*/

import java.util.*;

public class FirstUniqueNumber {
    public static void main(String[] args) {

        int[] stream = {4, 5, 4, 5, 3, 2, 3, 6};

        LinkedHashMap<Integer, Integer> map = new LinkedHashMap<>();
        for (int num : stream) {
            map.put(num, map.getOrDefault(num, 0) + 1);

            System.out.print("Current First Unique Number: ");
            boolean found = false;

            for (Map.Entry<Integer, Integer> entry : map.entrySet()) {
                if (entry.getValue() == 1) {
                    System.out.println(entry.getKey());
                    found = true;
                    break;
                }
            }

            if (!found) {
                System.out.println("No Unique Number");
            }
        }
    }
}


```

## Output:

<img width="696" height="622" alt="image" src="https://github.com/user-attachments/assets/fef51a3d-b393-4323-8011-a2dd3f0f89b2" />


## Result:
The program successfully tracks and returns the first unique number at any point in the integer stream using a LinkedHashMap.
