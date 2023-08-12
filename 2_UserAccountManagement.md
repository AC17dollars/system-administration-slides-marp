---
marp: true
paginate: true
author: Abhinav Chalise, Saugat Neupane
headingDivider: 2
footer: 2023-08-13
header: Abhinav Chalise, Saugat Neupane
---

# User Account Management

## What is User Account Management (UAM)?

User Account Management (UAM) refers to the processes and tools used to create, modify, and manage user accounts on computer systems. It involves controlling user access, permissions, and privileges to various resources within the system.

## Root Account and User Account

- **Root Account:** The root account, often referred to as the superuser or administrator, has unrestricted access to the entire system. It holds the highest level of privilege and can perform any action on the system.

- **User Account:** A user account is a regular account used by individuals to interact with the system. User accounts have limited privileges and access based on their assigned permissions.

## User Access Control and its Necessity

User Access Control (UAC) is a security feature that restricts user privileges to prevent unauthorized access and potential harm to the system. It ensures that users only have access to resources and operations they are authorized to use. UAC is necessary to enhance system security and protect sensitive data from malicious activities.

### Example: chmod and chown Commands

Suppose we have an imaginary file directory named `documents` with a file called `report.txt`.

---

- `chmod`: This command is used to change file permissions.

  Example: `chmod 644 report.txt` (Read and write for the owner, and read-only for the group and others)

- `chown`: This command is used to change the ownership of files.

  Example: `chown user1:group1 report.txt` (Change the owner to `user1` and the group to `group1`)

## Adding and Removing Users

- **Adding a New User:** The `adduser` or `useradd` command is used to add a new user account.

  Example: `sudo adduser newuser` (Create a new user named `newuser`)

- **Removing a User:** The `deluser` or `userdel` command is used to remove a user account.

  Example: `sudo deluser newuser` (Remove the user account `newuser`)

---

### Groups

Groups are collections of user accounts that share common permissions and access rights to files and resources. They simplify user management by allowing administrators to assign permissions to a group instead of individual users.

## su Command

The `su` (switch user) command allows a user to temporarily switch to another user account, including the root account, by providing the respective password.

Example: `su - username` (Switch to the specified user account)

## sudo Command

The `sudo` (superuser do) command allows authorized users to execute commands as the root user or another user with elevated privileges. It provides a more controlled and secure way of performing administrative tasks.

Example: `sudo apt update` (Update package lists using elevated privileges)
