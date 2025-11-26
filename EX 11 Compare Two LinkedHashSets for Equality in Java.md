# EX 11 Compare Two LinkedHashSets for Equality in Java

## AIM:
To write a Java program to compare two LinkedHashSets and determine if they are equal.

## Algorithm
1. Start  
2. Read the number of elements N for the first LinkedHashSet and its elements  
3. Read the number of elements M for the second LinkedHashSet and its elements  
4. Compare the two LinkedHashSets using the `equals()` method  
5. Print "Both LinkedHashSets are equal" if equal, else print "LinkedHashSets are not equal"  
6. End

## Program:
```java
import java.util.*;

public class LinkedHashSetEqualityCheck {

    public static boolean areEqual(LinkedHashSet<String> set1, LinkedHashSet<String> set2) {
        return set1.equals(set2);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        LinkedHashSet<String> linkedHashSet1 = new LinkedHashSet<>();
        LinkedHashSet<String> linkedHashSet2 = new LinkedHashSet<>();

        int n = sc.nextInt();
        sc.nextLine();
        for (int i = 0; i < n; i++) {
            linkedHashSet1.add(sc.nextLine());
        }

        int m = sc.nextInt();
        sc.nextLine();
        for (int i = 0; i < m; i++) {
            linkedHashSet2.add(sc.nextLine());
        }

        if (areEqual(linkedHashSet1, linkedHashSet2)) {
            System.out.println("Both LinkedHashSets are equal");
        } else {
            System.out.println("LinkedHashSets are not equal");
        }

        sc.close();
    }
}
```


## Output:
<img width="587" height="465" alt="Screen Shot 1947-08-25 at 20 01 35" src="https://github.com/user-attachments/assets/035756d1-6fae-494a-8472-0ccfde6da0c8" />


## Result:
Thus the Java program to compare two LinkedHashSets for equality is implemented successfully.

