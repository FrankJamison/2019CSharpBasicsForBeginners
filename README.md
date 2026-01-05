# C# Basics for Beginners — Practice Exercises

This repository contains a set of small **console app** projects created while working through the Udemy course “C# Basics for Beginners: Learn C# Fundamentals by Coding”.

Each exercise is a self-contained project with its own `Program.cs` and `*.csproj` (and often a `*.sln`). The goal is to practice fundamentals: input parsing, branching, loops, collections, and basic string/file manipulation.

## Prerequisites

- **.NET SDK**: these projects target **.NET 8** (`net8.0`).
- **Visual Studio** or **VS Code** (optional) with a C# extension.

## How to run an exercise

From the repository root, run any project with:

```powershell
dotnet run --project "Exercise2-FindingMaxOfTwoNumbers\Exercise2-FindingMaxOfTwoNumbers.csproj"
```

Or run from inside the project folder:

```powershell
cd .\Exercise2-FindingMaxOfTwoNumbers
dotnet run
```

## How to build (without running)

```powershell
dotnet build --project "Exercise2-FindingMaxOfTwoNumbers\Exercise2-FindingMaxOfTwoNumbers.csproj"
```

## Exercises that read from a text file

Exercises 20 and 21 read a file via the relative path `@"../../../text.txt"`. That file lives here:

- `Exercise20-CountWordsInFile\Exercise20-CountWordsInFile\text.txt`
- `Exercise21-FindLongestWordInFile\Exercise21-FindLongestWordInFile\text.txt`

If you run from a different working directory, the relative path may break.

## Project index

> Note: `Exercise16-DuplicateNumbers Test` contains a space in the folder name — keep the quotes.

| Exercise | Folder | Focus | Run command |
| --- | --- | --- | --- |
| 1 | `Exercise1-ValidatingNumbers` | Validating numeric input / ranges | `dotnet run --project "Exercise1-ValidatingNumbers\Exercise1-ValidatingNumbers.csproj"` |
| 2 | `Exercise2-FindingMaxOfTwoNumbers` | Conditional logic: max of two numbers | `dotnet run --project "Exercise2-FindingMaxOfTwoNumbers\Exercise2-FindingMaxOfTwoNumbers.csproj"` |
| 3 | `Exercise3-FindingImageOrientation` | Conditional logic: landscape vs portrait | `dotnet run --project "Exercise3-FindingImageOrientation\Exercise3-FindingImageOrientation.csproj"` |
| 4 | `Exercise4-SpeedCameraLogic` | Conditionals: speed camera / demerit points | `dotnet run --project "Exercise4-SpeedCameraLogic\Exercise4-SpeedCameraLogic.csproj"` |
| 5 | `Exercise5-CountNumbersDivisibleBy3` | Loops: counting with conditions | `dotnet run --project "Exercise5-CountNumbersDivisibleBy3\Exercise5-CountNumbersDivisibleBy3.csproj"` |
| 6 | `Exercise6-CalculateSumOfNumbers` | Loops + accumulation | `dotnet run --project "Exercise6-CalculateSumOfNumbers\Exercise6-CalculateSumOfNumbers.csproj"` |
| 7 | `Exercise7-CalculateFactorial` | Loops: factorial | `dotnet run --project "Exercise7-CalculateFactorial\Exercise7-CalculateFactorial.csproj"` |
| 8 | `Exercise8-GuessNumberBetween1And10` | Random + loops: guessing game | `dotnet run --project "Exercise8-GuessNumberBetween1And10\Exercise8-GuessNumberBetween1And10.csproj"` |
| 9 | `Exercise9-FindMaxValueInListOfNumbers` | Collections: find max in list | `dotnet run --project "Exercise9-FindMaxValueInListOfNumbers\Exercise9-FindMaxValueInListOfNumbers.csproj"` |
| 10 | `Exercise10-FacebookLikes` | Lists/strings: “likes” formatting | `dotnet run --project "Exercise10-FacebookLikes\Exercise10-FacebookLikes.csproj"` |
| 11 | `Exercise11-NameReversal` | Strings/arrays: reverse input | `dotnet run --project "Exercise11-NameReversal\Exercise11-NameReversal.csproj"` |
| 12 | `Exercise12-UniqueNumbers` | Input + uniqueness | `dotnet run --project "Exercise12-UniqueNumbers\Exercise12-UniqueNumbers.csproj"` |
| 13 | `Exercise13-UniqueNumbersInList` | Collections: de-duplication | `dotnet run --project "Exercise13-UniqueNumbersInList\Exercise13-UniqueNumbersInList.csproj"` |
| 14 | `Exercise14-SmallestThreeNumbers` | Collections: selecting smallest values | `dotnet run --project "Exercise14-SmallestThreeNumbers\Exercise14-SmallestThreeNumbers.csproj"` |
| 15 | `Exercise15-ConsecutiveNumberTest` | Parsing + sequence detection | `dotnet run --project "Exercise15-ConsecutiveNumberTest\Exercise15-ConsecutiveNumberTest.csproj"` |
| 16 | `Exercise16-DuplicateNumbers Test` | Duplicate detection | `dotnet run --project "Exercise16-DuplicateNumbers Test\Exercise16-DuplicateNumbers Test.csproj"` |
| 17 | `Exercise17-ValidTimeCheck` | Parsing/validation: time formats | `dotnet run --project "Exercise17-ValidTimeCheck\Exercise17-ValidTimeCheck.csproj"` |
| 18 | `Exercise18-PascalCase` | Strings: converting to PascalCase | `dotnet run --project "Exercise18-PascalCase\Exercise18-PascalCase.csproj"` |
| 19 | `Exercise19-CountVowels` | Strings: vowel counting | `dotnet run --project "Exercise19-CountVowels\Exercise19-CountVowels.csproj"` |
| 20 | `Exercise20-CountWordsInFile` | File I/O: count words in `text.txt` | `dotnet run --project "Exercise20-CountWordsInFile\Exercise20-CountWordsInFile\Exercise20-CountWordsInFile.csproj"` |
| 21 | `Exercise21-FindLongestWordInFile` | File I/O: longest word in `text.txt` | `dotnet run --project "Exercise21-FindLongestWordInFile\Exercise21-FindLongestWordInFile\Exercise21-FindLongestWordInFile.csproj"` |

