# Mission 4 - Programs and code

## 1. Task / objective

Write and run a one-line Python program, then compare how a compiler and an interpreter handle source code.

## 2. Work completed

I wrote `hello.py` with a `print` statement and ran it from Terminal with Python 3. The output was:

```text
Hello from Python
```

I also made a short comparison table for compilers and interpreters.

| Point | Compiler | Interpreter |
|---|---|---|
| When translation / execution happens | Translates the source before the program runs. | Reads and carries out instructions while the program runs. |
| Typical output | Often produces another form of the program, such as machine code or an executable. | Usually produces the program's result as it runs, without making a separate executable for this example. |
| One example | A C compiler such as `clang`. | Python 3 running `hello.py`. |
| One advantage | The translated program can run without translating the source each time. | It is quick to try a change and run the source again. |

A compiler usually translates source code into another form before the program runs. An interpreter reads instructions and carries them out as the program is running. The compiler often leaves a separate translated file, while this interpreter example just prints its result in Terminal. Some languages use a mix of these approaches, so this is a basic comparison.

## 3. Commands / tools used

- Terminal - ran the program from the assignment folder.
- `python3 mission-04-programs/hello.py` - asked Python 3 to run the script; it printed `Hello from Python`.
- `python3 --version` - checked the version used, Python 3.14.7.

## 4. My understanding

The lines in `hello.py` are source code. When I run `python3 mission-04-programs/hello.py`, Python reads the file and executes the `print` instruction, which sends the text to Terminal. This short program has no variables or decisions: the text is a string given directly to `print`. In a longer program, variables can hold values and logic such as `if` statements can choose what happens next.

Errors are messages that help show what went wrong. A syntax error means the code is not written in a form Python can understand, while a runtime error happens after the program starts and tries to do something invalid. I saw a syntax error while writing this file and fixed it before the final run.

## 5. Difficulties faced

I missed the closing parenthesis on the `print` line the first time. Python reported `SyntaxError: '(' was never closed` and pointed to line 1.

## 6. How I resolved them

I reread the line, added the missing `)`, and ran the script again with `python3 mission-04-programs/hello.py`. It then printed `Hello from Python` as expected.

## 7. Evidence / files

- `hello.py` - the working one-line Python program.
- This README - the run output, compiler/interpreter comparison and notes about source code and errors.
- No personal Mac details are included.

## 8. Commit details

- Commit message: `Run hello.py and compare compilers and interpreters`
- Status: committed locally on `main`; not pushed to GitHub.
