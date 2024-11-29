
# Linux Fundamentals Command Guide

## File System Navigation

1. **`ls ~/`**
   - **Description**: Lists the contents of the home directory.
   - **Example**:
     ```bash
     ls ~/
     ```
        ![Screenshot - ls home](screenshots/ls-home.png)

2. **`cd /var/log && ls`**
   - **Description**: Changes the current directory to `/var/log` and lists its contents.
   - **Example**:
     ```bash
     cd /var/log && ls
     ```
        ![Screenshot - cd and ls](screenshots/cd-ls.png)

3. **`which bash`**
   - **Description**: Finds and displays the path to the bash executable.
   - **Example**:
     ```bash
     which bash
     ```
        ![Screenshot - which bash](screenshots/which-bash.png)

4. **`echo $SHELL`**
   - **Description**: Displays the current shell being used.
   - **Example**:
     ```bash
     echo $SHELL
     ```
        ![Screenshot - find shell](screenshots/find-shell.png)

## File and Directory Operations

1. **`mkdir ~/linux_fundamentals`**
   - **Description**: Creates a directory named `linux_fundamentals` in your home directory.
   - **Example**:
     ```bash
     mkdir ~/linux_fundamentals
     ```
        ![Screenshot - mkdir linux fundamentals](screenshots/mkdir-linux-fundamentals.png)

2. **`mkdir ~/linux_fundamentals/scripts`**
   - **Description**: Creates a subdirectory named `scripts` inside `linux_fundamentals`.
   - **Example**:
     ```bash
     mkdir ~/linux_fundamentals/scripts
     ```
        ![Screenshot - mkdir scripts](screenshots/mkdir-scripts.png)

3. **`touch ~/linux_fundamentals/example.txt`**
   - **Description**: Creates an empty file named `example.txt` inside the `linux_fundamentals` directory.
   - **Example**:
     ```bash
     touch ~/linux_fundamentals/example.txt
     ```
        ![Screenshot - touch example](screenshots/touch.png)

4. **`cp ~/linux_fundamentals/example.txt ~/linux_fundamentals/scripts/`**
   - **Description**: Copies `example.txt` to the `scripts` directory.
   - **Example**:
     ```bash
     cp ~/linux_fundamentals/example.txt ~/linux_fundamentals/scripts/
     ```
        ![Screenshot - copy example](screenshots/copy.png)

5. **`mkdir ~/linux_fundamentals/backup && mv ~/linux_fundamentals/example.txt ~/linux_fundamentals/backup/`**
   - **Description**: Moves `example.txt` from `linux_fundamentals` to `linux_fundamentals/backup`.
   - **Example**:
     ```bash
     mkdir ~/linux_fundamentals/backup && mv ~/linux_fundamentals/example.txt ~/linux_fundamentals/backup/
     ```
        ![Screenshot - move example](screenshots/move.png)

6. **`chmod 644 ~/linux_fundamentals/backup/example.txt`**
   - **Description**: Changes the permissions of `example.txt` to read and write for the owner, and read-only for the group and others.
   - **Example**:
     ```bash
     chmod 644 ~/linux_fundamentals/backup/example.txt
     ```
        ![Screenshot - chmod example](screenshots/chmod-example.png)

7. **`ls -l ~/linux_fundamentals/backup/example.txt`**
   - **Description**: Verifies the permission changes.
   - **Example**:
     ```bash
     ls -l ~/linux_fundamentals/backup/example.txt
     ```
        ![Screenshot - ls permissions](screenshots/ls-permissions.png)

## File Modification

1. **`touch ~/example.txt`**
   - **Description**: Creates a file named `example.txt` in your home directory.
   - **Example**:
     ```bash
     touch ~/example.txt
     ```
        ![Screenshot - touch example](screenshots/touch-example.png)

2. **`sudo chown student ~/example.txt`**
   - **Description**: Changes the owner of `example.txt` to a user named `student`.
   - **Example**:
     ```bash
     sudo chown student ~/example.txt
     ```
        ![Screenshot - chown example](screenshots/chown.png)

3. **`sudo chgrp students ~/example.txt`**
   - **Description**: Changes the group of `example.txt` to a group named `students`.
   - **Example**:
     ```bash
     sudo chgrp students ~/example.txt
     ```
        ![Screenshot - chgrp example](screenshots/chgrp.png)

4. **`ls -l ~/example.txt`**
   - **Description**: Verifies the changes using appropriate commands.
   - **Example**:
     ```bash
     ls -l ~/example.txt
     ```
        ![Screenshot - ls permissions](screenshots/user-and-group-permissions.png)

## Ownership

1. **`mkdir ~/project`**
   - **Description**: Creates a directory named `project` in your home directory.
   - **Example**:
     ```bash
     mkdir ~/project
     ```
        ![Screenshot - mkdir project](screenshots/mkdir-project.png)

2. **`touch ~/project/report.txt`**
   - **Description**: Creates a file named `report.txt` inside the `project` directory.
   - **Example**:
     ```bash
     touch ~/project/report.txt
     ```
        ![Screenshot - touch report](screenshots/touch-report.png)

3. **`chmod 644 ~/project/report.txt`**
   - **Description**: Sets the permissions of `report.txt` to read and write for the owner, and read-only for the group and others.
   - **Example**:
     ```bash
     chmod 644 ~/project/report.txt
     ```
        ![Screenshot - chmod report](screenshots/chmod-report.png)

