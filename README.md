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
![Screenshot 2024-09-03 084059](https://github.com/user-attachments/assets/ce632aca-6d81-4a74-ad38-ed3cff50fd34)



cat < file2
## OUTPUT
![Screenshot 2024-09-03 084112](https://github.com/user-attachments/assets/27d84d0b-bd17-4b91-848b-229484b12fab)



# Comparing Files
cmp file1 file2
## OUTPUT
 ![Screenshot 2024-09-03 084220](https://github.com/user-attachments/assets/9df0818c-b3e3-4591-8187-317ad1a35261)

comm file1 file2
 ## OUTPUT
![Screenshot 2024-09-03 084248](https://github.com/user-attachments/assets/91f2f4f5-2ace-44a4-a05b-41b42f174a9a)

 
diff file1 file2
## OUTPUT
![Screenshot 2024-09-03 084324](https://github.com/user-attachments/assets/fd1246bd-8694-45a9-999c-28a10b35392c)


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
![Screenshot 2024-09-03 085129](https://github.com/user-attachments/assets/38bdf739-2f79-4306-a0df-d2607c0db600)




cut -d "|" -f 1 file22
## OUTPUT
![Screenshot 2024-09-03 085158](https://github.com/user-attachments/assets/ae8f663e-a944-4950-9d61-c0848e1799f3)



cut -d "|" -f 2 file22
## OUTPUT
![Screenshot 2024-09-03 085224](https://github.com/user-attachments/assets/9b7c467d-2601-458a-9f79-1c6fbd879d30)


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
![Screenshot 2024-09-03 085900](https://github.com/user-attachments/assets/68e583a6-6aef-4bf6-ad07-83a816c8728c)



grep hello newfile 
## OUTPUT

![Screenshot 2024-09-03 085831](https://github.com/user-attachments/assets/f137e1a6-a6c8-4b2e-8340-84df0fb118ca)



grep -v hello newfile 
## OUTPUT
![Screenshot 2024-09-03 085925](https://github.com/user-attachments/assets/398bac1a-ad13-457d-8e00-f28b357c4483)



cat newfile | grep -i "hello"
## OUTPUT
![Screenshot 2024-09-03 085957](https://github.com/user-attachments/assets/edc2d25e-b10e-4f0b-942b-2d702a8d4462)




cat newfile | grep -i -c "hello"
## OUTPUT
![Screenshot 2024-09-03 090508](https://github.com/user-attachments/assets/45b7d8a3-f25e-46ee-bf6b-2851d681750f)




grep -R ubuntu /etc
## OUTPUT

![Screenshot 2024-09-03 090058](https://github.com/user-attachments/assets/a83d1cf2-99f6-42b6-9ddb-ad655e9cacfe)


grep -w -n world newfile   
## OUTPUT

![Screenshot 2024-09-03 090153](https://github.com/user-attachments/assets/97059268-6e90-4983-b78c-fe3e3262be47)

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
![Screenshot from 2024-09-03 09-24-56](https://github.com/user-attachments/assets/ddd0ec30-fdfb-4dec-a2bd-b8462638dcd9)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![Screenshot from 2024-09-03 09-26-45](https://github.com/user-attachments/assets/6f20ad6d-7c09-4b6e-8467-5b51537c57f4)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![Screenshot from 2024-09-03 09-30-10](https://github.com/user-attachments/assets/41a75205-d5a7-466a-b569-37d3c7774826)




egrep '(^hello)' newfile 
## OUTPUT
![Screenshot from 2024-09-03 09-31-02](https://github.com/user-attachments/assets/75f28b59-4027-48c2-91a9-4f21cccde7dd)



egrep '(world$)' newfile 
## OUTPUT
![Screenshot from 2024-09-03 09-31-40](https://github.com/user-attachments/assets/bd60bf42-d896-4181-af51-e090b78ae4ce)



egrep '(World$)' newfile 
## OUTPUT
![Screenshot from 2024-09-03 09-31-40](https://github.com/user-attachments/assets/bd60bf42-d896-4181-af51-e090b78ae4ce)


egrep '((W|w)orld$)' newfile 
## OUTPUT

![Screenshot from 2024-09-03 09-33-34](https://github.com/user-attachments/assets/a533d063-8cee-47b6-84e3-bceab6be0791)


egrep '[1-9]' newfile 
## OUTPUT
![Screenshot from 2024-09-03 09-34-26](https://github.com/user-attachments/assets/8e06f4a0-c314-4d8b-a132-a9d98dd6b2b4)



egrep 'Linux.*world' newfile 
## OUTPUT
![Screenshot from 2024-09-03 09-35-05](https://github.com/user-attachments/assets/0d497fa9-60b8-49ea-a8a1-f45621181cab)


egrep 'Linux.*World' newfile 
## OUTPUT
![Screenshot from 2024-09-03 09-35-05](https://github.com/user-attachments/assets/0d497fa9-60b8-49ea-a8a1-f45621181cab)


egrep l{2} newfile
## OUTPUT
![Screenshot from 2024-09-03 09-36-13](https://github.com/user-attachments/assets/5cec8ce8-85db-43a5-b442-6b4af44eaf5b)



egrep 's{1,2}' newfile
## OUTPUT 
![Screenshot from 2024-09-03 09-36-50](https://github.com/user-attachments/assets/db3f40f2-de3b-4681-ba10-0e772555e8f7)


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
![Screenshot from 2024-09-11 21-09-47](https://github.com/user-attachments/assets/097771be-30cb-48b3-a357-34f5daf6dad9)



sed -n -e '$p' file23
## OUTPUT
![Screenshot from 2024-09-11 21-10-48](https://github.com/user-attachments/assets/ca972f03-2697-4b1c-9433-51bff3a02c25)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![Screenshot from 2024-09-11 21-11-42](https://github.com/user-attachments/assets/604b431f-3bb0-40da-94b4-9ce58c34c270)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![Screenshot from 2024-09-11 21-12-11](https://github.com/user-attachments/assets/f29e67e4-dc62-477c-97c3-503a67b5a608)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![Screenshot from 2024-09-11 21-12-53](https://github.com/user-attachments/assets/70c8b8b6-c762-4fc7-82ba-7ae125f962a5)



sed -n -e '1,5p' file23
## OUTPUT
![Screenshot from 2024-09-11 21-13-34](https://github.com/user-attachments/assets/530d4600-bfb1-44b8-831f-492e17360018)



sed -n -e '2,/Joe/p' file23
## OUTPUT

![Screenshot from 2024-09-11 21-14-08](https://github.com/user-attachments/assets/6743bed6-a311-4d6d-b3bc-8ff62b7461d7)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![Screenshot from 2024-09-11 21-14-42](https://github.com/user-attachments/assets/7a47be3a-e7eb-4a4e-8fd3-31c93433cb19)


seq 10 
## OUTPUT

![Screenshot from 2024-09-11 21-15-32](https://github.com/user-attachments/assets/b3b8fdeb-92d6-4c42-a4e9-dc3fbf314eb4)


seq 10 | sed -n '4,6p'
## OUTPUT
![Screenshot from 2024-09-11 21-17-16](https://github.com/user-attachments/assets/133fb48f-48c0-4a35-9a23-c9b0dfdc1db6)



seq 10 | sed -n '2,~4p'
## OUTPUT

![Screenshot from 2024-09-11 21-17-45](https://github.com/user-attachments/assets/45f1539d-425d-4eb2-928d-424b638a8bf2)


seq 3 | sed '2a hello'
## OUTPUT
![Screenshot from 2024-09-11 21-18-32](https://github.com/user-attachments/assets/a1086c6d-7c6a-47dd-ab99-acf7878a77e4)



seq 2 | sed '2i hello'
## OUTPUT
![Screenshot from 2024-09-11 21-19-00](https://github.com/user-attachments/assets/fd494e69-feb2-4a60-9df7-bd5a49f5ffc1)


seq 10 | sed '2,9c hello'
## OUTPUT
![Screenshot from 2024-09-11 21-19-35](https://github.com/user-attachments/assets/7249090c-4ab6-4e37-b80f-6c132a6c0faf)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![Screenshot from 2024-09-11 21-20-17](https://github.com/user-attachments/assets/aabd39ed-2e2a-4bd2-9428-1110a1424808)



sed -n '2,4{s/$/*/;p}' file23
![Screenshot from 2024-09-11 21-20-39](https://github.com/user-attachments/assets/a529a281-8b31-4878-8046-c31c80b08c34)


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
![Screenshot from 2024-09-11 21-21-42](https://github.com/user-attachments/assets/facf374a-03ff-465d-abc8-3ecb15514819)


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

![Screenshot from 2024-09-11 21-22-42](https://github.com/user-attachments/assets/07319960-703a-42d1-bb96-65dbecf3da85)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![Screenshot from 2024-09-11 21-23-36](https://github.com/user-attachments/assets/fa106289-2ab7-45d7-961d-c59cfd664e80)

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
![Screenshot from 2024-09-11 21-25-35](https://github.com/user-attachments/assets/30a31cdb-1ffc-48c7-a2dc-de4214d8cbeb)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![Screenshot from 2024-09-11 21-26-08](https://github.com/user-attachments/assets/e596ae52-228d-4941-98c8-a3d711f423d7)


#Backup commands
tar -cvf backup.tar *
## OUTPUT
![Screenshot 2024-09-23 114239](https://github.com/user-attachments/assets/8ec4e174-61d1-4138-8c5a-9e6c4b6281cd)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![Screenshot 2024-09-23 114306](https://github.com/user-attachments/assets/64045e1a-8077-4774-aee0-f5e5ead9299f)


tar -xvf backup.tar  
## OUTPUT
![Screenshot 2024-09-23 114324](https://github.com/user-attachments/assets/de1ec39f-1056-4dff-9bfc-91c3e64f8360)

gzip backup.tar

ls .gz
## OUTPUT
 ![Screenshot 2024-09-23 114337](https://github.com/user-attachments/assets/887b1a3e-a7af-441d-a3c0-f4722e2fdcb1)

gunzip backup.tar.gz
## OUTPUT
![Screenshot 2024-09-23 114353](https://github.com/user-attachments/assets/4c9d6190-570f-449e-83a2-d4ff74f5e2fd)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![Screenshot 2024-09-23 114416](https://github.com/user-attachments/assets/a4a62157-94df-47d8-b63a-9da8ff24f04e)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![Screenshot 2024-09-23 114431](https://github.com/user-attachments/assets/ca32f1bf-ba5a-4c1e-a1d7-63ac54f5e99f)


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

 ![Screenshot 2024-09-23 114451](https://github.com/user-attachments/assets/6b9de1fe-4d4a-49ee-b83a-21946258084a)

ls file1
## OUTPUT
![Screenshot 2024-09-23 114506](https://github.com/user-attachments/assets/f35b5f12-932a-486a-b7fc-a22e0a56f04b)

echo $?
## OUTPUT 
![Screenshot 2024-09-23 114521](https://github.com/user-attachments/assets/0ed3b3d4-2490-486a-add7-c0e5745f5d33)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT


 
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
## OUTPUT
![Screenshot 2024-09-23 114538](https://github.com/user-attachments/assets/d3b39808-90df-40fb-a4ae-b4c2f09cd6a2)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

![Screenshot 2024-09-23 114554](https://github.com/user-attachments/assets/3ede8da4-15a5-463b-bdf4-df48b3143efe)

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
![Screenshot 2024-09-23 114609](https://github.com/user-attachments/assets/c4f7f899-6fbb-4052-9372-da2315b7250c)

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
![Screenshot 2024-09-23 114622](https://github.com/user-attachments/assets/773e8e81-1c9d-42f0-b25e-2be5472fe31a)



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
## OUTPUT
![Screenshot 2024-09-23 114636](https://github.com/user-attachments/assets/4c40133d-e151-4384-a4e1-49098a5206c3)

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
## OUTPUT
![Screenshot 2024-09-23 114649](https://github.com/user-attachments/assets/f719b4a4-f31c-42b4-9015-0c7c79370382)

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
![Screenshot 2024-09-23 114703](https://github.com/user-attachments/assets/1c7798db-13c6-43e6-9e9b-81e2b49dd9c6)


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
![Screenshot 2024-09-23 114720](https://github.com/user-attachments/assets/41ce7152-282e-4742-ba30-355a18297bf9)

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
## OUTPUT

 ![Screenshot 2024-09-23 114735](https://github.com/user-attachments/assets/7da9ef45-eccf-4dae-acf3-782d42244010)

$ ./casecheck.sh 
 ## OUTPUT
 ![Screenshot 2024-09-23 114735](https://github.com/user-attachments/assets/8a746d0c-8d69-4b64-9082-ac43be969c08)

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
 
 ## OUTPUT
 ![Screenshot 2024-09-23 114749](https://github.com/user-attachments/assets/129bf818-e128-47d8-9601-81f4dfb282c4)

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
 
 ## OUTPUT
 ![Screenshot 2024-09-23 114803](https://github.com/user-attachments/assets/936ea1f3-c765-49f4-86ea-ea3ed081ab7f)

 
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
## OUTPUT
![Screenshot 2024-09-23 114815](https://github.com/user-attachments/assets/695799e8-2dff-4698-878f-4e225b5f32ad)

 
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
 ## OUTPUT
 ![Screenshot 2024-09-23 114829](https://github.com/user-attachments/assets/288ebed1-96de-420c-9d24-96d0b069fd70)

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
 ## OUTPUT
 ![Screenshot 2024-09-23 114829](https://github.com/user-attachments/assets/02484fcc-b31b-4662-b3d1-1204285accab)

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
 ## OUTPUT
 ![Screenshot 2024-09-23 114843](https://github.com/user-attachments/assets/74126e29-8f9c-4310-bdf0-36eec4c2a47f)

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

![Screenshot 2024-09-23 114858](https://github.com/user-attachments/assets/10a39bde-098d-437e-9332-2c829ed249a8)

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
![Screenshot 2024-09-23 114912](https://github.com/user-attachments/assets/01e3979e-bb7b-4c0b-9436-21943e094681)

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
![Screenshot 2024-09-23 114925](https://github.com/user-attachments/assets/f92a2088-e014-48c4-aceb-4592858045cf)

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
![Screenshot 2024-09-23 114948](https://github.com/user-attachments/assets/819b8650-df27-4135-9b55-2b4f7c4edab0)

 
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
 ![Screenshot 2024-09-23 115004](https://github.com/user-attachments/assets/6e50d452-0a74-40b3-826f-623308b31011)

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

![Screenshot 2024-09-23 115017](https://github.com/user-attachments/assets/9a5c4dff-6189-417a-a4e4-e3fc2986f339)

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

![Screenshot 2024-09-23 115029](https://github.com/user-attachments/assets/6f89b186-0e1a-482c-9121-4d2af0efb785)


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


$ ./argshift.sh 1 2 3
 ## OUTPUT
 ![Screenshot 2024-09-23 115043](https://github.com/user-attachments/assets/b40f4933-5123-4905-b347-6fcec5b5ee51)

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
![Screenshot 2024-09-23 115057](https://github.com/user-attachments/assets/8a175b09-efb7-4611-95f9-0ead39561ae0)

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
 
 ![Screenshot 2024-09-23 115111](https://github.com/user-attachments/assets/95ee8167-5dee-4604-9ffe-aeb1f9ac8c76)

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
 ![Screenshot 2024-09-23 115126](https://github.com/user-attachments/assets/1c613f05-599c-4b7e-a5d8-d4b4345cc0c0)

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

![Screenshot 2024-09-23 115153](https://github.com/user-attachments/assets/56399789-05ba-43da-87b1-3b70101eb42e)

# RESULT:
The Commands are executed successfully.
