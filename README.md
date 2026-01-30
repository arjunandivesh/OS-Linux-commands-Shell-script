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

<img width="341" height="102" alt="image" src="https://github.com/user-attachments/assets/fedbfdba-9249-4a99-b865-eacb312a964a" />


cat < file2
## OUTPUT

<img width="328" height="162" alt="image" src="https://github.com/user-attachments/assets/21e7fa25-ba36-48a0-9e4a-ce34906bb533" />


# Comparing Files
cmp file1 file2
## OUTPUT
 
comm file1 file2
 ## OUTPUT
<img width="420" height="45" alt="image" src="https://github.com/user-attachments/assets/8a09ee05-508b-453a-9e73-19fa93f9b788" />

 
diff file1 file2
## OUTPUT

<img width="428" height="305" alt="image" src="https://github.com/user-attachments/assets/42d7e53a-4940-4fe5-a4cb-37fcc89898ce" />


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

<img width="383" height="84" alt="image" src="https://github.com/user-attachments/assets/047413a9-29f9-4d97-b1f1-e07028049218" />



cut -d "|" -f 1 file22
## OUTPUT
<img width="433" height="109" alt="image" src="https://github.com/user-attachments/assets/94586e21-58ff-4360-8a33-729377d83517" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="442" height="110" alt="image" src="https://github.com/user-attachments/assets/fb9a5b51-a6c0-46a8-8ba1-e1ad1ab74c5d" />


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

<img width="409" height="56" alt="image" src="https://github.com/user-attachments/assets/02b1b503-9bf1-4282-8213-4fa35bf490b2" />


grep hello newfile 
## OUTPUT

<img width="400" height="58" alt="image" src="https://github.com/user-attachments/assets/56113fa2-3565-4994-9ae0-af484eb3ae90" />



grep -v hello newfile 
## OUTPUT

<img width="430" height="59" alt="image" src="https://github.com/user-attachments/assets/d4a81506-d435-42a2-9e69-cc87df8ee3c4" />


cat newfile | grep -i "hello"
## OUTPUT
<img width="546" height="81" alt="image" src="https://github.com/user-attachments/assets/4bd9e1f0-188c-412b-b4d9-3ed24c4cd5e0" />




cat newfile | grep -i -c "hello"
## OUTPUT

<img width="578" height="52" alt="image" src="https://github.com/user-attachments/assets/f7188887-afbb-4d97-8376-edef35f3172e" />



grep -R ubuntu /etc
## OUTPUT
<img width="609" height="218" alt="image" src="https://github.com/user-attachments/assets/8a637ef9-2cea-4e4a-8ca7-3205f68cd5e8" />



grep -w -n world newfile   
## OUTPUT
<img width="474" height="80" alt="image" src="https://github.com/user-attachments/assets/6b0794f8-7c58-4e73-bfd2-f685e25b4675" />


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
<img width="563" height="78" alt="image" src="https://github.com/user-attachments/assets/209cef00-cc29-4525-a9b8-a35cc931a93c" />



egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="522" height="82" alt="image" src="https://github.com/user-attachments/assets/094f71a1-10a1-420b-8d54-dfe35d6290a4" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="605" height="81" alt="image" src="https://github.com/user-attachments/assets/eef54ce1-0a47-4fc2-95e2-1b2f88a1d1b3" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="489" height="58" alt="image" src="https://github.com/user-attachments/assets/a9a45513-8c2b-4bb6-9fef-a03020c6eb0d" />



egrep '(world$)' newfile 
## OUTPUT

<img width="495" height="54" alt="image" src="https://github.com/user-attachments/assets/9acb5385-9210-4be1-b98e-fd4b0b0e09c3" />


egrep '(World$)' newfile 
## OUTPUT
<img width="485" height="49" alt="image" src="https://github.com/user-attachments/assets/774e285a-f12c-4848-ac04-1da6d97c7845" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="559" height="76" alt="image" src="https://github.com/user-attachments/assets/f657774f-fdc9-48e0-998c-f07aef3bb574" />



egrep '[1-9]' newfile 
## OUTPUT

<img width="475" height="62" alt="image" src="https://github.com/user-attachments/assets/ff0ddf47-97ef-4d68-9676-ae06e0fe74e8" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="547" height="55" alt="image" src="https://github.com/user-attachments/assets/c77977f5-f7ce-4464-a390-880bc9c63354" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="540" height="57" alt="image" src="https://github.com/user-attachments/assets/c8049b84-30ec-499e-9e70-52d8a4d3f1a4" />


egrep l{2} newfile
## OUTPUT

