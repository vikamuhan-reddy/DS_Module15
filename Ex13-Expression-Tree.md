# EX 13 Check if All Characters of One String Are Present in Another

## AIM:
To write a Java program to check if all characters of one string are present in another using Set and `containsAll()`.

## Algorithm
1. Start  
2. Read two strings: `source` and `target`  
3. Convert both strings to Set<Character>  
4. Use `containsAll()` to check if all characters of target are in source  
5. Print "Yes" if true, else print "No"  
6. End

## Program:
```java
import java.util.*;

public class StringCharacterCheck {

    public static boolean allCharsPresent(String source, String target) {
        Set<Character> set1 = new HashSet<>();
        Set<Character> set2 = new HashSet<>();
        
        for(char ch : source.toCharArray()){
            set1.add(ch);
        }
        for(char ch : target.toCharArray()){
            set2.add(ch);
        }
        return set1.containsAll(set2);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String source = sc.nextLine();
        String target = sc.nextLine();

        boolean result = allCharsPresent(source, target);
        System.out.println(result ? "Yes" : "No");

        sc.close();
    }
}

```

## Output:
<img width="320" height="168" alt="Screen Shot 1947-08-25 at 20 06 48" src="https://github.com/user-attachments/assets/c725be0b-8880-456a-97ed-246e765e095c" />


## Result:
Thus the Java program to check if all characters of one string are present in another using Set and containsAll() is implemented successfully.

