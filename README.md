# Basics-Linux-for-Robotics
understand Linux file permissions and their structure. Includes a flowchart that simplifies the process of analyzing file permissions and demonstrates how to use the chmod command to modify permissions. A practical example is provided by applying chmod to a Python file, setting its permissions to rwxrwxr-x.

## **Overview**
The purpose of this repository is to:
- Demonstrate the basics of Linux file permissions.
- Show how to analyze and modify permissions using `chmod`.
  
## **Steps Covered**

### **1. File Permissions Basics**
- File permissions in Linux are categorized for:
  - **Owner**: The user who owns the file.
  - **Group**: Users in the same group as the owner.
  - **Others**: Everyone else.
- Permissions include:
  - `r` (read): Permission to read the file.
  - `w` (write): Permission to modify the file.
  - `x` (execute): Permission to execute the file (if it's a script or program).

### **2. Commands Used**
#### **Creating a File**
`touch my_file.txt`
`nano my_script.py`

### **3. Checking File Permissions**
To display the permissions of files:
`ls -l`

### **4. Changing File Permissions**
To set permissions to rwxrwxr-x (read, write, execute for owner and group, and read, execute for others):
`chmod 775 my_script.py`

### **5. Changing Ownership**
To change the file owner and group:
`sudo chown travis:travismedia my_file.txt`

### **6. Running a Python Script**
To execute the Python script:
`python3 my_script.py`

### **Examples**
#### **Before Changing Permissions**
`-rw-r--r-- 1 sarah sarah 15 Jan 6 14:55 my_script.py`
#### **After Changing Permissions**
`-rwxrwxr-x 1 sarah sarah 15 Jan 6 14:55 my_script.py`

### **Error Handling**
1.chown: invalid group
  Ensure the group exists or create it:
  `sudo groupadd travismedia`
2.File not found:
  Ensure the file exists in the current directory:
  `ls -l`

## **Flowchart**
The flowchart illustrates the steps to understand and modify file permissions

