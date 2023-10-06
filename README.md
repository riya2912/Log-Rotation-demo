# Log-Rotation-demo

**Overview**

This Bash script is designed to perform log rotation and backup for a specific log file. It renames the existing log file with a timestamp, creates a new empty log file, compresses the old log file, and moves the compressed log file to a backup directory. The script is intended to run continuously, rotating and backing up logs every hour.

**Usage**

To use this script, follow these steps:

1. Configuration: Before running the script, configure the following variables according to your requirements:

  - `log_dir`: The directory where the log file to be rotated is located.
  - `backup_dir`: The directory where compressed log files will be stored as backups.
  - `one_hour`: The timestamp format used for log file rotation.

2. Execution: Run the script using following command:

   `sh log_rotation_backup.sh`


**How It Works**

It checks if the log file to be rotated exists in the specified `log_dir`.

If the log file exists, it renames the existing log file with a timestamp to keep a historical record.

It creates a new empty log file with the same name as the original.

The old log file is compressed using `gzip` command.

The compressed log file is moved to the specified `backup_dir`.

The script repeats this process every hour, continuously rotating and backing up logs.
