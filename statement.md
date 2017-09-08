Search for the data by using the methods of Stream classes...
findFirst
findAny
anyMatch
allMatch
noneMatch

Methods ending with "Match" returns boolean value.
Methods starting with "find" returns return Optional<T> (we discuss Optional<T> in further playgrounds)

```java runnable
// { autofold
public class Main {

public static void main(String[] args) {
// }

//returns false
boolean anyMatch
    = IntStream.of(-6, -7, -5, -2, -8, -1, -9).anyMatch(temp -> temp > 0);
System.out.println("anyMatch(temp -> temp > 0): " + anyMatch);

//returns false
boolean allMatch
    = IntStream.of(-6, -7, -5, -2, -8, -1, -9).allMatch(temp -> temp > 0);
System.out.println("allMatch(temp -> temp > 0): " + allMatch);

//returns true
boolean noneMatch
    = IntStream.of(-6, -7, -5, -2, -8, -1, -9).noneMatch(temp -> temp > 0);
System.out.println("noneMatch(temp -> temp > 0): " + noneMatch);

OptionalInt temperature = IntStream.of(-6, -7, 5, -2, -8, 1, 9)
                                          .filter(temp -> temp > 0)
                                          .findFirst();
System.out.println("First matching value > 0 is " + temperature.getAsInt());

//{ autofold
}

}
//}
```

