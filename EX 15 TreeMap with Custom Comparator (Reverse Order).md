# EX 15 TreeMap with Custom Comparator (Reverse Order)

## AIM:
To write a Java program to create a TreeMap where keys are stored in reverse order using a custom comparator.

## Algorithm
1. Start  
2. Read the number of entries N  
3. Read N key-value pairs from the user  
4. Store entries in a HashMap  
5. Create a TreeMap with `Comparator.reverseOrder()`  
6. Add all entries from the HashMap to the TreeMap  
7. Print all entries in reverse key order  
8. End

## Program:
```java
import java.util.*;

public class ReverseOrderTreeMap {
    public static TreeMap<Integer, String> createReverseTreeMap(Map<Integer, String> input) {
        TreeMap<Integer,String> tmap = new TreeMap<>(Comparator.reverseOrder());
        for(Integer key : input.keySet()){
            tmap.put(key, input.get(key));
        }
        return tmap;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Map<Integer, String> inputMap = new HashMap<>();
        int n = sc.nextInt(); 
        for (int i = 0; i < n; i++) {
            int key = sc.nextInt();
            sc.nextLine();
            String value = sc.nextLine();
            inputMap.put(key, value);
        }
        TreeMap<Integer, String> reverseMap = createReverseTreeMap(inputMap);
        reverseMap.forEach((k, v) -> System.out.println(k + " -> " + v));
        sc.close();
    }
}
```


## Output:

<img width="426" height="346" alt="Screen Shot 1947-08-25 at 20 11 36" src="https://github.com/user-attachments/assets/74407a3a-9482-4b56-a7ff-5b1aa502debf" />


## Result:
Thus the Java program to create a TreeMap with keys stored in reverse order using a custom comparator is implemented successfully.