<img width="489" height="81" alt="image" src="https://github.com/user-attachments/assets/3e5dee2d-4891-4776-a669-7ecd09cee0e9" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="492" height="116" alt="image" src="https://github.com/user-attachments/assets/22219598-09b5-4d72-a1c0-b0b3f82f14dd" />


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
<img width="446" height="52" alt="image" src="https://github.com/user-attachments/assets/34699337-dcab-4ab7-b671-889273501f5c" />



sed -n -e '$p' file23
## OUTPUT
<img width="463" height="58" alt="image" src="https://github.com/user-attachments/assets/29913897-dc86-472c-8961-917788265a34" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="520" height="243" alt="image" src="https://github.com/user-attachments/assets/c6c4d612-749f-4550-bce5-b98d38bcbd78" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="521" height="237" alt="image" src="https://github.com/user-attachments/assets/2d5b5c3d-12c6-4ad3-8572-523272766a12" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="555" height="245" alt="image" src="https://github.com/user-attachments/assets/cb6415cb-f2ae-4283-a226-eefc8fc64739" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="481" height="169" alt="image" src="https://github.com/user-attachments/assets/61e64086-8011-4ef7-9cf4-0dabc72f844f" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="520" height="108" alt="image" src="https://github.com/user-attachments/assets/20407a7f-a4f4-462f-9e65-94678db9dcd6" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="560" height="83" alt="image" src="https://github.com/user-attachments/assets/cf56b47b-42c2-40b1-8cba-9c6068529598" />



seq 10 
## OUTPUT
<img width="337" height="301" alt="image" src="https://github.com/user-attachments/assets/2f86b03a-0d9b-40ef-b8c3-efd6ec86628e" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="482" height="107" alt="image" src="https://github.com/user-attachments/assets/c6518b01-ca72-4312-8085-e67c894194b8" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="504" height="107" alt="image" src="https://github.com/user-attachments/assets/8a9495b4-f4d0-4342-9315-4e387e262e92" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="474" height="135" alt="image" src="https://github.com/user-attachments/assets/874ebb5b-9a28-46ab-a4c8-9913221a2e94" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="464" height="106" alt="image" src="https://github.com/user-attachments/assets/df7df72d-9c4f-48da-9721-0db2b290efe4" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="504" height="108" alt="image" src="https://github.com/user-attachments/assets/87c82587-d3a2-417a-a668-bce7386924cc" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="542" height="102" alt="image" src="https://github.com/user-attachments/assets/e0663960-68f0-4189-9adb-38591648a5ab" />


sed -n '2,4{s/$/*/;p}' file23
#OUTPUT
<img width="565" height="112" alt="image" src="https://github.com/user-attachments/assets/348601df-6a20-4932-805c-c90ad6b56ead" />


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
<img width="343" height="156" alt="image" src="https://github.com/user-attachments/assets/1e29c3f0-e0f8-4ab3-b974-97bc000aac60" />


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

<img width="363" height="160" alt="image" src="https://github.com/user-attachments/assets/1c00f276-b879-41cd-b476-dbe8ddae160a" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="652" height="243" alt="image" src="https://github.com/user-attachments/assets/8dbdc208-873b-416a-a314-152d2b7e8f6f" />

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

<img width="536" height="113" alt="image" src="https://github.com/user-attachments/assets/5882a646-3e56-4850-a777-330f79d26167" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="664" height="109" alt="image" src="https://github.com/user-attachments/assets/c8983baa-46c6-4701-8385-83c28a0f9729" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="304" height="149" alt="image" src="https://github.com/user-attachments/assets/55bcdaac-ce8f-454c-b03a-0a4acc67b340" />


tar -xvf backup.tar
## OUTPUT
<img width="474" height="163" alt="image" src="https://github.com/user-attachments/assets/0b7cdd78-4d1f-4c8b-ad3e-aa1ebef8d89a" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="784" height="162" alt="image" src="https://github.com/user-attachments/assets/bdcc8b8c-6850-4b66-831d-b35863bb8c8c" />

gunzip backup.tar.gz
## OUTPUT
<img width="796" height="244" alt="image" src="https://github.com/user-attachments/assets/34320357-c859-4d4b-85df-f14b2709b19a" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="785" height="335" alt="image" src="https://github.com/user-attachments/assets/3800b4a7-342f-4a5e-974c-6e2db4732a3e" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="396" height="109" alt="image" src="https://github.com/user-attachments/assets/321eb3fc-4d64-4031-8169-e2c3a747ad2a" />


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
<img width="454" height="411" alt="image" src="https://github.com/user-attachments/assets/0a5100c8-9a45-4e18-ab19-1edb11c3c53c" />

 
ls file1
## OUTPUT
<img width="274" height="55" alt="image" src="https://github.com/user-attachments/assets/a51a7181-fb60-4f6a-b1cb-47a5f6d8ad99" />

