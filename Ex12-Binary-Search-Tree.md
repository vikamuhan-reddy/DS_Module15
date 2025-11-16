# EX 12 Sort a List of Names Using TreeSet

## AIM:
To write a Java program to sort a list of names using TreeSet and display them in ascending order.

## Algorithm
1. Start  
2. Read the number of names N  
3. Read N names from the user and add them to a TreeSet  
4. Convert the TreeSet to a list and sort it  
5. Print the sorted names, each on a new line  
6. End

## Program:
```java
import java.util.*;

public class SortNamesTreeSet {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        TreeSet<String> names = new TreeSet<>();
        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String name = sc.nextLine().trim();
            names.add(name);
        }

        printSortedNames(names);

        sc.close();
    }

    public static void printSortedNames(TreeSet<String> names) {
        ArrayList<String> list = new ArrayList<>();
        for(String ch : names){
            list.add(ch);
        }
        Collections.sort(list);
        System.out.println("Names in sorted order:");
        for(String c : list){
            System.out.println(c);
        }
    }
}
```


## Output:
<img width="496" height="328" alt="Screen Shot 1947-08-25 at 20 04 24" src="https://github.com/user-attachments/assets/242d4235-13ec-49ab-a64a-e89bb3b90212" />


## Result:
Thus the Java program to sort a list of names using TreeSet and display them in ascending order is implemented successfully.

