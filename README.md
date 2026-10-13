# 10Alytics Assignment 1: Linux Fundamentals

## Project Overview

This project documents my practical work for **10Alytics Assignment 1: Linux Fundamentals**. The assignment focuses on using Kali Linux to explore basic system information, examine memory and filesystem usage, and test network connectivity using the Linux command line.

Through this exercise, I practiced essential Linux commands and learned how to interpret system information and basic network diagnostic results.

## Objectives

The main objectives of this assignment were to:

- Identify the current Linux username and hostname.
- Determine the current working directory.
- Examine operating system and kernel information.
- Check filesystem storage and system uptime.
- Test network connectivity using the `ping` command.
- Compare connectivity tests using an IP address and a domain name.
- Interpret packet transmission, packet reception, packet loss, and response times.
- Document command outputs and observations.

## Tools and Technologies

- **Operating System:** Kali Linux
- **Command-Line Interface:** Linux Terminal
- **System Information Commands:** `whoami`, `hostname`, `pwd`, `uname`
- **Resource and Storage Commands:** `df`, `uptime`
- **Network Diagnostic Tool:** `ping`
- **Networking Concepts:** IP addressing, DNS resolution, connectivity, and latency

## Tasks Performed

### 1. Identifying the Current User

**Command:**

```bash
whoami
```

**Purpose:**

The `whoami` command displays the username associated with the current terminal session.

**Result:**

The command returned:

```text
kali
```

**Observation:**

The output confirmed that the current user was `kali`.

### 2. Identifying the Hostname

**Command:**

```bash
hostname
```

**Purpose:**

The `hostname` command displays the name assigned to the computer or Linux system.

**Result:**

```text
kali
```

**Observation:**

The system hostname was identified as `kali`.

### 3. Checking the Current Working Directory

**Command:**

```bash
pwd
```

**Purpose:**

The `pwd` command stands for *print working directory*. It displays the full path of the directory in which the user is currently working.

**Result:**

```text
/home/kali
```

**Observation:**

The terminal was operating in the `/home/kali` directory, which is the home directory shown for the `kali` user.

### 4. Examining System Information

**Command:**

```bash
uname -a
```

**Purpose:**

The `uname -a` command displays detailed system identification information, including the kernel name, hostname, kernel release, kernel version, and hardware architecture.

**Observation:**

The assignment screenshot showed Kali Linux system information, including a kernel release of `6.19.14+kali-amd64` and an `x86_64` architecture.

This exercise demonstrated how Linux provides system and kernel information directly through the terminal.

### 5. Checking Filesystem Usage

**Command:**

```bash
df -h
```

**Purpose:**

The `df` command reports filesystem disk-space usage. The `-h` option displays the values in human-readable units, making the output easier to interpret.

The output includes information such as:

- Filesystem name
- Total filesystem size
- Used space
- Available space
- Percentage of space used
- Filesystem mount point

**Observation:**

The assignment included filesystem usage output. This exercise provided practice reading storage information and understanding how much space was used and available on mounted filesystems.

### 6. Checking System Uptime

**Command:**

```bash
uptime
```

**Purpose:**

The `uptime` command displays how long the system has been running. It can also show the number of logged-in users and system load averages.

**Observation:**

The command was used to inspect the system's runtime information and demonstrate another basic Linux administration utility.

### 7. Testing Network Connectivity to an IP Address

**Command:**

```bash
ping -c 2 8.8.8.8
```

**Purpose:**

The `ping` command tests whether a destination responds to ICMP echo requests. The `-c 2` option limits the test to two requests.

The destination `8.8.8.8` is a public IP address commonly associated with Google's public DNS service.

**Results recorded in the assignment:**

- Packets transmitted: 2
- Packets received: 2
- Packet loss: 0%
- Reported total test time: approximately 1002 milliseconds

**Observation:**

Both requests received responses, resulting in 0% packet loss during this test. This indicated that the destination was reachable from the system at the time the command was executed.

### 8. Testing Network Connectivity Using a Domain Name

**Command:**

```bash
ping -c 4 google.com
```

**Purpose:**

This command tests connectivity to a destination identified by a domain name rather than by manually entering an IP address.

The `-c 4` option sends four echo requests before terminating the command.

**Results recorded in the assignment:**

- Domain name: `google.com`
- Resolved IP address: `142.251.35.238`
- Packets transmitted: 4
- Packets received: 4
- Packet loss: 0%
- Reported total test time: approximately 3005 milliseconds
- Individual response times shown: approximately 25–29 milliseconds

**Observation:**

The domain name resolved to an IP address, and all four requests received responses. This demonstrated successful name resolution and network reachability during the test.

The response times and packet statistics represent the results captured in the assignment and may differ when the test is repeated.

## Results Summary

| Command | Purpose | Recorded Result |
|---|---|---|
| `whoami` | Identify current user | `kali` |
| `hostname` | Identify system hostname | `kali` |
| `pwd` | Display working directory | `/home/kali` |
| `uname -a` | Display system and kernel information | Kali Linux, `x86_64` architecture |
| `df -h` | Examine filesystem storage | Filesystem usage displayed |
| `uptime` | Check system runtime | Uptime information displayed |
| `ping -c 2 8.8.8.8` | Test connectivity to an IP address | 2 replies, 0% packet loss |
| `ping -c 4 google.com` | Test connectivity using a domain name | 4 replies, 0% packet loss |

## Key Learnings

### Linux Command-Line Fundamentals

I practiced using Linux commands to identify the current user, hostname, working directory, operating system, and system runtime information.

### System and Storage Monitoring

I learned how commands such as `uname -a`, `df -h`, and `uptime` can provide useful information about a Linux system.

### Network Connectivity Testing

I practiced using `ping` to determine whether a destination responds to network requests and to review packet loss and response times.

### IP Addresses and Domain Names

The assignment demonstrated the difference between testing connectivity using a numeric IP address and using a domain name. The domain-name test also illustrated how a hostname can resolve to an IP address through DNS.

### Technical Documentation

Recording terminal outputs and summarizing observations helped reinforce the importance of documenting practical work clearly and accurately.

## Conclusion

This assignment provided practical exposure to fundamental Linux commands and basic networking diagnostics in a Kali Linux environment.

By identifying system information, inspecting filesystem usage, checking uptime, and testing connectivity to `8.8.8.8` and `google.com`, I developed a stronger understanding of essential command-line operations.

These skills provide a foundation for further learning in Linux system administration, networking, troubleshooting, and cybersecurity.

## Skills Demonstrated

- Linux command-line usage
- System information gathering
- Basic filesystem monitoring
- Network connectivity testing
- DNS resolution concepts
- Interpretation of ping statistics
- Technical documentation and reporting

## Repository Structure

A suggested repository structure for this project is:

```text
10alytics-linux-fundamentals/
├── README.md
├── screenshots/
│   ├── system-information.png
│   ├── filesystem-usage.png
│   ├── ping-ip-address.png
│   └── ping-domain-name.png
└── assignment/
    └── assignment-1.pdf
```

The folder and screenshot names are suggestions. Replace them with the actual filenames you upload to GitHub.

## Disclaimer

This repository documents an educational Linux fundamentals assignment. The recorded results reflect the submitted assignment and are not guaranteed to match other systems or network conditions. The work documented here covers basic system inspection and connectivity testing, not a comprehensive security assessment or penetration test.
