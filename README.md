# Numbered Triangle Pattern in Java

## Description
This Java program generates a right-angled triangle pattern of numbers based on user input. The pattern consists of rows where each row starts from `1` and increments up to the current row number. The program utilizes loops and user input handling to achieve this pattern dynamically.

## Code
```java
package number_patterns;

import java.util.Scanner;
public class Numbered_Triangle
{
    public static void main(String[] args)
    {
        Scanner s = new Scanner(System.in); // Creating Scanner object to take user input
        System.out.println("Enter the number"); // Prompting user for input
        int n = s.nextInt(); // Reading user input as an integer
        
        for(int i = 1; i <= n; i++) // Outer loop for rows
        {
            int num = 1; // Initializing the number to be printed
            for(int j = 1; j <= i; j++) // Inner loop for printing numbers in each row
            {
                System.out.print(num++); // Printing number and incrementing it
            }
            System.out.println(); // Moving to the next line after printing a row
        }
        
        s.close(); // Closing the scanner to prevent resource leak
    }
}
```

---

## Explanation

### 1. **Scanner Class**
- The program imports `java.util.Scanner`, which allows us to take user input.
- `Scanner s = new Scanner(System.in);` creates a `Scanner` object `s` to read input from the console.
- `int n = s.nextInt();` reads an integer input from the user, which determines the number of rows in the pattern.
- `s.close();` is used to close the scanner object to prevent memory/resource leakage.

### 2. **Outer `for` Loop (Controls Rows)**
- `for(int i = 1; i <= n; i++)`
  - The loop runs `n` times, where `n` is the user-input number.
  - Controls the number of rows printed.

### 3. **Inner `for` Loop (Controls Columns and Printing)**
- `for(int j = 1; j <= i; j++)`
  - Runs from `1` to `i`, meaning the first row has `1` number, the second row has `2` numbers, and so on.
  - Controls how many numbers are printed in each row.
- `System.out.print(num++);`
  - Prints the value of `num` and then increments it by `1`.
  - Ensures numbers start from `1` in each row and increase sequentially.
- `System.out.println();`
  - Moves to the next line after printing each row.

## Example Output
### User Input: `4`
```
Enter the number
4
1
12
123
1234
```

## Key Features
- Uses nested loops to construct the number pattern.
- Uses the `Scanner` class to take user input.
- Demonstrates `for` loops and `System.out.print` for pattern printing.

## Complexity Analysis
- **Time Complexity**: `O(n^2)` (Due to nested loops running up to `n`).
- **Space Complexity**: `O(1)` (No extra space is used apart from variables).

## Clone
```
git clone https://github.com/Ananthadatta02/Java-Numbered_Triangle.git
```
