# C# Fundamentals Practice (Console Apps)

A collection of small, self-contained **C#/.NET console applications** built as hands-on practice while working through a C# fundamentals curriculum.

This repo is intentionally “many tiny projects” instead of one big app: each exercise focuses on a specific concept (input parsing, control flow, collections, strings, and basic file I/O).

## What this demonstrates (for employers/recruiters)

- **Core C# fluency**: variables, conditionals, loops, collections, and string manipulation.
- **Problem decomposition**: each folder is a focused problem statement with a single entrypoint.
- **Practical console UX**: prompt/validate/loop patterns common in CLI tooling.
- **.NET build literacy**: projects are runnable via the `dotnet` CLI and IDEs.

## Tech stack

- **Language**: C#
- **Runtime/SDK**: .NET (targets **net8.0**)
- **Project type**: Console applications (`Program.cs`)
- **Build tools**: `dotnet build`, `dotnet run`

## Repository layout

- Each `ExerciseXX-*` folder is a standalone project.
- Most exercises include a solution file (`*.sln`) and a project file (`*.csproj`).
- Build outputs are in `bin/` and `obj/` (generated).

## Prerequisites

- Install the **.NET 8 SDK** (or newer that can build `net8.0`).
- Optional IDE:
	- Visual Studio 2022+
	- VS Code + C# extension

Verify your SDK:

```powershell
dotnet --version
```

## Quick start

Run a single exercise directly from the repo root:

```powershell
dotnet run --project "Exercise2-FindingMaxOfTwoNumbers\Exercise2-FindingMaxOfTwoNumbers.csproj"
```

Or run from inside a project folder:

```powershell
cd .\Exercise2-FindingMaxOfTwoNumbers
dotnet run
```

## Build instructions

Build one project:

```powershell
dotnet build "Exercise2-FindingMaxOfTwoNumbers\Exercise2-FindingMaxOfTwoNumbers.csproj"
```

Build all exercises (PowerShell):

```powershell
Get-ChildItem -Recurse -Filter *.csproj | ForEach-Object { dotnet build $_.FullName }
```

## Common dev commands

Restore packages for a specific exercise:

```powershell
dotnet restore "Exercise2-FindingMaxOfTwoNumbers\Exercise2-FindingMaxOfTwoNumbers.csproj"
```

Clean build outputs for a specific exercise:

```powershell
dotnet clean "Exercise2-FindingMaxOfTwoNumbers\Exercise2-FindingMaxOfTwoNumbers.csproj"
```

## File I/O exercises (Exercises 20–21)

Exercises 20 and 21 read a file using the relative path `@"../../../text.txt"`.

The `text.txt` files live here:

- `Exercise20-CountWordsInFile\Exercise20-CountWordsInFile\text.txt`
- `Exercise21-FindLongestWordInFile\Exercise21-FindLongestWordInFile\text.txt`

If you run with an unusual working directory, that relative path may not resolve. Running via `dotnet run --project <path-to-csproj>` is the most reliable approach.

## Exercise index

> Note: `Exercise16-DuplicateNumbers Test` contains a space in the folder name—use quotes in CLI commands.

