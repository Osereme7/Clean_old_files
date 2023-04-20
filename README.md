# Clean_old_files
This script is a Bash script that deletes old files from a specified directory. 
The script first defines the directory where the files to be deleted are stored. 
It then sets the date format to ISO 8601 and calculates the cutoff date for file deletion,
which is 90 days prior to the current date.
The script then loops through all the files in the specified directory and extracts the date from each file name. 
It checks if the date is valid by matching it to the defined date format.
If the date is valid, the script converts the date to a Unix timestamp and checks if the file is older than 90 days from the cutoff date. 
If the file is older, the script deletes the file from the directory.
If the date in the file name does not match the defined date format, the script checks for an alternate date format. 
If the alternate format is found, the script follows the same procedure to delete the old files.
If neither the defined format nor the alternate format is found in the file name, 
the script skips the file and prints a debugging message indicating that the filename format is invalid.
