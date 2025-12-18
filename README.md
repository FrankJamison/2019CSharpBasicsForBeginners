# C# Basics for Beginners — Practice Exercises

This repository contains a set of small **console app** projects created while working through the Udemy course **“C# Basics for Beginners: Learn C# Fundamentals by Coding”**.

Each exercise is a self-contained project with its own `Program.cs` and `*.csproj` (and often a `*.sln`).

## Prerequisites

You can run these projects using either Visual Studio or the .NET CLI.

- **.NET SDK**
	- Many projects target **.NET Core 2.1** (`netcoreapp2.1`).
	- If you hit a build error like “The current .NET SDK does not support targeting .NET Core 2.1”, either:
		- Install an older SDK that supports `netcoreapp2.1` (common for older coursework), or
		- Retarget the projects to a newer framework (see **Retargeting** below).
- **VS Code (optional)** with the **C#** extension (or **Visual Studio**).

## How to run an exercise (recommended)

From the repository root:

```powershell
dotnet run --project "Exercise2-FindingMaxOfTwoNumbers\Exercise2-FindingMaxOfTwoNumbers.csproj"
```

This approach works well because each exercise is its own project.

### Alternative: run from the project folder

```powershell
cd .\Exercise2-FindingMaxOfTwoNumbers
dotnet run
```

## How to build (without running)

```powershell
dotnet build --project "Exercise2-FindingMaxOfTwoNumbers\Exercise2-FindingMaxOfTwoNumbers.csproj"
```

## Exercises that read from a text file

Exercises 20 and 21 include a `text.txt` file and use a relative path like `@"../../../text.txt"`.

That file is located in the project folder:

- `Exercise20-CountWordsInFile\Exercise20-CountWordsInFile\text.txt`
- `Exercise21-FindLongestWordInFile\Exercise21-FindLongestWordInFile\text.txt`

If you change how you run the app or your working directory, keep that relative path in mind.

## Retargeting (if your SDK is too new)

If you have a modern .NET SDK and builds fail due to `netcoreapp2.1`, you can retarget each project:

1. Open the project’s `*.csproj`.
2. Change:
	 ```xml
	 <TargetFramework>netcoreapp2.1</TargetFramework>
	 ```
	 to something newer, for example:
	 ```xml
	 <TargetFramework>net6.0</TargetFramework>
	 ```
3. Re-run `dotnet build` / `dotnet run`.

Most beginner console apps retarget cleanly.

## Project catalog

Below is a quick index of the included exercises and how to run them from the repo root.

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

## Notes

- Each exercise is intentionally small and focused.
- You’ll see `bin/` and `obj/` folders inside the exercise directories (build outputs).