| # | Folder | Focus | Run |
| ---: | --- | --- | --- |
| 1 | `Exercise1-ValidatingNumbers` | Validating numeric input/range checks | `dotnet run --project "Exercise1-ValidatingNumbers\Exercise1-ValidatingNumbers.csproj"` |
| 2 | `Exercise2-FindingMaxOfTwoNumbers` | Conditionals: max of two values | `dotnet run --project "Exercise2-FindingMaxOfTwoNumbers\Exercise2-FindingMaxOfTwoNumbers.csproj"` |
| 3 | `Exercise3-FindingImageOrientation` | Conditionals: landscape vs portrait | `dotnet run --project "Exercise3-FindingImageOrientation\Exercise3-FindingImageOrientation.csproj"` |
| 4 | `Exercise4-SpeedCameraLogic` | Branching: demerit points / suspension logic | `dotnet run --project "Exercise4-SpeedCameraLogic\Exercise4-SpeedCameraLogic.csproj"` |
| 5 | `Exercise5-CountNumbersDivisibleBy3` | Loops: counting with conditions | `dotnet run --project "Exercise5-CountNumbersDivisibleBy3\Exercise5-CountNumbersDivisibleBy3.csproj"` |
| 6 | `Exercise6-CalculateSumOfNumbers` | Loops: sentinel input (`OK`) + accumulation | `dotnet run --project "Exercise6-CalculateSumOfNumbers\Exercise6-CalculateSumOfNumbers.csproj"` |
| 7 | `Exercise7-CalculateFactorial` | Loops: factorial calculation | `dotnet run --project "Exercise7-CalculateFactorial\Exercise7-CalculateFactorial.csproj"` |
| 8 | `Exercise8-GuessNumberBetween1And10` | Random + attempts loop | `dotnet run --project "Exercise8-GuessNumberBetween1And10\Exercise8-GuessNumberBetween1And10.csproj"` |
| 9 | `Exercise9-FindMaxValueInListOfNumbers` | Parsing + collections: find max | `dotnet run --project "Exercise9-FindMaxValueInListOfNumbers\Exercise9-FindMaxValueInListOfNumbers.csproj"` |
| 10 | `Exercise10-FacebookLikes` | Lists/strings: “likes” formatting | `dotnet run --project "Exercise10-FacebookLikes\Exercise10-FacebookLikes.csproj"` |
| 11 | `Exercise11-NameReversal` | Strings/arrays: reverse input | `dotnet run --project "Exercise11-NameReversal\Exercise11-NameReversal.csproj"` |
| 12 | `Exercise12-UniqueNumbers` | Collections: uniqueness enforcement | `dotnet run --project "Exercise12-UniqueNumbers\Exercise12-UniqueNumbers.csproj"` |
| 13 | `Exercise13-UniqueNumbersInList` | Collections: de-duplication | `dotnet run --project "Exercise13-UniqueNumbersInList\Exercise13-UniqueNumbersInList.csproj"` |
| 14 | `Exercise14-SmallestThreeNumbers` | Collections: sorting/selecting smallest | `dotnet run --project "Exercise14-SmallestThreeNumbers\Exercise14-SmallestThreeNumbers.csproj"` |
| 15 | `Exercise15-ConsecutiveNumberTest` | Parsing + sequence validation | `dotnet run --project "Exercise15-ConsecutiveNumberTest\Exercise15-ConsecutiveNumberTest.csproj"` |
| 16 | `Exercise16-DuplicateNumbers Test` | Duplicate detection | `dotnet run --project "Exercise16-DuplicateNumbers Test\Exercise16-DuplicateNumbers Test.csproj"` |
| 17 | `Exercise17-ValidTimeCheck` | Parsing/validation: 24h time strings | `dotnet run --project "Exercise17-ValidTimeCheck\Exercise17-ValidTimeCheck.csproj"` |
| 18 | `Exercise18-PascalCase` | Strings: PascalCase conversion | `dotnet run --project "Exercise18-PascalCase\Exercise18-PascalCase.csproj"` |
| 19 | `Exercise19-CountVowels` | Strings: counting vowels | `dotnet run --project "Exercise19-CountVowels\Exercise19-CountVowels.csproj"` |
| 20 | `Exercise20-CountWordsInFile` | File I/O: count words in `text.txt` | `dotnet run --project "Exercise20-CountWordsInFile\Exercise20-CountWordsInFile\Exercise20-CountWordsInFile.csproj"` |
| 21 | `Exercise21-FindLongestWordInFile` | File I/O: longest word in `text.txt` | `dotnet run --project "Exercise21-FindLongestWordInFile\Exercise21-FindLongestWordInFile\Exercise21-FindLongestWordInFile.csproj"` |

## Common implementation patterns

- `Console.ReadLine()` + numeric parsing for basic input handling.
- `Split(...)` for parsing comma/hyphen/space-separated lists.
- `List<T>` for accumulation and simple set-like operations (e.g., `Contains`).
- Sorting + linear scans for tasks like smallest/duplicates/consecutive checks.

## Troubleshooting

- **Folder names with spaces**: quote paths in `dotnet` commands.
- **SDK mismatch**: install .NET 8 SDK (projects target `net8.0`).
- **Restore issues**: run `dotnet restore` inside the exercise folder or against the `.csproj`.

## Notes

- These projects are intentionally small and focused (learning exercises rather than a production application).
- There are no external dependencies; everything uses the standard .NET libraries.
