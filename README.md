import java.util.ArrayList;
import java.util.List;
import java.util.stream.Collectors;

public class PipelineExample {
    public static void main(String[] args) {
        List<String> fruits = new ArrayList<>();
        fruits.add("Apple");
        fruits.add("Banana");
        fruits.add("Orange");
        fruits.add("Grapes");
        fruits.add("Watermelon");

        List<String> processedFruits = fruits.stream()
                .filter(fruit -> fruit.length() > 5) // Filter fruits with length greater than 5
                .map(String::toUpperCase) // Convert fruits to uppercase
                .sorted() // Sort the fruits alphabetically
                .collect(Collectors.toList()); // Collect the processed fruits into a new list

        // Print the processed fruits
        for (String fruit : processedFruits) {
            System.out.println(fruit);
        }
    }
}
