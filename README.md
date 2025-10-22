# Log Archive Tool

A simple command-line tool to archive logs on a Unix-based system by compressing them and storing them in a new directory. This is useful for removing old logs to keep the system clean while maintaining compressed copies for future reference. This project is a great way to practice shell scripting, working with files and directories, and building CLI tools.

*Project from: https://roadmap.sh/projects/log-archive-tool* 

---

## Features

- Accepts a log directory as a command-line argument.
- Compresses all logs in the specified directory into a `tar.gz` file.
- Saves the archive with a timestamped name for easy reference.
- Logs the date and time of the archive in the archive file name.

---

## Requirements

- Unix-based operating system (Linux, macOS, etc.)
- Bash shell

---

## Installation / Setup

1. **Clone the repository:**

```bash
git clone https://github.com/Salieri20/Log-Archive-Tool.git
cd Log-Archive-Tool
```
2. **Make the script executable:**

```bash
chmod +x log-archive
```
3. **Run the script from the command line, providing the path to the log directory as an argument:**
```bash
./log-archive <log-directory>
```
*Example*
```bash
./log-archive /var/log
```
If successful, the script will create a compressed archive of the logs in the current working directory with a name like: 
```bash
logs_archive_20240816_100648.tar.gz
```
Where 20240816 is the date and 100648 is the time the archive was created. 

**How It Works**
1. The script checks if the provided path is a valid directory.

2. It generates a timestamp using the current date and time.

3. It compresses the directory contents into a tar.gz archive named with the timestamp.

4. If the directory is invalid, it prints an error message.

**Notes**
- Ensure you have write permissions in the directory where you run the script, as the archive will be created there.
- For scheduled automated archiving, consider using cron to run the script at regular intervals. 


