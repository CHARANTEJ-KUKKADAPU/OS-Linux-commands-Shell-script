# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
cat < file1
## OUTPUT
<img width="231" height="72" alt="image" src="https://github.com/user-attachments/assets/36783e21-dfc6-4d2e-bbf8-f594d40950ad" />



cat < file2
## OUTPUT


<img width="171" height="82" alt="image" src="https://github.com/user-attachments/assets/7301da47-5873-4c7c-88ef-a8d04c7c227b" />


# Comparing Files
cmp file1 file2
## OUTPUT



 <img width="328" height="135" alt="image" src="https://github.com/user-attachments/assets/53e6b2b7-f4e3-45c0-bd67-dea8b2c2d63e" />

comm file1 file2
 ## OUTPUT

 <img width="207" height="130" alt="image" src="https://github.com/user-attachments/assets/66fb50c4-1f65-4d9a-aa1e-23c9d408f88b" />

diff file1 file2
## OUTPUT


#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```


cut -c1-3 file11
## OUTPUT

<img width="273" height="58" alt="image" src="https://github.com/user-attachments/assets/b9643a4f-f132-4665-bca3-1790404afa11" />



cut -d "|" -f 1 file22
## OUTPUT
<img width="21" height="43" alt="image" src="https://github.com/user-attachments/assets/5af72c32-07c4-4268-97b2-f6c25933d04d" />

cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world



 <img width="167" height="42" alt="image" src="https://github.com/user-attachments/assets/afae5a8c-be1b-436e-ba84-082002e60be1" />

grep Hello newfile 
## OUTPUT

<img width="322" height="42" alt="image" src="https://github.com/user-attachments/assets/9c1052e9-d376-4eef-9702-9a15159cba36" />


grep hello newfile 
## OUTPUT

<img width="322" height="42" alt="image" src="https://github.com/user-attachments/assets/c925851d-170a-4a58-93f4-dfd099ba2b11" />



grep -v hello newfile 
## OUTPUT

<img width="272" height="52" alt="image" src="https://github.com/user-attachments/assets/1dab4c49-a312-4eb8-bbf4-f5d154b594b1" />


cat newfile | grep -i "hello"
## OUTPUT


<img width="338" height="61" alt="image" src="https://github.com/user-attachments/assets/cf4c0731-35bf-47af-9c4c-6dfea5187554" />


cat newfile | grep -i -c "hello"
## OUTPUT


<img width="382" height="42" alt="image" src="https://github.com/user-attachments/assets/98daad91-e77f-46cd-8877-25dd7fdfdaf0" />


grep -R ubuntu /etc
## OUTPUT

<img width="692" height="177" alt="image" src="https://github.com/user-attachments/assets/7a358585-f5c8-4b4f-9924-b4825c2ffc86" />


grep -w -n world newfile   
## OUTPUT

<img width="285" height="60" alt="image" src="https://github.com/user-attachments/assets/551b0e70-08b1-48d9-ba89-b7d87158a225" />


cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```



egrep '(world$)' newfile 
## OUTPUT

<img width="411" height="75" alt="image" src="https://github.com/user-attachments/assets/d0f267a5-c77c-4de2-85f4-3fc58d367f97" />


egrep '(World$)' newfile 
## OUTPUT
<img width="411" height="75" alt="image" src="https://github.com/user-attachments/assets/3a1a0f95-2d75-4c6b-a265-736c8bc51f2b" />


egrep '((W|w)orld$)' newfile 
## OUTPUT


<img width="411" height="75" alt="image" src="https://github.com/user-attachments/assets/9d93126f-e0b2-4e96-82c1-0756509396a7" />

egrep '[1-9]' newfile 
## OUTPUT


<img width="391" height="53" alt="image" src="https://github.com/user-attachments/assets/7719df64-3978-467b-9385-878ae459ca17" />

egrep 'Linux.*world' newfile 
## OUTPUT

<img width="347" height="46" alt="image" src="https://github.com/user-attachments/assets/b51c5cfe-e825-4b42-b9b7-fecea02d0046" />



egrep l{2} newfile
## OUTPUT

<img width="355" height="67" alt="image" src="https://github.com/user-attachments/assets/fe3a008e-0060-40a8-b9f5-8acccabf580e" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="355" height="67" alt="image" src="https://github.com/user-attachments/assets/a32a7c0c-ade2-4f7a-97a0-885b157b00f8" />


cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```


sed -n -e '3p' file23
## OUTPUT


<img width="238" height="40" alt="image" src="https://github.com/user-attachments/assets/179b9cd7-5349-439e-8a92-dc9ef3036c58" />

sed -n -e '$p' file23
## OUTPUT

<img width="241" height="42" alt="image" src="https://github.com/user-attachments/assets/003eeed9-5cf1-4609-b0ef-6ddd29757bb2" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="230" height="127" alt="image" src="https://github.com/user-attachments/assets/4206cd60-aa35-4ae1-9a01-28b159b61daf" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="208" height="133" alt="image" src="https://github.com/user-attachments/assets/e9a89428-2157-409e-87b5-7979e773cc75" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="240" height="107" alt="image" src="https://github.com/user-attachments/assets/8150bdcd-54fc-47a9-8532-5902b8705b1c" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="303" height="96" alt="image" src="https://github.com/user-attachments/assets/ddef2b60-d5b0-434a-8d53-0a6420829781" />


sed -n -e '2,/Joe/p' file23
## OUTPUT


<img width="257" height="61" alt="image" src="https://github.com/user-attachments/assets/3bb2cbd9-5e05-4048-b78c-1583533d2e4d" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT


<img width="292" height="52" alt="image" src="https://github.com/user-attachments/assets/d37ab374-2284-4610-8b47-926baa031eab" />

seq 10 
## OUTPUT

<img width="283" height="151" alt="image" src="https://github.com/user-attachments/assets/e6d6bb0c-48b6-43ed-99a7-1859bbb82f1f" />



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="291" height="67" alt="image" src="https://github.com/user-attachments/assets/5500364e-12a1-4c10-8df9-c949b53b9aa5" />


seq 10 | sed -n '2,~4p'
## OUTPUT


<img width="278" height="62" alt="image" src="https://github.com/user-attachments/assets/8d9832d2-ab33-4be9-b012-d93f5ddb153e" />

seq 3 | sed '2a hello'
## OUTPUT
<img width="262" height="61" alt="image" src="https://github.com/user-attachments/assets/ce4f1fbf-6046-4070-9791-a6046ba4a018" />



# RESULT:
The Commands are executed successfully.
