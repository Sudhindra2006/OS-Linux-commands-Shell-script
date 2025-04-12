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
![image](https://github.com/user-attachments/assets/cef6d243-9332-4ec8-a9d4-26db2406a2ef)




cat < file2
## OUTPUT
![image](https://github.com/user-attachments/assets/3009b1e9-f3aa-4357-9481-e78c49b4149b)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![image](https://github.com/user-attachments/assets/c39534d6-93cf-437b-923b-72a7baabfe3e)

comm file1 file2
 ## OUTPUT
![image](https://github.com/user-attachments/assets/76536443-1e7e-4398-8028-3e4b5394ab98)

 
diff file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/e5a5a113-0b81-4bde-b9d6-55d2c715e458)



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
![image](https://github.com/user-attachments/assets/811e07c9-6745-4bbe-9a43-7b2aa23c7f25)



cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/633d5e24-3dc6-42ff-b514-4ec5978d32bf)



cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/4f5fe21a-3e58-42ec-a8b9-7d5029bf71e0)


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/774c5947-df97-4883-a52d-6560ba5c1441)


grep hello newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/15b47bf6-8384-47b9-89bd-97f3fbfc819f)



grep -v hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/1aed6f12-c510-4e95-9e4c-1bbe95a13b6c)



cat newfile | grep -i "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/32008397-521a-4d0d-8ac4-8dc0150131b1)




cat newfile | grep -i -c "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/4b7b619d-727a-44b4-a0cb-7d641e793ccc)




grep -R ubuntu /etc
## OUTPUT
![image](https://github.com/user-attachments/assets/4250737b-c783-4192-a3d9-c9d0d1a674a9)



grep -w -n world newfile   
## OUTPUT
![image](https://github.com/user-attachments/assets/6b1f1ecf-5f40-46e4-b2b1-fa93a68e34e4)


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
egrep -w 'Hello|hello' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/2473da24-69ab-4a70-a488-1a7734239551)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/8819f059-438b-4da4-ba12-80d3565e8176)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/408fb497-8d19-44ca-af2b-235d6232e6ec)



egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/484c4b42-d29c-4f10-8128-9385923802ca)



egrep '(world$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/75ebd61b-2f05-4fc7-b1c2-0076ad2d1c20)



egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/e9a3ee8d-1625-46ef-a3f1-432adaf17b9c)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/466bf5e8-10b6-46a7-a072-a665e8f6a0af)



egrep '[1-9]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/27f2836a-ce57-494a-b2e0-5a2468c5655c)


egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/7876d03d-8aac-4b04-8e0b-a76a45182bf2)


egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/9ebe83b8-4321-42df-8fe0-700fd059dc3f)


egrep l{2} newfile
## OUTPUT
![image](https://github.com/user-attachments/assets/8434cea2-17b8-4835-94c4-7d56a3b2e219)



egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/user-attachments/assets/072ec332-44cd-40a2-b927-91e6d3ae3d62)


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
![image](https://github.com/user-attachments/assets/5c51c0ac-f681-434d-8144-7ffdfe9e998d)



sed -n -e '$p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/df8704ab-30d7-4214-8ba4-0fe19647d80c)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/af2006d4-4cd0-41cb-9f03-5af4239e8027)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/4a57df98-b8f9-40ba-96b0-688f4253ad57)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/0b528832-e90b-46ac-a088-9f6f3b055cab)



sed -n -e '1,5p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/6fefea1f-cbd3-4c4e-babf-87ffcb776ba1)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/4d47b68a-4a9d-4b5b-9762-b3e098804ac0)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/32d4001f-95bd-46b3-bc16-4c3a95f5f812)



seq 10 
## OUTPUT

![image](https://github.com/user-attachments/assets/53b7f998-b495-4fd0-a063-2b725386f9a1)


seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/user-attachments/assets/1b7c2586-c926-4575-b96f-b2909d67410a)



seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/user-attachments/assets/b9cf0896-c0c4-438b-a54d-6b3072c105ad)



seq 3 | sed '2a hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/3de556aa-b595-4846-94da-c678f78220b1)



seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/51e19214-1527-466c-8453-4b76b8f89ff0)



seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/eef60eac-5a0b-4702-b36d-1084fd11e5ca)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/736c8653-c146-4bcb-935d-0608fc442651)


