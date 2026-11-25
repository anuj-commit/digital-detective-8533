# Mission 3 - Operating system

## 1. Task / objective

Explore macOS, running processes, available storage, file paths and permissions. I also wrote down what the operating system does while apps are running.

## 2. Work completed

### Task 3.1 - System information

| Information explored | What it tells me | My observation (privacy-safe) |
|---|---|---|
| Operating system / system details | Which operating system is running. | `sw_vers` reported macOS 27.2.1, and `uname -s` reported Darwin. |
| Current account identity | Which account is active in Terminal. | `whoami` returned the account name; I have written it as `[redacted]`. |
| Available and used storage | How much space is used and still available. | In `df -h`, the Data volume showed 926 GiB total, 83 GiB used and 816 GiB available (10% used). |
| System activity snapshot | Which programs are running at that moment. | `ps` showed Google Chrome and its helper processes. Process IDs are temporary and can change. |

### Task 3.2 - Processes

A process is a program or part of a program that is currently running. `ps -A -o pid,comm` shows a PID column and the command for each process. In my snapshot, Google Chrome had PID 35130 and one of its helper processes had PID 35132. Chrome and VS Code are the two application examples for this activity. PIDs are temporary and can change the next time the apps start.

The PID is the number macOS assigns to a running process so it can tell processes apart. Closing an app ends its processes, and opening it again can give it different PIDs.

### Task 3.3 - Paths and permissions

An absolute path starts from the top of the file system. My project path is `/Users/[redacted]/Documents/Digital-detective-8533`. A relative path starts from the folder I am currently in; from the project root, `mission-03-operating-system/README.md` points to this file.

I used `cd mission-03-operating-system` and `pwd` to see the path change when I entered the mission folder. I checked the README with `ls -l`; its permission listing was `-rw-r--r--`. The owner has read (`r`) and write (`w`) permission, but no execute (`x`) permission. I did not change any permissions.

| Permission | Meaning | Example |
|---|---|---|
| `r` - read | Allows the file contents to be read. | Opening this README. |
| `w` - write | Allows the file to be changed. | Editing the README. |
| `x` - execute | Allows a file to be run; on a folder it allows access through it. | Running a script. |

### Task 3.4 - Operating-system responsibilities

| OS responsibility | My explanation | Example |
|---|---|---|
| Process management | Keeps track of running programs and gives each one time to use the CPU. | Chrome and VS Code can both stay responsive while open. |
| Memory management | Gives programs working memory and reuses it when they close. | The open editor keeps its current text in memory while I work. |
| Device management | Helps apps communicate with the computer's hardware. | macOS passes keyboard input to an app and sends its display output to the screen. |
| File management | Organises files and folders and handles reading and saving them. | VS Code can save a source file into a folder on the SSD. |
| User interface / shell | Provides ways for a person to use the computer. | I can use the macOS desktop or type commands in zsh. |
| Security and permissions | Controls which accounts and programs can access or change files. | The permission letters on the README show who can read or write it. |

I also checked Homebrew because it is already installed on this Mac. `brew --version` showed Homebrew 7.0.9, and `brew list` displayed installed packages such as `ca-certificates` and `cairo`. I only looked at the list; I did not install or remove anything.

## 3. Commands / tools used

- `sw_vers`, `uname -s` - checked the macOS version and system name.
- `whoami` - checked the active account; its value is redacted here.
- `df -h` - checked disk size, used space and available space.
- `ps -A -o pid,comm` - viewed running processes with their process IDs and command names.
- `pwd`, `cd` - checked my current path and moved into the Mission 3 folder.
- `ls -l` - checked the README file's permission letters.
- `brew --version`, `brew list` - checked Homebrew and viewed its package list.

## 4. My understanding

The operating system connects apps to the hardware and manages shared resources like CPU time, memory, storage and devices. A process is one running program or part of one, and its PID helps the system keep it separate from other processes. The PID is not permanent; it can change the next time the app starts.

Paths tell me where a file is, and permissions show what the owner and other users are allowed to do with it. I also saw that `df -h` gives a readable storage summary, while `ps` is only a snapshot of processes at the time I run it.

## 5. Difficulties faced

The first `ps` attempt was blocked with an “operation not permitted” message, so I could not see the process list from that Terminal session.

## 6. How I resolved them

I checked the message and reran the read-only `ps` command with the required permission. It then showed Chrome and its helper processes. I only kept the app names in my notes and did not copy any account or device information.

## 7. Evidence / files

- This README contains the privacy-safe system, storage, process and permission observations, plus the OS responsibility table.
- No screenshots or personal account, device or serial details are included.

## 8. Commit details

- Commit message: `Document operating system and file management`
- Status: committed locally on `main`; not pushed to GitHub.
