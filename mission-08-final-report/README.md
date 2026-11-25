# Mission 8 - Final report

## 1. Task / objective

Review the repository, check the mission work and commit history, and write down what I learned from the assignment. This report also records what is still pending before final submission.

## 2. Work completed

I checked the tracked files, the current branch and recent commit history. The mission folders and their README files are present. The Python files `mission-04-programs/hello.py` and `mission-05-numbers-data/number_converter.py` are also in the repository. Before starting this report, `main` matched `origin/main`, so the work through Mission 7 was pushed.

| Mission | Review status |
|---|---|
| 0 - Repository setup | Setup structure and README committed separately; present on `main`. |
| 1 - Computer basics | IPOS, hardware/software and everyday systems documented and committed. |
| 2 - Terminal | zsh navigation, file operations, flags, pipes and Homebrew documented and committed. |
| 3 - Operating system | macOS, processes, storage, paths and permissions documented and committed with private details redacted. |
| 4 - Programs and code | `hello.py` runs and the compiler/interpreter comparison is documented. |
| 5 - Numbers and data | Conversions, Python checks, encoding and the working converter are documented. |
| 6 - Git and GitHub | The README is committed, but the `update-about` branch and Pull Request are still pending. |
| 7 - Networking | Network concepts and privacy-safe `example.com` observations are documented and committed. |
| 8 - Final report | This README is being committed locally; it still needs to be pushed. |

The separate commits for Missions 0–7 are visible in the recent history. The Mission 6 branch and PR step has not been completed, so I have not marked that activity as finished.

### How to run the converter

From the repository root, run:

```sh
python3 mission-05-numbers-data/number_converter.py
```

It asks for a decimal integer and displays the binary and hexadecimal forms.

### Final review notes

- All mission folders, mission README files, `hello.py`, `number_converter.py` and the optional `evidence` folder are present.
- Each mission from 0 through 7 has its own commit on `main`; `main` was in sync with `origin/main` before this report.
- Mission 6 still needs the `update-about` branch, the root README “My Learning” update and the Pull Request.
- The root README still has its earlier status text saying Missions 1–8 are not started and Mission 0 is not pushed. It also needs a learning summary and converter run instructions. I have left it untouched because this final update is limited to this Mission 8 README.
- This Mission 8 commit is local and has not been pushed. I have not submitted a repository link through the instructor's form.

## 3. Commands / tools used

- `git status --short --branch` - checked the working tree and whether `main` matched `origin/main`.
- `git log --oneline --decorate` - reviewed the separate mission commits.
- `git ls-files` - checked that the mission folders and required files were tracked.
- `python3 mission-05-numbers-data/number_converter.py` - command to run the converter from the repository root.

## 4. My understanding

The missions fit together like one flow. Mission 0 gave the work a repository and a place for each part. In Mission 1, I traced typing as input, the CPU and memory handling the editor's work, the screen showing output and the SSD keeping the saved file. Mission 2 showed me how zsh commands move through folders and create, inspect and clean up files. Mission 3 helped me see macOS managing processes, memory, devices, storage and file permissions.

In Mission 4, Python source code became actions when I ran it with the interpreter. Mission 5 showed that the values and text used by programs are stored as bits and bytes: binary and hexadecimal are ways to write numbers, while ASCII and UTF-8 map characters to data. Git then keeps selected project changes as commits, and GitHub holds the remote copy. On a network, DNS finds an address for a name, routers forward packets, and a browser client uses HTTP or HTTPS to request a response from a server.

My biggest lesson was to check what a command actually did instead of guessing. I got better at checking the current folder, reading an error, using the right base for a number, and keeping private computer details out of notes. I also understand that the work is not fully finished while the Mission 6 branch/PR and final README updates are still pending.

## 5. Difficulties faced

During the final check, the root README still showed the early “not started” statuses even though the mission commits were present. That made it easy to give a misleading completion summary.

## 6. How I resolved them

I compared the root README with the tracked files and commit history, then wrote the actual status in this report. I also listed the root README refresh and Mission 6 branch/PR as remaining items rather than claiming they were done. The root README itself is unchanged in this Mission 8 update.

## 7. Evidence / files

- This README contains the final mission status, review notes, learning summary and converter command.
- The converter and Python program are in their Mission 5 and Mission 4 folders.
- No Mac username, device name, Wi-Fi name, local IP or MAC address, or serial number is included.

## 8. Commit details

- Commit message: `Complete final report and review assignment`
- Status: committed locally on `main`; not pushed to GitHub.
