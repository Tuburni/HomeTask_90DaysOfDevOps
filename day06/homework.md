# 1. Creating a Simple File and Viewing Details

To create a simple file and view its details using the ls -ltr command:
>  <sub> _copy and past this comand to terminal_ </sub>
```bash
touch myfile.txt && ls -ltr myfile.txt
```
# 2. Changing User Permissions and Noting Changes

To change the user permissions of a file and observe the changes:
>  <sub> _copy and past this comand to terminal_ </sub>
```bash
chmod u+x myfile.txt && ls -ltr myfile.txt
```

_In this example, we added execute permission for the owner of the file. You can use u for the owner, g for the group, and o for others, along with + or - to add or remove permissions (+x adds execute permission, -x removes execute permission)._

# 3. Article about File Permissions

Title: Understanding Linux File Permissions and Ownership

Linux file permissions and ownership play a crucial role in maintaining the security and integrity of your system. Each file and directory on a Linux system has associated permissions that control who can read, write, and execute them. Additionally, these permissions are categorized into three main groups: owner, group, and others.

Owner Permissions:
The owner of a file or directory is the user who created it. The owner has the highest level of control over the file and can modify its permissions, change its ownership, and perform any actions on the file. Owner permissions include read (r), write (w), and execute (x).

Group Permissions:
Every file is associated with a group, and users who belong to that group have group-level permissions. Group permissions allow a set of users to access and manipulate files as a collective unit. Similar to owner permissions, group permissions include read, write, and execute.

Others Permissions:
The "others" category refers to all users who are not the owner of the file and do not belong to the group that owns the file. These permissions are applied to anyone who falls into this category. Others permissions also consist of read, write, and execute permissions.

Changing Permissions:
The chmod command is used to modify permissions for a file or directory. You can use the command with various options, such as u for the owner, g for the group, o for others, and + or - to add or remove permissions. For example, chmod u+x myfile.txt adds execute permission for the owner of the file.

Changing Ownership:
The chown command allows you to change the ownership of a file or directory. This can be useful when transferring files between users or reassigning ownership after system changes.

Access Control Lists (ACL):
While traditional permissions provide basic access control, ACLs offer more granular control over file access. ACLs allow you to define permissions for specific users or groups beyond the owner, group, and others categories. The getfacl and setfacl commands are used to manage ACLs.

In conclusion, understanding Linux file permissions and ownership is essential for maintaining the security and organization of your system. Properly configuring permissions ensures that users can access only what they need while keeping sensitive data secure.

# 4. Using ACL Commands
To use the getfacl and setfacl commands for Access Control Lists:
>  <sub> _copy and past this comand to terminal_ </sub>
```bash
sudo apt install acl && getfacl myfile.txt && setfacl -m u:username:r myfile.txt
```