# C-Day-40-Largest-Smallest-Digit
# C Day 40 - Largest and Smallest Digit

This program finds the largest and smallest digit of a given number.

## Example

Input:

```text
58321
```

Output:

```text
Largest digit = 8
Smallest digit = 1
```

## Concepts Used

* while loop
* if condition
* Modulus operator (%)
* Division operator (/)
* Digit extraction
* Variable comparison

## How It Works

1. Extract the last digit using `% 10`.
2. Compare the digit with `largest`.
3. Compare the digit with `smallest`.
4. Update the values when required.
5. Remove the last digit using `/ 10`.
6. Repeat until all digits are checked.

## C Code

```c
#include <stdio.h>

int main()
{
    int num, digit;
    int largest = 0;
    int smallest = 9;

    printf("Enter a number: ");
    scanf("%d", &num);

    while (num != 0)
    {
        digit = num % 10;

        if (digit > largest)
        {
            largest = digit;
        }

        if (digit < smallest)
        {
            smallest = digit;
        }

        num = num / 10;
    }

    printf("Largest digit = %d\n", largest);
    printf("Smallest digit = %d", smallest);

    return 0;
}
```

## Output

```text
Enter a number: 58321
Largest digit = 8
Smallest digit = 1
```