sed -n '2,4{s/$/*/;p}' file23
![image](https://github.com/user-attachments/assets/75667ff0-dfe4-4815-99ce-f1d3f20b99c2)


#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT
![image](https://github.com/user-attachments/assets/46387148-1b3c-4de3-b66a-1ac6f8d4febd)


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT
![image](https://github.com/user-attachments/assets/61209adf-7c1a-4f46-a835-56b4f07338a9)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/user-attachments/assets/5f6b2efe-4d45-4919-99a3-2ff71a9cdfd6)

cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT
![image](https://github.com/user-attachments/assets/82f1cfb1-885a-4dcf-aa0a-5306e251de6b)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image](https://github.com/user-attachments/assets/a37b2b3c-d24c-415f-8aaf-5254f32c86bd)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![image](https://github.com/user-attachments/assets/e4b4d519-8ede-4d74-adbd-0d238f5dc992)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/dc7c38e5-41f8-40ec-ae81-b851609de216)


tar -xvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/34f1deef-5b00-421f-9d2b-d4a90d092235)

gzip backup.tar

ls .gz
## OUTPUT
![image](https://github.com/user-attachments/assets/0f619887-e86d-473f-a3aa-798e57b1a8e2)

gunzip backup.tar.gz
## OUTPUT
![image](https://github.com/user-attachments/assets/2a3b692e-8a3d-4874-b6b6-cbbb273999e3)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![image](https://github.com/user-attachments/assets/affe51e9-2ae5-4a8d-847c-afcd42ab2593)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![image](https://github.com/user-attachments/assets/3a9f0b50-34dc-4351-89d1-d703f6cfdf47)


cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT
![image](https://github.com/user-attachments/assets/c313ddc2-cb12-4ba5-9545-d2c69f802f23)

 
ls file1
## OUTPUT
![image](https://github.com/user-attachments/assets/79d5c96d-10f9-4240-885e-648a425fb386)

echo $?
## OUTPUT
![image](https://github.com/user-attachments/assets/7c969b5b-48f4-45f7-8c33-e96481e7ea88)


./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
![image](https://github.com/user-attachments/assets/11771454-c6de-4d10-9cc8-81d64fd3aa33)

abcd
 
echo $?
 ## OUTPUT

![image](https://github.com/user-attachments/assets/17dd87b8-6a17-49a7-8ab1-dc7f4dc03c69)


 
# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
##OUTPUT

![image](https://github.com/user-attachments/assets/7122813c-e5b4-4e6d-a102-e048de5ce8ee)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/30834129-85c3-4b28-b02c-1cdefbab8f3b)


# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT
![image](https://github.com/user-attachments/assets/1049f553-1f75-42ad-97ff-2702691dddd0)

# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
## OUTPUT

![image](https://github.com/user-attachments/assets/c01854ae-afee-4cbe-b976-69bc3d645bfd)


# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT
![image](https://github.com/user-attachments/assets/0040449b-527a-4c11-a896-8dd410944f81)

# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```

cat ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT
![image](https://github.com/user-attachments/assets/4ecf2fd4-cbe9-4864-8269-ad391e72cb3c)

# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/1154ffc4-8d78-49c4-ac99-af99a30cb955)


# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/5b600886-beb6-46dc-881f-a5f5bbed2ba1)

# using the case command
cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
![image](https://github.com/user-attachments/assets/f00de214-df9f-436a-a577-9cc750fd3e56)

 
cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
![image](https://github.com/user-attachments/assets/471008bc-cdeb-4865-8b60-ea19f65a6245)

 
cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
 ![image](https://github.com/user-attachments/assets/728176a5-7499-436c-ae4b-85c9bbbd1480)

 
 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
![image](https://github.com/user-attachments/assets/27597aac-dc05-4653-9cc4-76f601508d93)

 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
![image](https://github.com/user-attachments/assets/88ce5ac6-b8c6-49a2-a7b1-e2933831738e)

cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh
 
$ ./forin2.sh 
![image](https://github.com/user-attachments/assets/48c6c40e-b57c-4aa5-ade7-e12e8cb559c5)

cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
![image](https://github.com/user-attachments/assets/a95b1c9e-25fd-4821-97d4-a210ea0e2b92)

cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT

cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ chmod 777 forinfile.sh
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT


cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/ab613730-9918-44f8-a0f0-e3b5f534f1a9)


cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/80d1852b-eb30-4682-9068-690e3c4d83bd)

cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT
![image](https://github.com/user-attachments/assets/ae814ab4-2a64-45b3-9141-332274573f9e)

 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```
## OUTPUT
![image](https://github.com/user-attachments/assets/0e408750-9b70-4175-b925-f324c6190e19)

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/4f4e2189-0341-4279-9c3c-fce7b78c1670)

cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/1ea68b5c-983d-4af5-80d5-f221632e9b9c)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
![image](https://github.com/user-attachments/assets/44d907b1-a621-4908-9132-6dbd5ecd8069)



$ ./exread1.sh 
 
cat funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
## OUTPUT
 ./funcex.sh 
![image](https://github.com/user-attachments/assets/415f42a7-4c3b-4074-9547-cb8c9f4a538b)

 
 ./funcex.sh 1 2
![image](https://github.com/user-attachments/assets/e465a9cc-806d-4d66-8c8c-fc9ea4f24774)

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
$ ./argshift.sh 1 2 3
![image](https://github.com/user-attachments/assets/31b4f38a-ff53-4c0d-b43a-074b5bfe638f)

 
 cat argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
## OUTPUT
![image](https://github.com/user-attachments/assets/b6507ba7-cfa7-4b14-88f8-e8e5932b72c9)

$ ./argshift.sh 1 2 3
 
cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
## OUTPUT
 ./argshift.sh 1 2 3
 ![image](https://github.com/user-attachments/assets/75e6e794-70f0-4ce2-a0cf-eb03a329f65a)

 
cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
## OUTPUT 
![image](https://github.com/user-attachments/assets/ed44808c-eaaf-43c2-bcb4-b2b38466fd37)

cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 
![image](https://github.com/user-attachments/assets/fbe0a119-0cd2-4ebb-80b9-880b698a41d5)


# RESULT:
The Commands are executed successfully.
