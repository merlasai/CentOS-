#!/bin/bash

# Prompt user to enter a directory path
echo "Enter the directory path:"
read directory

# Check if the directory exists
if [ -d "$directory" ]; then
    # List files in the directory
    echo "Files in $directory:"
    ls "$directory"

    # Count the number of files in the directory
    file_count=$(ls -1 "$directory" | wc -l)
    echo "Total number of files: $file_count"
else
    echo "Directory not found!"
fi
