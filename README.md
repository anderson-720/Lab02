## Lab 02

- Name: Ava Anderson 
- Email: anderson.720@wright.edu

## Part 1 Answers

Command to SSH to AWS instance:
```
ssh -i "C:\Users\denry\Downloads\labsuser (1).pem" ubuntu@52.7.228.64
```

## Part 2 Answers

1. `chmod u+r bubbles.txt`
    - Means: Allows the user/owner of the file to be able to read the file bubbles.txt
2. `chmod u=rw,g-w,o-x banana.cabana`
    - Means: Allows the user/owner of the file to be able to read and write in the file banana.cabana, while removing the group's ability to write in the file and other users' ability to execute the file
3. `chmod a=w snow.md`
    - Means: Sets the file permissions so all users (owner, group, and others) all are able to write in the file snow.md
4. `chmod 751 program`
    - Means: Allows the owner of the file to read, write and execute the file (7), the group to read and execute the file (5), and others to only execute it (1)
5. `chmod -R ug+w share`
    - Means: The user and group are now able to write in the all of the files inside of the folder share (-R lets this permission go to every file in the folder)

## Part 3 Answers

1. Command to create new user: sudo adduser aanderson
2. Path to user's home directory: /home/aanderson
3. Evaluate if `ubuntu` can add files to user's home directory: ubunto cannot add files to my home directory, I tried to add a file by doing "touch /home/aanderson/deer" and it denied my access to make the file
4. Command to switch to user: su - aanderson
5. Command(s) to go to user's home directory: pwd
6. Evaluate if user can add files to user's home directory: I can add files to my home directory. I did the same command as #3 and it did not give me an error message, and the file deer shows up when I do the ls command
7. Command to switch to `ubuntu`: "exit" takes me out of my user and back to the defauly ubuntu
8. Command to return to `ubuntu` home directory: pwd

## Part 4 Answers

For each, write the command used or answer the question posed.

1. Command to create group named `crew`: sudo addgroup crew
2. Command(s) to add `ubuntu` & user to group `crew`: sudo usermod -aG crew ubuntu & sudo usermod -aG crew aanderson
3. Command to modify `share` to have group ownership of `crew`: sudo chgrp -R crew /home/ubuntu/share & sudo chmod -R g+w /home/ubuntu/share
4. Command to switch to user: sudo su - aanderson
5. Command to add file to `share`: touch /home/ubuntu/share/doe.txt
6. Evaluate why these steps allowed the above action: A group was created with my account and ubuntu and the permission to write and read the files, so I was able to create a file in the folder since I am in the group

## Part 5 Answers

For each, write the command used or answer the question posed.

1. Command to create file using `sudo`: sudo touch /home/ubuntu/sudowho.txt
2. Evaluate (in plain text) the permission of the file: -rw-r--r-- 1 root root
3. Provide a method to edit the file without modifying permissions: sudo nano /home/ubuntu/sudowho.txt
4. Command(s) to modify permissions: sudo chown ubuntu:crew /home/ubuntu/sudowho.txt

Finished this a couple hours late, ended up taking me much longer than I think but I got it done :,)