## Detailed exercise descriptions

### Exercise 1 — Validating numbers

**What it does**: Reads one integer and prints whether it is in the range 1–10.

**How it works**

- Reads input from `Console.ReadLine()` and parses it with `Convert.ToInt32`.
- Uses a range check (`number >= 1 && number <= 10`) to choose between `Valid` and `Invalid`.

**Input format**: a single integer (example: `7`).

**Output**: `Valid` or `Invalid`.

### Exercise 2 — Max of two numbers

**What it does**: Reads two integers and prints the larger.

**How it works**

- Parses both integers.
- Uses the ternary operator to choose the maximum.

**Input format**: two lines, each an integer.

**Output**: `The highest number is X`.

### Exercise 3 — Image orientation

**What it does**: Reads height and width and prints whether the image is landscape or portrait.

**How it works**

- Compares width vs height.
- Prints `Landscape` when `width > height`; otherwise `Portrait`.

**Input format**: two integers (height then width).

**Output**: `Landscape` or `Portrait`.

**Note**: square images are treated as `Portrait`.

### Exercise 4 — Speed camera logic

**What it does**: Computes demerit points based on how far over the limit the car is.

**How it works**

- If `speed <= limit`, prints `OK`.
- Otherwise computes points as `(speed - limit) / 5` (integer division).
- Prints points when 1–12; prints `License Suspended!` when > 12.

**Input format**: two integers (speed limit, then car speed).

### Exercise 5 — Count numbers divisible by 3

**What it does**: Counts how many numbers between 1 and 100 are divisible by 3.

**How it works**

- Loops from 1 to 100.
- Increments a counter when `i % 3 == 0`.

**Input**: none.

### Exercise 6 — Sum of numbers until `OK`

**What it does**: Keeps reading integers and adds them up until the user types `OK`.

**How it works**

- Loops forever with `while (true)`.
- Breaks on the exact sentinel string `OK`.
- Otherwise parses the input as an integer and accumulates the sum.

**Input format**: one number per line, then `OK`.

### Exercise 7 — Factorial

**What it does**: Prints `n!`.

**How it works**

- Initializes `factorial = 1`.
- Multiplies `factorial` by `n, n-1, ..., 1`.

**Input format**: one integer `n`.

**Note**: the result uses `int`, so large `n` will overflow.

### Exercise 8 — Guess a number

**What it does**: Picks a random number and gives the user 4 attempts to guess it.

**How it works**

