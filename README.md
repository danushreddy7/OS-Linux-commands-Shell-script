Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting
## REWG NO: 212223040029
# NAME: T DANUSH REDDY
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
![image](https://github.com/user-attachments/assets/1fbe0bc5-8ddd-4e92-8cb5-33b0e3983594)





cat < file2
## OUTPUT
![image](https://github.com/user-attachments/assets/ae86eb06-f30b-4f52-b6ca-5f2271ee9305)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![image](https://github.com/user-attachments/assets/db84d2e8-d446-42ab-9d5f-65e8dbd6fc19)

comm file1 file2
 ## OUTPUT
![image](https://github.com/user-attachments/assets/8690da20-fcf2-4e13-a1c5-4b9fc2de689d)

 
diff file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/dfc5b724-1270-4729-8d87-7296714475c9)


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
![image](https://github.com/user-attachments/assets/a44ccdfc-93fe-4cad-966c-dbb312fc5fd4)




cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/e313b8ac-7043-4b85-93b4-d5a6daf9fee3)



cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/c8899f81-aa40-49fd-af8a-09e62ac45aa1)


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
![image](https://github.com/user-attachments/assets/b76bae3e-227f-4a61-845a-616a8872fece)



grep hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/2dd9326d-f30f-4f24-853b-4e662a2a91e0)





grep -v hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/f8f1ed2a-63a7-4469-9db6-91a87ef1d8ec)



cat newfile | grep -i "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/361d1e01-2b9a-4f71-890b-caae6b84af66)




cat newfile | grep -i -c "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/2f6fad98-6246-4860-a6e9-fb99d037e12e)




grep -R ubuntu /etc
## OUTPUT
![image](https://github.com/user-attachments/assets/83db9dc7-1eae-425e-b2d9-c196bc6c2183)



grep -w -n world newfile   
## OUTPUT
![image](https://github.com/user-attachments/assets/8bb95900-58d4-47ee-ac41-d04f6be39915)



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
![image](https://github.com/user-attachments/assets/520a62b2-e48a-419a-a7c9-46fd0d2eaec1)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/a7915a73-4f1b-4676-9a06-88cd16f34ebc)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/a12ecbc1-1a01-4c61-842c-98a5e25ad87e)




egrep '(^hello)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/92fbd70c-94bf-4de4-a1a8-f2b1c5ac312e)


egrep '(world$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/6b5d2bc5-9d43-444c-9d28-12edc33ba9fe)



egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/230459ab-9551-47e0-a2fa-16496df60dc1)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/88ad62c8-85d8-4671-8578-930be0f95d59)




egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/8f075ae7-130d-45e3-8e07-eac3b4fdae9c)



egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/2f0908e3-17a5-4c6a-96a7-29800113244b)


egrep 'Linux.*World' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/d43af940-1bd6-4e6a-a339-ab20d2b566f4)

egrep l{2} newfile
## OUTPUT
![image](https://github.com/user-attachments/assets/47c7e918-b64d-4e4c-8256-1a4128bbab2a)



egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/user-attachments/assets/54e68c14-91a4-4584-9748-be919df35a92)


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
![image](https://github.com/user-attachments/assets/3ca8a5d8-cf8e-4937-9a68-ec7b81dd176b)



sed -n -e '$p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/ff6a36e8-fe0f-441e-b23d-ce00b1f5a541)


sed  -e 's/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/4762733a-0f6d-48e9-a1c3-1b5aa4b1b45e)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/1826178f-6f68-4326-806a-cfe13f05a806)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/e71fb85f-95b2-411a-8399-eab20da04721)



sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/984c29d5-a88a-48e5-9aad-3733747708be)




sed -n -e '2,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/2fa69837-0e8b-4b87-a1a4-eb38da9867b8)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/db5bcb2b-7133-4847-89d2-a41cf7b28948)



seq 10 
## OUTPUT
![image](https://github.com/user-attachments/assets/6ee17304-f013-492d-8b61-03a1442dc44a)



seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/user-attachments/assets/a021805e-7c6c-4a33-9eeb-62c4258a7afc)



seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/user-attachments/assets/a711c3d1-55e4-42de-81f5-ba460aa19f1e)



seq 3 | sed '2a hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/9e174803-3084-4e85-8069-09644ebe2978)



seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/8cdaaf84-d14e-45d2-a161-de25c780db9a)


seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/f6e3f020-8af3-45a1-bb0d-b16068975211)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/1ca8a036-0d7e-4bcc-8075-5e2e655404fd)



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/e281416a-2783-4fc6-a89c-e4bcaf5c4c8e)


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
![image](https://github.com/user-attachments/assets/7451ff2c-aae3-4747-ba8c-c8754be302d3)


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

![image](https://github.com/user-attachments/assets/5c376f3a-7624-4a91-a312-543723fec4c7)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/user-attachments/assets/6f3cfe8c-dac4-4406-838f-69fdaee437a2)

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
![image](https://github.com/user-attachments/assets/d38abecd-47fa-4d4a-a686-763b8fd82097)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image](https://github.com/user-attachments/assets/fb65afda-05c5-48ef-9d1c-ce3af389fdf8)



#Backup commands
tar -cvf backup.tar *
## OUTPUT

![image](https://github.com/user-attachments/assets/6bb58c77-7db0-4dbc-90a6-71392457bfe9)
![image](https://github.com/user-attachments/assets/8aff84a8-940d-458b-916e-a27b824df9c3)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/07358383-b068-4541-8538-2f48c3c85fc3)


tar -xvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/c270aa42-7f65-409e-8b55-54f782054e14)

gzip backup.tar

ls .gz
## OUTPUT
 ![image](https://github.com/user-attachments/assets/b2b5ac31-db46-4f54-8a39-0385bc77d71e)

gunzip backup.tar.gz
## OUTPUT
![image](https://github.com/user-attachments/assets/815f10c3-4bb3-4e87-af17-e6866be9e9b6)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![image](https://github.com/user-attachments/assets/458ea6bf-0c70-475a-ba5e-38f66397755d)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![image](https://github.com/user-attachments/assets/e06ac6fc-c7ed-4b81-8170-008fa16a60a8)


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
![image](https://github.com/user-attachments/assets/c8138c42-870f-4af2-bfb9-91bc47dbcd21)

 
ls file1
## OUTPUT
![image](https://github.com/user-attachments/assets/9ab201e8-0dbb-4fe9-b817-34d1f7ec9cf6)

echo $?
## OUTPUT
![image](https://github.com/user-attachments/assets/9e9f587c-4c16-4418-b44e-462903103e51)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT
 ![image](https://github.com/user-attachments/assets/7f4546c0-b06e-4cb9-abe8-564d5cedddde)



 
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
![image](https://github.com/user-attachments/assets/d2f511ce-b51a-4ce0-a8be-7052b50ab94b)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/1c9f9240-33b4-4b48-99e6-22f95e69de72)


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
![image](https://github.com/user-attachments/assets/d35213e3-5a2b-49a7-850c-bdd72ec7a0e0)

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
![image](https://github.com/user-attachments/assets/d1c1a265-e03c-4602-b868-9fe411b88ac8)



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
![image](https://github.com/user-attachments/assets/0bfdee8d-2c57-44c4-b994-63edb5330be7)

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
![image](https://github.com/user-attachments/assets/9b959846-425c-4b95-aba9-0bcbdb4e916a)

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
![image](https://github.com/user-attachments/assets/89357964-4cc3-4b0c-8176-522521d42677)


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
![image](https://github.com/user-attachments/assets/589f561c-6f19-4077-b93b-1e4703c4d9bb)

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
 ![image](https://github.com/user-attachments/assets/19d97cd9-ff32-4288-b7df-3a7f930fe636)

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
 ![image](https://github.com/user-attachments/assets/9b72d4b8-6d5b-4435-907c-5c18d67cdc2a)

 
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
 ![image](https://github.com/user-attachments/assets/e76c44b1-c203-4b25-b4ce-c78bbce3da7f)

 
 
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
 ![image](https://github.com/user-attachments/assets/70961836-1fa2-450b-9b3a-cbc4d911d8fd)

 
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
![image](https://github.com/user-attachments/assets/0c0031a7-ee9c-4a73-a6e7-36d56e552934)
 
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
 ![image](https://github.com/user-attachments/assets/6b52d7be-5904-4a26-82e5-3e514b255983)

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
![image](https://github.com/user-attachments/assets/bd60914e-a1ab-4daf-b0de-ac81afa754a7)

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

![image](https://github.com/user-attachments/assets/0b54f461-fe00-42c6-a8af-e93557329781)


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

![image](https://github.com/user-attachments/assets/1dbcb7fe-0939-4771-97a9-bd73802e5167)

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

![image](https://github.com/user-attachments/assets/e768311f-ff5f-4bd0-866b-b799eb1b9638)

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

![image](https://github.com/user-attachments/assets/71ef0f21-0547-483d-90fb-f218e9c2eef1)

 
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

![image](https://github.com/user-attachments/assets/bf231025-14fc-4a0c-875f-47a2253ac48c)

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

![image](https://github.com/user-attachments/assets/1d3f6340-8082-4bca-8273-14988ffa281d)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

![image](https://github.com/user-attachments/assets/e2cc87b7-bfcc-453f-bd49-5ddce7b58838)



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

![image](https://github.com/user-attachments/assets/78ddb57d-b49f-42b6-ba69-42fff2242eb2)

 
 ./funcex.sh 1 2

 
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

 ![image](https://github.com/user-attachments/assets/68a6f7ef-dab1-4e4d-a4f3-67d64eb4c1da)

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
$ ./argshift.sh 1 2 3

 ![image](https://github.com/user-attachments/assets/fd5a11ed-58d6-4743-9a66-291b191e8947)

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

 ![image](https://github.com/user-attachments/assets/1ac75161-42b7-4c86-bc9e-f9ddc178dfe4)

 
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

 ![image](https://github.com/user-attachments/assets/4587a1ba-da59-497b-b04d-97e5c4ce332d)

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

![image](https://github.com/user-attachments/assets/ed572f11-402e-4b85-af30-9f7785f169bf)


# RESULT:
The Commands are executed successfully.
