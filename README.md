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

<img width="890" height="251" alt="Screenshot 2026-07-28 140754" src="https://github.com/user-attachments/assets/144070c0-be36-41b5-9b4e-b811ba917521" />


cat < file2
## OUTPUT
<img width="725" height="486" alt="Screenshot 2026-07-28 140923" src="https://github.com/user-attachments/assets/e9cf095f-6a6c-4068-af55-bdacebf09365" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="457" height="135" alt="Screenshot 2026-07-28 140959" src="https://github.com/user-attachments/assets/da9e4661-cb4a-4290-80d2-771801eb1d62" />


 
comm file1 file2
 ## OUTPUT
 
<img width="577" height="362" alt="image" src="https://github.com/user-attachments/assets/5a2accc1-c8b5-4521-baf5-378e47e6d160" />

 
diff file1 file2
## OUTPUT
<img width="533" height="365" alt="Screenshot 2026-07-28 141020" src="https://github.com/user-attachments/assets/eb75e1c9-aeb0-460f-a378-7309d0e573a2" />


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

<img width="438" height="137" alt="Screenshot 2026-07-28 141150" src="https://github.com/user-attachments/assets/3ce5e2e4-2a26-4f44-831f-94e21dbea647" />



cut -d "|" -f 1 file22
## OUTPUT
<img width="496" height="167" alt="Screenshot 2026-07-28 141247" src="https://github.com/user-attachments/assets/9eed1f44-60d8-48ae-b06e-00c6ae9e5ecf" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="352" height="145" alt="Screenshot 2026-07-28 141324" src="https://github.com/user-attachments/assets/97780ee4-00ce-4e82-8933-e9debfdb647e" />


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

<img width="465" height="132" alt="Screenshot 2026-07-28 141623" src="https://github.com/user-attachments/assets/428ef3d3-06a8-4523-80d0-282f23dcb98e" />


grep hello newfile 
## OUTPUT

<img width="457" height="83" alt="Screenshot 2026-07-28 141654" src="https://github.com/user-attachments/assets/6854c2b5-7ec8-4889-a8f2-ed8839340988" />



grep -v hello newfile 
## OUTPUT

<img width="412" height="112" alt="Screenshot 2026-07-28 141725" src="https://github.com/user-attachments/assets/5a5dda8d-793b-45ef-970d-b49399842551" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="382" height="107" alt="Screenshot 2026-07-28 141742" src="https://github.com/user-attachments/assets/e5592c18-03af-4622-8690-9f86b28692c5" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="422" height="77" alt="Screenshot 2026-07-28 141800" src="https://github.com/user-attachments/assets/bc9e53f6-5d92-4c6d-a423-5a89b9da5765" />



grep -R ubuntu /etc
## OUTPUT
<img width="822" height="668" alt="Screenshot 2026-07-28 141937" src="https://github.com/user-attachments/assets/c8bd6a0f-20b6-464a-bd59-6803b04d5f4e" />



grep -w -n world newfile   
## OUTPUT

<img width="407" height="111" alt="Screenshot 2026-07-28 141957" src="https://github.com/user-attachments/assets/8ffabb07-ed1e-4cb2-b67a-3dbcdb4ab954" />

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

<img width="450" height="105" alt="Screenshot 2026-07-28 142223" src="https://github.com/user-attachments/assets/9cdc25bd-e7bc-4ab9-baef-84e351334607" />


egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="420" height="120" alt="Screenshot 2026-07-28 142240" src="https://github.com/user-attachments/assets/1a80af20-ebf3-462b-b2d0-d46b3f98261c" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="420" height="106" alt="Screenshot 2026-07-28 142258" src="https://github.com/user-attachments/assets/9adaa60e-7b5f-442c-9d7f-afb18ae32e13" />




egrep '(^hello)' newfile 
## OUTPUT

<img width="432" height="77" alt="Screenshot 2026-07-28 142312" src="https://github.com/user-attachments/assets/d28e8b19-e3a1-42d7-98b7-c41b3432cbce" />


egrep '(world$)' newfile 
## OUTPUT
<img width="378" height="107" alt="Screenshot 2026-07-28 142335" src="https://github.com/user-attachments/assets/e61846c2-67aa-48be-8993-c92f65fd4a42" />



egrep '(World$)' newfile 
## OUTPUT

<img width="377" height="82" alt="Screenshot 2026-07-28 142359" src="https://github.com/user-attachments/assets/8e811695-c9e8-451b-9d43-eb27f0b4a71b" />

egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="371" height="106" alt="Screenshot 2026-07-28 142415" src="https://github.com/user-attachments/assets/ca230c9a-79dc-41c1-8d8a-56e101edecde" />