- Uses `new Random().Next(1, 10)` to generate the target.
- Reads guesses up to 4 times.
- Prints a win message if guessed, else prints the target.

**Input format**: up to 4 integer guesses.

**Note**: `Next(1, 10)` generates 1–9 (10 is never chosen).

### Exercise 9 — Max from comma-separated list

**What it does**: Reads a comma-separated list of integers and prints the maximum.

**How it works**

- Splits the input on `,`.
- Parses each number and tracks the maximum.

**Input format**: one line like `5, 3, 8, 1`.

### Exercise 10 — Facebook likes

**What it does**: Collects names until blank input and prints a “likes” summary.

**How it works**

- Stores names in a list.
- If 1 name: `Name likes your post.`
- If 2 names: `Name1 and Name2 like your post.`
- If >2: `Name1, Name2 and N others like your post.`

**Input format**: one name per line; stop by pressing Enter on an empty line.

### Exercise 11 — Name reversal

**What it does**: Prints the input name reversed.

**How it works**

- Copies characters into a new `char[]` from end to start.
- Builds the result with `new string(charArray)`.

### Exercise 12 — Five unique numbers

**What it does**: Keeps prompting until the user enters 5 unique integers, then prints them sorted.

**How it works**

- Uses a `List<int>`.
- Rejects duplicates via `Contains`.
- Sorts and prints.

### Exercise 13 — Unique numbers until `quit`

**What it does**: Reads integers until the user types `quit`, then prints the unique values.

**How it works**

- Collects values, sorts them, then builds a second list of unique values.
- Uses a case-insensitive `quit` check.

### Exercise 14 — Smallest three numbers

**What it does**: Prompts for a comma-separated list with at least 5 numbers, then prints the 3 smallest.

**How it works**

- Validates the list length (re-prompts until it has ≥ 5).
- Parses to integers, sorts, and prints the first three.

### Exercise 15 — Consecutive number test

**What it does**: Reads hyphen-separated integers and prints whether they form a consecutive sequence.

**How it works**

- Splits on `-`, parses to integers, sorts.
- Checks that each number is exactly `previous + 1`.

**Input format**: one line like `5-6-7-8-9`.

**Note**: because it sorts first, input order doesn’t matter (`3-1-2` is still consecutive).

### Exercise 16 — Duplicate numbers test

**What it does**: Reads hyphen-separated integers and prints `Duplicates` if any duplicates exist.

**How it works**

- Returns immediately on blank input.
- Sorts and checks adjacent values for equality.

### Exercise 17 — Valid time check

**What it does**: Validates a 24-hour time string and prints `OK` or `Invalid Time`.

**How it works**

- Splits on `:` and parses hours/minutes.
- Valid ranges: hours 0–23, minutes 0–59.
- Uses `try/catch` to handle parsing failures.

**Input format**: `HH:MM` (note: the code accepts `7:5` as valid).

### Exercise 18 — PascalCase conversion

**What it does**: Converts a phrase into PascalCase and prints it.

**How it works**

- Rejects blank input.
- Splits on spaces, capitalizes the first letter of each word, lowercases the rest, concatenates.

**Input format**: e.g. `number of students` → `NumberOfStudents`.

### Exercise 19 — Count vowels

**What it does**: Counts vowels in a word and prints the count.

**How it works**

- Lowercases the input.
- Counts characters in `{ a, e, i, o, u }`.

### Exercise 20 — Count words in a file

**What it does**: Reads `text.txt` and prints the number of words.

**How it works**

- Loads the full file text with `File.ReadAllText`.
- Splits using `text.Split(' ')` and prints the resulting array length.

**Note**: splitting only on `' '` means multiple spaces/newlines can affect the count.

### Exercise 21 — Find the longest word in a file

**What it does**: Reads `text.txt` and prints the longest word.

**How it works**

- Loads the full file text.
- Splits on `' '`.
- Tracks the word with the highest length.

## Common patterns you’ll see

- `Console.ReadLine()` + `Convert.ToInt32` for basic parsing.
- `Split(...)` to parse comma/hyphen/space-separated lists.
- `List<int>` for accumulation and basic set-like operations (`Contains`).
- `Sort()` + a linear scan for tasks like “find duplicates”, “find smallest”, and “check consecutive”.

## Notes

- Each exercise is intentionally small and focused.
- Each project has `bin/` and `obj/` folders (build outputs).
