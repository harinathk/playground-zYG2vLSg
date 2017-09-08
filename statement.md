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
import java.util.stream.IntStream;
import java.util.OptionalInt;
public class Main {

public static void main(String[] args) {
// }

//returns false
boolean anyMatch
    = IntStream.of(-6, -7, -5, -2, -8, -1, -9).anyMatch(value -> value > 0);
System.out.println("anyMatch(value -> value > 0): " + anyMatch);

//returns false
boolean allMatch
    = IntStream.of(-6, -7, -5, -2, -8, -1, -9).allMatch(value -> value > 0);
System.out.println("allMatch(value -> value > 0): " + allMatch);

//returns true
boolean noneMatch
    = IntStream.of(-6, -7, -5, -2, -8, -1, -9).noneMatch(value -> value > 0);
System.out.println("noneMatch(value -> value > 0): " + noneMatch);

OptionalInt optValue = IntStream.of(-6, -7, 5, -2, -8, 1, 9)
                                          .filter(value -> value > 0)
                                          .findFirst();
System.out.println("First matching value > 0 is " + optValue.getAsInt());

//{ autofold
}

}
//}
```

