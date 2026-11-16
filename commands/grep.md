
# grep Command

The grep utility finds matching text in files and prints the matching lines.

## Sample Log File

The following examples use a file named `server.log` with this content:

    INFO Server started
    ERROR Database connection failed
    INFO User logged in
    WARNING Disk space is low
    ERROR Network timeout

The `grep` command searches for lines that match a specified pattern in one or more files.

## Sample Log File

The following examples use a file named `server.log` with this content:

    INFO Server started
    ERROR Database connection failed
    INFO User logged in
    WARNING Disk space is low
    ERROR Network timeout

## 1. Basic Search

Search for lines containing the word `ERROR`.

Command:

    grep "ERROR" server.log

Expected output:

    ERROR Database connection failed
    ERROR Network timeout

## 2. Case-Insensitive Search

Use `-i` to ignore uppercase and lowercase differences.

Command:

    grep -i "error" server.log

Expected output:

    ERROR Database connection failed
    ERROR Network timeout

## 3. Show Line Numbers

Use `-n` to display the line number of each matching line.

Command:

    grep -n "ERROR" server.log

Expected output:

    2:ERROR Database connection failed
    5:ERROR Network timeout

## 4. Count Matching Lines

Use `-c` to count the matching lines.

Command:

    grep -c "ERROR" server.log

Expected output:

    2

## 5. Invert the Search

Use `-v` to display lines that do not match the pattern.

Command:

    grep -v "INFO" server.log

Expected output:

    ERROR Database connection failed
    WARNING Disk space is low
    ERROR Network timeout