egrep '[1-9]' newfile 
## OUTPUT
<img width="426" height="83" alt="Screenshot 2026-07-28 142433" src="https://github.com/user-attachments/assets/f3df9721-4967-4262-b4ef-feb6763f57c4" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="385" height="82" alt="Screenshot 2026-07-28 142524" src="https://github.com/user-attachments/assets/357e13a7-a941-4590-82c2-d6b8a4617853" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="367" height="80" alt="Screenshot 2026-07-28 142543" src="https://github.com/user-attachments/assets/f5675c6c-d314-4cc2-bc00-d3d8eb5855c8" />

egrep l{2} newfile
## OUTPUT
<img width="397" height="110" alt="Screenshot 2026-07-28 142559" src="https://github.com/user-attachments/assets/0665aed9-3d28-4129-8c04-6fa3d26f8d33" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="391" height="135" alt="Screenshot 2026-07-28 142615" src="https://github.com/user-attachments/assets/d980c06a-834c-4d4f-af32-d4e25180491c" />


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
<img width="406" height="87" alt="Screenshot 2026-07-28 142653" src="https://github.com/user-attachments/assets/2b362d4a-a4f9-45c6-88ff-f43c07c0f1cc" />



sed -n -e '$p' file23
## OUTPUT
<img width="370" height="82" alt="Screenshot 2026-07-28 142714" src="https://github.com/user-attachments/assets/01c313c7-00d5-4a65-8e3e-471a0c529c2f" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="421" height="282" alt="Screenshot 2026-07-28 142730" src="https://github.com/user-attachments/assets/ed0b5d68-d48a-40ed-9689-c7b873262bf2" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="432" height="280" alt="Screenshot 2026-07-28 142745" src="https://github.com/user-attachments/assets/92387003-6723-4bf5-96e0-c1135fbd3880" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="476" height="272" alt="Screenshot 2026-07-28 142805" src="https://github.com/user-attachments/assets/ef8ce809-33b5-4db0-8220-2f53a95eb6fd" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="400" height="177" alt="Screenshot 2026-07-28 142834" src="https://github.com/user-attachments/assets/7add37b4-09ff-4d56-8fc6-73a07bf22910" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="403" height="122" alt="Screenshot 2026-07-28 142849" src="https://github.com/user-attachments/assets/73be24da-c561-4920-8f35-e622ec209548" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="457" height="101" alt="Screenshot 2026-07-28 142905" src="https://github.com/user-attachments/assets/39771f29-4d76-44a6-8cb7-67c2fcf2d67b" />



seq 10 
## OUTPUT
<img width="421" height="303" alt="Screenshot 2026-07-28 142922" src="https://github.com/user-attachments/assets/fc4fbf52-79b2-4f66-8d58-d2973a6ab6a6" />



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="401" height="140" alt="Screenshot 2026-07-28 142936" src="https://github.com/user-attachments/assets/ceaf49de-9426-4bea-b86e-fb8902dac025" />


seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="366" height="135" alt="Screenshot 2026-07-28 142958" src="https://github.com/user-attachments/assets/ff8ce819-5a8e-40f8-8993-4856c335b343" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="353" height="162" alt="Screenshot 2026-07-28 143019" src="https://github.com/user-attachments/assets/08c91a36-9ab1-4fe8-87c4-4ef93fbc4c92" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="403" height="122" alt="Screenshot 2026-07-28 142849" src="https://github.com/user-attachments/assets/9af99eed-7063-434b-b1b3-aba20b9bba85" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="480" height="132" alt="image" src="https://github.com/user-attachments/assets/303ce2cf-ec1e-4f4c-bd00-e739076761ef" />



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="456" height="130" alt="image" src="https://github.com/user-attachments/assets/6dfdd971-7392-4965-a866-c6925e8d5438" />


sed -n '2,4{s/$/*/;p}' file23


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

<img width="545" height="182" alt="image" src="https://github.com/user-attachments/assets/6cc61481-3816-4a4e-8095-721d268c7421" />

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

<img width="496" height="180" alt="image" src="https://github.com/user-attachments/assets/6994b26c-43ef-4ab5-8812-da5da2361a35" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="507" height="266" alt="image" src="https://github.com/user-attachments/assets/f5df0a5a-5d41-46bc-ac78-f84f0938980a" />

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
<img width="472" height="142" alt="image" src="https://github.com/user-attachments/assets/4f1acb55-972b-423e-bbac-383f28a41c38" />
 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="507" height="125" alt="image" src="https://github.com/user-attachments/assets/123f8d8c-8d5c-4382-b4e6-fe06b7344468" />

#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="566" height="322" alt="image" src="https://github.com/user-attachments/assets/a2807d1e-821a-44c5-b1d7-7b449e706951" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="680" height="536" alt="image" src="https://github.com/user-attachments/assets/a4339bdf-8ecc-4544-95e0-dbb20f785568" />


tar -xvf backup.tar
## OUTPUT

<img width="635" height="322" alt="image" src="https://github.com/user-attachments/assets/0742161c-5bec-4772-b625-d37f1645fe10" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="612" height="95" alt="image" src="https://github.com/user-attachments/assets/fa1f7908-cf8c-4d31-a75b-efdb46457547" />

