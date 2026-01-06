# Linux-and-Shell-scripting-assignments

This repository contains **Linux shell scripting assignments** focused on **system automation**, **configuration management**, and **file handling**.
The scripts demonstrate practical Linux administration concepts such as input validation, filesystem search, compression handling, and safe configuration updates.

# Files Included

* `update_conf.sh` – Script to update configuration values in `sig.conf`
* `sig.conf` – Sample configuration file
* `research_lab.sh` – Script to create, detect, and uncompress a `research` file
* `README.md` – Project documentation


#  Assignment 1: Configuration Update Script

## User Inputs

The script prompts the user for validated inputs:

* **Component Name:** `INGESTOR | JOINER | WRANGLER | VALIDATOR`
* **Scale:** `LOW | MID | HIGH`
* **View:** `Auction | Bid`
* **Count:** Single-digit number (`0–9`)


## How It Works

* Accepts input via terminal
* Validates inputs against allowed values
* Searches for the **first matching line** in `sig.conf`
* Updates **only the count value** (`vdopia-etl=<count>`)
* Prevents accidental modification of multiple lines


## How to Run

```bash
chmod +x update_conf.sh
./update_conf.sh
```

# Assignment 2: Research File Automation Script


This script automates the handling of a compressed file named **`research`**.
It creates the file, compresses it, searches the filesystem for it, detects the compression type, and uncompresses it automatically.


## What the Script Does

* Creates a file named `research`
* Compresses it using **gzip**
* Searches the entire Linux filesystem for `research.*`
* Detects compression type based on file extension
* Automatically uncompresses the file
* Works system-wide from any directory

##  How to Run

```bash
chmod +x research_lab.sh
./research_lab.sh
```

##  Compression Types Supported

* `.gz` (gzip)
* `.bz2` (bzip2)
* `.xz` (xz)
* `.zip` (zip)


# Tools & Concepts Used

* Bash shell scripting
* Input validation
* `find`, `sed`, `case` statements
* Linux file system operations
* Compression & decompression utilities
* Script execution from `/usr/local/bin`


## 🎯 Key Learning Outcomes

* Safe and controlled configuration file updates
* Writing reusable and system-wide shell scripts
* Automating file detection and decompression
* Applying real-world Linux administration concepts


## Author

**Chandana R**


