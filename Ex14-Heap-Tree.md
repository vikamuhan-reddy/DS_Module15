# EX 14 Remove All Duplicate Characters from a String Using HashMap

## AIM:
To write a Java program to remove all duplicate characters from a string using HashMap.

## Algorithm
1. Start  
2. Read the input string  
3. Create a HashMap<Character, Boolean> to store characters  
4. Traverse the string character by character  
5. If a character is not in the map, add it to the map and append to result string  
6. Return the result string  
7. Print the string without duplicates  
8. End
   

## Program:
```java
import java.util.*;

public class RemoveDuplicatesUsingHashMap {
    public static String removeDuplicates(String s) {
        HashMap<Character, Boolean> map = new HashMap<>();
        String val = "";
        
        for(char ch : s.toCharArray()){
            if(!map.containsKey(ch)){
                map.put(ch, true);
                val += ch;
            }
        }
        return val;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String input = sc.nextLine();
        String output = removeDuplicates(input);
        System.out.println(output);
        sc.close();
    }
}
```

## Output:

<img width="317" height="153" alt="Screen Shot 1947-08-25 at 20 09 29" src="https://github.com/user-attachments/assets/a0e8f915-ebc6-4575-aae2-437908e1a452" />


## Result:
Thus the Java program to remove all duplicate characters from a string using HashMap is implemented successfully.