4. **`chmod 755 ~/project`**
   - **Description**: Sets the permissions of the `project` directory to read, write, and execute for the owner, and read and execute for the group and others.
   - **Example**:
     ```bash
     chmod 755 ~/project
     ```
        ![Screenshot - chmod project](screenshots/chmod-project.png)

5. **`ls -l ~/project`**
   - **Description**: Verifies the changes using appropriate commands.
   - **Example**:
     ```bash
     ls -l ~/project
     ```
        ![Screenshot - ls project](screenshots/ls-project.png)

## User Add/Modify

1. **`sudo useradd -m developer`**
   - **Description**: Creates a new user named `developer` with a home directory and shell.
   - **Example**:
     ```bash
     sudo useradd -m developer
     ```
        ![Screenshot - useradd developer](screenshots/useradd-developer.png)

2. **`sudo useradd -m -d /home/developer_home developer`**
   - **Description**: Set the home derectory of user `developer` to `developer_home`.
   - **Example**:
     ```bash
     sudo usermod -m -d /home/developer_home developer
     ```
        ![Screenshot - useradd developer](screenshots/developer-home.png)

3. **`sudo usermod -s /bin/bash developer`**
   - **Description**: Changes the shell of the user `developer` to `bash` from  `sh`.
   - **Example**:
     ```bash
     sudo usermod -s /bin/bash developer
     ```
        ![Screenshot - usermod devuser](screenshots/bin-bash.png)

4. **`grep developer /etc/passwd`**
   - **Description**: Verify details of user `developer`.
   - **Example**:
     ```bash
     grep developer /etc/passwd
     ```
        ![Screenshot - usermod devuser](screenshots/user-details.png)

5. **`sudo usermod -l devuser developer`**
   - **Description**: Change the username `developer` to `devuser`.
   - **Example**:
     ```bash
     sudo usermod -l devuser developer
     ```
        ![Screenshot - usermod devuser](screenshots/usermod-devuser.png)

6. **`sudo usermod -aG devgroup devuser`**
   - **Description**: Adds `devuser` to a group named `devgroup`.
   - **Example**:
     ```bash
     sudo usermod -aG devgroup devuser
     ```
        ![Screenshot - usermod group](screenshots/usermod-group.png)

7. **`sudo passwd devuser`**
   - **Description**: Sets the password of `devuser` to `devpass`.
   - **Example**:
     ```bash
     sudo passwd devuser
     ```
        ![Screenshot - passwd devuser](screenshots/passwd-devuser.png)

## Hard/Soft Link

1. **`touch ~/original.txt`**
   - **Description**: Creates a file named `original.txt` in the home directory.
   - **Example**:
     ```bash
     touch original.txt
     ```
        ![Screenshot - ln softlink](screenshots/original-file.png)

2. **`ln -s ~/original.txt ~/softlink.txt`**
   - **Description**: Creates a symbolic link named `softlink.txt` pointing to `original.txt`.
   - **Example**:
     ```bash
     ln -s ~/original.txt ~/softlink.txt
     ```
        ![Screenshot - ln softlink](screenshots/ln-softlink.png)

3. **`rm ~/original.txt && ls`**
   - **Description**: Removes the original.txt file and `ls` shows the link is broken.
   - **Example**:
     ```bash
     rm ~/original.txt && ls
     ```
        ![Screenshot - ln softlink](screenshots/rm-original.png)

4. **`ln ~/datafile.txt ~/hardlink.txt`**
   - **Description**: Creates a hard link named `hardlink.txt` pointing to `datafile.txt`.
   - **Example**:
     ```bash
     ln ~/datafile.txt ~/hardlink.txt
     ```
        ![Screenshot - ln hardlink](screenshots/ln-hardlink.png)

3. **`find ~ -name "*.txt"`**
   - **Description**: Finds all `.txt` files in your home directory.
   - **Example**:
     ```bash
     find ~ -name "*.txt"
     ```
        ![Screenshot - find txt](screenshots/find-txt.png)

## Package Installation

1. **`sudo apt update`**
   - **Description**: Updates the repository cache using `apt`.
   - **Example**:
     ```bash
     sudo apt update
     ```
        ![Screenshot - apt update](screenshots/apt-update.png)

2. **`sudo apt install tree`**
   - **Description**: Installs a package named `tree`.
   - **Example**:
     ```bash
     sudo apt install tree
     ```
        ![Screenshot - apt install tree](screenshots/tree.png)

3. **`google-cloud-cli`**
   - **Description**: Installs the Google Cloud CLI tool using `apt` with all the prerequisite.
   - **Example**:
     ```bash
     sudo apt upadte && \
     sudo apt install -y apt-transport-https ca-certificates gnupg curl && \
     curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo gpg --dearmor -o /usr/share/keyrings/cloud.google.gpg && \
     echo "deb [signed-by=/usr/share/keyrings/cloud.google.gpg] https://packages.cloud.google.com/apt cloud-sdk main" | sudo tee -a /etc/apt/sources.list.d/google-cloud-sdk.list && \
     sudo apt update && \
     sudo apt install -y google-cloud-cli
     ```
        ![Screenshot - apt install gcloud](screenshots/gcloud.png)

