1. Task 1: Creating Directories Using a Bash Script

Create a file named createDirectories.sh and add the following content:
>  <sub> _copy and past this comand to terminal_ </sub>
```bash
#!/bin/bash

if [ "$#" -ne 3 ]; then
    echo "Usage: $0 <directory_name> <start_number> <end_number>"
    exit 1
fi

directory_name=$1
start_number=$2
end_number=$3

for ((i=start_number; i<=end_number; i++)); do
    mkdir "${directory_name}${i}"
done
```

Make the script executable by running:
>  <sub> _copy and past this comand to terminal_ </sub>
```bash
chmod +x createDirectories.sh
```

Now you can execute the script with the desired arguments. For example:
>  <sub> _copy and past this comand to terminal_ </sub>
```bash
./createDirectories.sh day 1 90
```

2. Task 2: Creating a Backup Script

Create a file named backup.sh and add the following content:
>  <sub> _copy and past this comand to terminal_ </sub>
```bash
#!/bin/bash

backup_dir="/path/to/backup/directory" # Replace with your backup directory path

timestamp=$(date +"%Y%m%d%H%M%S")
backup_filename="backup_${timestamp}.tar.gz"

tar -czvf "${backup_dir}/${backup_filename}" /path/to/source/directory # Replace with your source directory path
```

Make the script executable:
>  <sub> _copy and past this comand to terminal_ </sub>
```bash
chmod +x backup.sh
```

You need to replace /path/to/backup/directory with the actual path where you want to store your backups and /path/to/source/directory with the actual path of the directory you want to back up.


3. Task 5: Display Usernames
To create users and display their usernames:
>  <sub> _copy and past this comand to terminal_ </sub>
```bash
# Create two users
sudo useradd user1
sudo useradd user2

# Display their usernames
echo "Usernames:"
echo "User 1: $(getent passwd user1 | cut -d ':' -f 1)"
echo "User 2: $(getent passwd user2 | cut -d ':' -f 1)"
```