gunzip backup.tar.gz
## OUTPUT
<img width="596" height="92" alt="image" src="https://github.com/user-attachments/assets/6d82ee5f-3ddc-463c-b5c3-2894a3e67b64" />


# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh

## OUTPUT
<img width="592" height="160" alt="image" src="https://github.com/user-attachments/assets/b8097b42-4ff0-4bca-a6fd-18663145b371" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="592" height="170" alt="image" src="https://github.com/user-attachments/assets/727e3c8f-686b-46b4-846f-dbdb7e7df40a" />


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
<img width="691" height="435" alt="image" src="https://github.com/user-attachments/assets/99ab9199-56e6-4a81-a924-f26209dfcb9e" />

 
ls file1
## OUTPUT

<img width="620" height="86" alt="image" src="https://github.com/user-attachments/assets/ec6abb14-0b43-4909-a6d3-a7d32038812a" />

echo $?
## OUTPUT

<img width="597" height="80" alt="image" src="https://github.com/user-attachments/assets/c8afd65c-2681-4aba-a392-5e8b68412270" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT
 
<img width="651" height="85" alt="image" src="https://github.com/user-attachments/assets/96905151-3004-4713-a4a5-e4427c5ab3b1" />


 
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



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="672" height="297" alt="image" src="https://github.com/user-attachments/assets/3a08962a-7654-4f56-9428-7a64d168235c" />


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

<img width="582" height="77" alt="image" src="https://github.com/user-attachments/assets/d39ef5e0-cced-4a81-b17a-2a84bdb0bbd8" />

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
<img width="635" height="500" alt="image" src="https://github.com/user-attachments/assets/38e8b40c-47b4-4f4e-95af-f485494f2734" />



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

<img width="651" height="157" alt="image" src="https://github.com/user-attachments/assets/81eebb11-334f-4d1b-b645-aec0579ea48c" />

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
<img width="670" height="515" alt="image" src="https://github.com/user-attachments/assets/98e73e84-45bc-4fe4-9ee4-fd7d54f79cb8" />


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

<img width="607" height="231" alt="image" src="https://github.com/user-attachments/assets/40577550-77ba-4986-98a5-1c0cb5176cee" />


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
<img width="651" height="222" alt="image" src="https://github.com/user-attachments/assets/bb92f7f7-983b-4070-a13e-7543a349c755" />

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
$ #!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done

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

<img width="605" height="190" alt="image" src="https://github.com/user-attachments/assets/2b77ef16-9556-45fb-aa9e-904d367f1ba6" />

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
<img width="637" height="271" alt="image" src="https://github.com/user-attachments/assets/ea17caa3-b21d-4789-af8a-0706daa90d93" />

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

<img width="592" height="357" alt="image" src="https://github.com/user-attachments/assets/eb7f01f7-954a-4f1d-8e50-5906edd0ace2" />


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
 
<img width="616" height="331" alt="image" src="https://github.com/user-attachments/assets/4cc24414-f8a9-4a16-9cd8-0ae5d38f22f1" />
 
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

<img width="687" height="365" alt="image" src="https://github.com/user-attachments/assets/36a406b4-41af-44c3-ada8-368022c4f52b" />

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

<img width="635" height="112" alt="image" src="https://github.com/user-attachments/assets/f8c5d575-07a0-47fb-819a-90371df77659" />

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

<img width="651" height="197" alt="image" src="https://github.com/user-attachments/assets/f01d4e84-2d4b-48d4-be5b-2ceea2e10d43" />

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="711" height="372" alt="image" src="https://github.com/user-attachments/assets/11bcbfd7-191c-4222-a11e-ee3416515379" />

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
<img width="636" height="230" alt="image" src="https://github.com/user-attachments/assets/ebb425f7-2ee6-4b70-8cc9-cf9e826bb424" />

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

## OUTPUT
<img width="662" height="352" alt="image" src="https://github.com/user-attachments/assets/99dfd6f0-742e-4903-96d4-357980dfae8b" />

$ ./argshift.sh 1 2 3
 
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

<img width="670" height="385" alt="image" src="https://github.com/user-attachments/assets/fb9dba2e-f6e2-4344-bde6-bce0044dc011" />

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
<img width="572" height="606" alt="image" src="https://github.com/user-attachments/assets/8eaceac4-93c5-469a-866b-7c7eb14dc9b1" />

 ./argshift.sh 1 2 3
 
 
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
<img width="602" height="387" alt="image" src="https://github.com/user-attachments/assets/c74d04b8-d651-4889-8257-ed445ea210ba" />

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

<img width="612" height="582" alt="image" src="https://github.com/user-attachments/assets/42160f59-9e14-41b0-ad41-a37fd5995b15" />

# RESULT:
The Commands are executed successfully.
