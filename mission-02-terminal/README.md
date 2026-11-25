# Mission 2 - Command line / Terminal

## 1. Task / objective

Practise basic Terminal commands inside the assignment folder, manage a few safe practice files, understand listing options and pipes, and learn what a package manager does.

## 2. Work completed

### Task 2.1 - Basic Terminal operations

I used macOS Terminal with zsh. These are the commands I tried and the privacy-safe observations I kept.

| Operation | Command | What it does and what I observed |
|---|---|---|
| Current-directory display | `pwd` | Prints the full path of the folder I am in. The project path was `/Users/[redacted]/Documents/Digital-detective-8533`. |
| Directory listing | `ls` | Lists visible files and folders. I saw the mission folders and the root README. |
| Detailed listing | `ls -la` | Shows details and hidden entries too. The owner column contained a Mac account name, so I did not copy that output; it is `[redacted]` here. |
| Change directory | `cd ..` then `cd Digital-detective-8533` | `cd ..` moved up to the Documents folder. I used the project folder name to return. |
| Create directory | `mkdir terminal-practice` | Made a temporary practice folder inside the Mission 2 folder. |
| Create empty file | `touch notes.txt` | Made an empty text file. |
| Copy file | `cp notes.txt backup.txt` | Made a separate copy of the file. |
| Move / rename file | `mv backup.txt notes-backup.txt` | Renamed the copy. It stayed in the same folder. |
| Display file contents | `cat notes.txt` | Printed the two lines I had added to the file. |

### Task 2.2 - Safe file changes

I worked inside `mission-02-terminal/terminal-practice`. I used `printf 'First line: saved from the Terminal.\n' > notes.txt` to write the first line, then used `printf 'Second line: added without replacing the first.\n' >> notes.txt` to add the next one. `cat notes.txt` showed:

```text
First line: saved from the Terminal.
Second line: added without replacing the first.
```

I copied the file with `cp notes.txt backup.txt`, renamed the copy with `mv backup.txt notes-backup.txt`, and checked the folder with `ls -l`. After that I removed the two practice files with `rm notes.txt notes-backup.txt` and removed the now-empty folder with `rmdir terminal-practice`.

- `>` writes to a file and replaces its old contents. `>>` adds text to the end, so the first line stays there.
- `cp` leaves the original file in place and makes another one. `mv` moves a file or changes its name.
- `pwd` tells me which folder a command will work in, which helps avoid creating files in the wrong place.
- `ls` is useful for checking what is in a folder before and after making changes.

### Task 2.3 - Flags and pipes

I compared `ls` with `ls -la`. The `-l` option shows a detailed list, and `-a` includes hidden entries such as `.git`. For human-readable file sizes I used `ls -lah`; `-h` displays sizes in easier units. Detailed listings also show owner information, so I kept that output private and did not paste it here.

I used `ls -la | head -n 5` to show only the first five lines of the detailed listing. The `|` sends the output on its left (`ls -la`) into the command on its right (`head -n 5`), which limits how much is displayed.

### Task 2.4 - Package managers

Homebrew was already installed. `brew --version` showed `Homebrew 7.0.9`, and `brew list` displayed installed packages. I did not install or remove anything. A package manager keeps software installation and updates in one place, which saves time compared with finding each tool and updating it separately.

## 3. Commands / tools used

- Terminal with zsh - ran the command-line practice in the assignment folder.
- `pwd`, `ls`, `cd` - checked my location, listed a folder and moved between folders.
- `mkdir`, `touch`, `printf`, `cat`, `cp`, `mv`, `rm`, `rmdir` - created, wrote, read, copied, renamed and cleaned up temporary practice files.
- `ls -la`, `ls -lah`, `head -n 5`, and `|` - viewed detailed and hidden entries, readable file sizes and only the first few lines.
- `brew --version`, `brew list` - checked Homebrew and viewed its installed package list.

## 4. My understanding

The current folder matters because relative file commands act there. I can check it with `pwd` and check its contents with `ls` before changing anything. I also learned that a single character changes what redirection does: `>` replaces a file's contents, while `>>` appends to it.

Flags change how much detail a command shows. A pipe connects commands, so I can pass a long listing to `head` and just see the first few lines. Homebrew is a package manager that helps keep software packages organised and makes updates easier to manage.

## 5. Difficulties faced

I paused before adding the second line because I almost used `>` again. That would have replaced the first line, which I wanted to keep.

## 6. How I resolved them

I checked the difference between the two redirection symbols and used `>>` for the second line. Then I ran `cat notes.txt` and saw both lines in the file.

## 7. Evidence / files

- This README contains the command notes and the two-line output from the temporary practice file.
- The practice files and folder were removed after I finished, so only this README remains for Mission 2.
- Any account name shown in detailed Terminal output has been redacted as `[redacted]`.

## 8. Commit details

- Commit message: `Complete Terminal and file management mission`
- Status: committed locally on `main`; not pushed to GitHub.
