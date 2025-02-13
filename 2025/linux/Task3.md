# Linux Log Analysis Guide

## **Task Overview**
Logs are crucial in DevOps! This guide helps you analyze logs using the `Linux_2k.log` file from LogHub (GitHub Repo).

## **Step 1: Download the Log File**
To download the log file, use:
```bash
wget https://raw.githubusercontent.com/LogHub/Linux_Logs/main/Linux_2k.log
```
Alternatively, you can clone the repository and navigate to the file.

## **Step 2: Extract Insights using Linux Commands**

### **Find all occurrences of the word "error"**
```bash
grep -i "error" Linux_2k.log
```
The `-i` flag makes the search case-insensitive.

### **Extract timestamps and log levels using `awk`**
Assuming the log format follows:
```
[TIMESTAMP] [LOG LEVEL] Message
```
Use the following command:
```bash
awk '{print $1, $2}' Linux_2k.log
```
This extracts and prints the timestamp and log level.

### **Replace all IP addresses with `[REDACTED]` using `sed`**
For security, replace IP addresses:
```bash
sed -E 's/[0-9]+\.[0-9]+\.[0-9]+\.[0-9]+/[REDACTED]/g' Linux_2k.log > sanitized_log.log
```
This will create a new file `sanitized_log.log` with IPs masked.

## **Bonus: Find the Most Frequent Log Entry**
```bash
awk '{print $0}' Linux_2k.log | sort | uniq -c | sort -nr | head -10
```
This counts occurrences of each log entry and displays the top 10 most frequent ones.

---
Now you have a clear workflow for analyzing Linux logs efficiently. 🚀