echo $?
## OUTPUT 
<img width="290" height="56" alt="image" src="https://github.com/user-attachments/assets/92328f3a-eaff-4f77-9db1-606eb7a57d97" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="265" height="64" alt="image" src="https://github.com/user-attachments/assets/a966ec46-4286-42ef-9722-6d0346425800" />

abcd
 
echo $?
 ## OUTPUT

<img width="557" height="268" alt="image" src="https://github.com/user-attachments/assets/b7a99be2-0cc4-4011-8697-3cfc59cbdd34" />

 
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

<img width="542" height="299" alt="image" src="https://github.com/user-attachments/assets/f0bea342-f4cf-4341-9abc-daeb93c5bbd6" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="725" height="222" alt="image" src="https://github.com/user-attachments/assets/8961b0c2-fbc7-4548-9181-d5b59a9fbf89" />


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
<img width="751" height="307" alt="image" src="https://github.com/user-attachments/assets/0432c471-f482-4b42-814d-aee006359f27" />

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
<img width="605" height="583" alt="image" src="https://github.com/user-attachments/assets/25079b6d-eebe-44fd-ba69-e241e67fcfc9" />



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
<img width="579" height="473" alt="image" src="https://github.com/user-attachments/assets/f06640fd-f1ce-4a96-a4e6-35be1576c0aa" />



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
<img width="587" height="582" alt="image" src="https://github.com/user-attachments/assets/225ebb4a-1e9a-45bd-8d68-2ccb5e922fa4" />


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

<img width="690" height="571" alt="image" src="https://github.com/user-attachments/assets/d33f1c50-d881-458e-8b8d-cea4bd25bca3" />

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
<img width="584" height="298" alt="image" src="https://github.com/user-attachments/assets/638cdc05-5a90-4712-b6bb-2cc82e05d4e4" />


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
$ chmod 755 forin1.sh

## OUTPUT
<img width="599" height="193" alt="image" src="https://github.com/user-attachments/assets/de818b94-8943-4fc7-a668-5da06a6145e1" />

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

<img width="452" height="246" alt="image" src="https://github.com/user-attachments/assets/596df5c1-4b45-4792-91e6-faa759cd38fc" />

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
<img width="461" height="243" alt="image" src="https://github.com/user-attachments/assets/05353b6d-8fcb-442f-8eec-2564719d7968" />

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
<img width="448" height="243" alt="image" src="https://github.com/user-attachments/assets/d6b3390a-8c69-4bc1-95ab-e186770e52c0" />

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

 <img width="782" height="309" alt="image" src="https://github.com/user-attachments/assets/5dad65af-c42b-432e-9651-8054e24496ce" />


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

<img width="791" height="305" alt="image" src="https://github.com/user-attachments/assets/ac7dac85-b644-47e2-aee8-d0c83a813f78" />



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
<img width="517" height="282" alt="image" src="https://github.com/user-attachments/assets/6c7795d6-0b1a-4ad7-8791-3b0b4a8635b2" />

 
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
<img width="526" height="172" alt="image" src="https://github.com/user-attachments/assets/1e43f84c-860a-49b6-82bc-ff0ca999af6c" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="471" height="135" alt="image" src="https://github.com/user-attachments/assets/0730db2b-5b2a-4990-ac0a-c014e0e41613" />


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
<img width="336" height="39" alt="image" src="https://github.com/user-attachments/assets/6bffb717-2f59-483e-a9cb-2677f1902e4d" />

 
 ./funcex.sh 1 2

 <img width="313" height="35" alt="image" src="https://github.com/user-attachments/assets/906f3b61-20ad-4fec-9d11-4b38a2e92f77" />

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
<img width="373" height="59" alt="image" src="https://github.com/user-attachments/assets/88fc4c82-b9e6-4399-b71e-8cc18cd4369d" />

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
<img width="338" height="87" alt="image" src="https://github.com/user-attachments/assets/d4b5d672-4fcf-46a7-a7d2-ccc1620171e1" />

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

<img width="310" height="335" alt="image" src="https://github.com/user-attachments/assets/c330675a-314f-4f07-ab2e-05f7b8d2e778" />

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
 <img width="298" height="225" alt="image" src="https://github.com/user-attachments/assets/9916b7ee-cb7e-4544-aac0-8b11bf954eb0" />

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
<img width="772" height="63" alt="image" src="https://github.com/user-attachments/assets/ef770228-fead-4c42-b129-fb10b49f1720" />


# RESULT:
The Commands are executed successfully.
The Commands are executed successfully.
