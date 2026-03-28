# Open Source Audit Toolkit

A collection of bash scripts for auditing, analyzing, and celebrating open-source software on Linux systems. This toolkit provides system reporting, package inspection, security auditing, log analysis, and manifesto generation capabilities.

## Overview

This project contains five specialized bash scripts designed to help you understand and audit your Linux system from an open-source perspective. Each script focuses on a different aspect of system analysis and FOSS (Free and Open Source Software) philosophy.

## Scripts

### 1. System Identity Report (`script.sh`)

Generates a comprehensive system identity report including kernel version, distribution, user information, and licensing details.

**Features:**
- Displays current kernel version and distribution
- Shows logged-in user and home directory
- Reports system uptime and current date/time
- Highlights GPL v2 licensing information

**Usage:**
```bash
bash script.sh
```

**Output includes:**
- Student name and project information
- Linux distribution and kernel version
- Current user and home directory path
- System uptime
- OS licensing details (GPL v2)

---

### 2. FOSS Package Inspector (`script2.sh`)

Inspects installed FOSS packages and provides philosophical context about their importance in the open-source ecosystem.

**Features:**
- Detects package manager (RPM or DEB-based systems)
- Queries running kernel package information
- Provides contextual information about major FOSS projects
- Works across different Linux distributions

**Usage:**
```bash
bash script2.sh
```

**Supported packages:**
- Linux Kernel
- Apache/httpd
- MySQL/MariaDB
- Python
- Git
- And more...

---

### 3. Disk and Permission Auditor (`script3.sh`)

Audits critical system directories for permissions, ownership, and disk usage.

**Features:**
- Scans multiple system directories (`/etc`, `/var/log`, `/home`, `/usr/bin`, `/tmp`, `/boot`, `/lib`)
- Reports permissions, owner, group, and size for each directory
- Checks kernel configuration file existence and permissions
- Handles missing directories gracefully

**Usage:**
```bash
bash script3.sh
```

**Audited directories:**
- `/etc` - System configuration
- `/var/log` - System logs
- `/home` - User home directories
- `/usr/bin` - User binaries
- `/tmp` - Temporary files
- `/boot` - Boot files and kernel
- `/lib` - System libraries

---

### 4. Log File Analyzer (`script4.sh`)

Analyzes log files for specific keywords and provides match statistics.

**Features:**
- Searches log files for specific keywords (case-insensitive)
- Counts total matches
- Displays last 5 matching lines
- Handles empty or missing files with retry logic
- Defaults to searching for "error" if no keyword specified

**Usage:**
```bash
bash script4.sh <logfile> [keyword]
```

**Examples:**
```bash
# Search for errors in syslog
bash script4.sh /var/log/syslog error

# Search for warnings in auth.log
bash script4.sh /var/log/auth.log warning

# Search for failed login attempts
bash script4.sh /var/log/auth.log failed
```

**Parameters:**
- `logfile` (required): Path to the log file to analyze
- `keyword` (optional): Search term (defaults to "error")

---

### 5. Open Source Manifesto Generator (`script5.sh`)

Interactive script that generates a personalized open-source manifesto based on user input.

**Features:**
- Interactive questionnaire about open-source values
- Generates timestamped manifesto file
- Creates unique output files to prevent overwrites
- Celebrates FOSS philosophy and community contribution

**Usage:**
```bash
bash script5.sh
```

**Interactive prompts:**
1. Name one open-source tool you use every day
2. In one word, what does freedom mean to you?
3. Name one thing you would build and share freely

**Output:**
- Creates `manifesto_<username>_<timestamp>.txt`
- Contains personalized manifesto text
- Displays the manifesto on screen

---

## Requirements

- Linux-based operating system
- Bash shell (version 4.0 or higher recommended)
- Standard Unix utilities: `uname`, `whoami`, `uptime`, `date`, `grep`, `awk`, `du`, `ls`
- Package manager: `rpm` or `dpkg` (for script2.sh)
- Appropriate permissions to read system directories and log files

## Installation

1. Clone or download this repository
2. Make scripts executable:
```bash
chmod +x script.sh script2.sh script3.sh script4.sh script5.sh
```

## Quick Start

Run all scripts in sequence:
```bash
bash script.sh
bash script2.sh
bash script3.sh
bash script4.sh /var/log/syslog
bash script5.sh
```

## Philosophy

This toolkit embodies the principles of Free and Open Source Software:
- **Freedom to study**: All scripts are readable and well-commented
- **Freedom to modify**: Adapt these scripts to your needs
- **Freedom to share**: Distribute and improve these tools
- **Community-driven**: Built on the shoulders of giants

## License

This project celebrates open-source software and the GPL v2 license under which the Linux kernel is distributed. The scripts themselves are provided as educational tools for understanding and auditing FOSS systems.

## Contributing

Contributions are welcome! Feel free to:
- Report bugs or issues
- Suggest new features
- Submit pull requests
- Share your manifesto

## Author

Created as part of an Open Source Audit project by Divyam.

---

*"Built on giants. Paying it forward."*
