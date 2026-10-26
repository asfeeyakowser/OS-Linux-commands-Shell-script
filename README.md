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
<img width="685" height="310" alt="image" src="https://github.com/user-attachments/assets/ea44d537-2b0d-460e-bcb8-7fd98e4f0a5f" />



cat < file2
## OUTPUT
<img width="712" height="326" alt="image" src="https://github.com/user-attachments/assets/1df3c705-e47b-4f2f-acfa-4c1996e98f15" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="817" height="557" alt="image" src="https://github.com/user-attachments/assets/1b26bd32-b695-4ba1-809a-f44a018aa5de" />

comm file1 file2
 ## OUTPUT

 
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
<img width="682" height="108" alt="image" src="https://github.com/user-attachments/assets/48ea9be9-a2cf-4356-920f-d077c69faba2" />
<img width="635" height="117" alt="image" src="https://github.com/user-attachments/assets/41bcdc0d-2e71-41a6-b5f0-6767f0a79e2a" />
<img width="646" height="93" alt="image" src="https://github.com/user-attachments/assets/74f95efb-ec8b-4ed5-a177-8034d33898b3" />
<img width="646" height="142" alt="image" src="https://github.com/user-attachments/assets/f6d1cf39-94b6-4689-9083-0aef3e64ff23" />


cut -d "|" -f 1 file22
## OUTPUT
cut -d "|" -f 2 file22
<img width="642" height="110" alt="image" src="https://github.com/user-attachments/assets/21379410-01eb-4602-bc0d-e627e852bccc" />

## OUTPUT


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
grep hello newfile 
<img width="645" height="183" alt="image" src="https://github.com/user-attachments/assets/55614d39-d4d0-4a95-a2c0-5c0b6ed3cc4e" />




## OUTPUT
grep -v hello newfile 
<img width="633" height="76" alt="image" src="https://github.com/user-attachments/assets/9ce2a4a3-e53a-4e14-a03a-ec18068bbe45" />

## OUTPUT
cat newfile | grep -i "hello"
<img width="633" height="108" alt="image" src="https://github.com/user-attachments/assets/cee8249e-ed35-41f6-97cb-3b66ef9b6113" />

## OUTPUT
cat newfile | grep -i -c "hello"
<img width="633" height="78" alt="image" src="https://github.com/user-attachments/assets/e38bdeac-152f-4600-b635-ed74c4aa1008" />

## OUTPUT
grep -R ubuntu /etc
<img width="641" height="77" alt="image" src="https://github.com/user-attachments/assets/c4d77914-12ca-44d9-a19c-94ad4e365f31" />

## OUTPUT
grep -w -n world newfile 
<img width="695" height="92" alt="image" src="https://github.com/user-attachments/assets/4a12c3f7-44bd-45a0-b58c-c60cc2c639ab" />

## OUTPUT


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
egrep -w '(H|h)ello' newfile 
<img width="670" height="448" alt="image" src="https://github.com/user-attachments/assets/379b8161-c80d-48dd-a3e2-8a7697347e91" />

## OUTPUT
egrep -w '(H|h)ell[a-z]' newfile 
<img width="633" height="97" alt="image" src="https://github.com/user-attachments/assets/1ce88610-5625-49c5-9741-0bb95e519eda" />

## OUTPUT
egrep '(^hello)' newfile 
<img width="637" height="110" alt="image" src="https://github.com/user-attachments/assets/8be89d7a-4457-4995-873d-19643cbc8f53" />


## OUTPUT
egrep '(world$)' newfile 
<img width="635" height="102" alt="image" src="https://github.com/user-attachments/assets/ff210b33-6ad9-4182-bc01-ec0ee13af2b5" />

## OUTPUT
egrep '(World$)' newfile 
<img width="653" height="76" alt="image" src="https://github.com/user-attachments/assets/2db657ca-9531-43ed-a914-83197b599a3f" />

## OUTPUT
egrep '((W|w)orld$)' newfile 
<img width="668" height="117" alt="image" src="https://github.com/user-attachments/assets/fd649f07-59be-4e06-b01d-911a47a26d96" />

## OUTPUT
egrep '[1-9]' newfile 
<img width="637" height="67" alt="image" src="https://github.com/user-attachments/assets/8ae85593-d401-460c-8f6b-c8dda9758a46" />

## OUTPUT
egrep 'Linux.*world' newfile 
<img width="627" height="87" alt="image" src="https://github.com/user-attachments/assets/a1f96d5f-8f9e-445a-8964-007270352b6e" />

## OUTPUT
egrep 'Linux.*World' newfile 
<img width="637" height="82" alt="image" src="https://github.com/user-attachments/assets/7bee2e5c-052a-489e-bed0-ecdf6ca519c9" />

## OUTPUT
egrep l{2} newfile
<img width="636" height="110" alt="image" src="https://github.com/user-attachments/assets/23721654-d6b4-4c46-a7d8-67bfae4278d8" />

## OUTPUT
egrep 's{1,2}' newfile
<img width="630" height="127" alt="image" src="https://github.com/user-attachments/assets/8e78700d-4fe1-4aab-a466-fdae04685cf0" />

## OUTPUT 


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
<img width="706" height="313" alt="image" src="https://github.com/user-attachments/assets/587dda31-8238-48e6-901e-ff93faa72900" />

## OUTPUT

sed -n -e '$p' file23
<img width="645" height="77" alt="image" src="https://github.com/user-attachments/assets/af757244-cd79-4ca0-9d7c-c929c3d946f6" />


## OUTPUT

sed  -e 's/Ram/Sita/' file23
<img width="627" height="245" alt="image" src="https://github.com/user-attachments/assets/4d912fca-5cd6-4fee-857c-388ee6f605b3" />

## OUTPUT

sed  -e '2s/Ram/Sita/' file23
<img width="590" height="277" alt="image" src="https://github.com/user-attachments/assets/f6f0be78-2ed2-4492-98cb-69361ccabd35" />

## OUTPUT

sed  '/tom/s/5000/6000/' file23
<img width="622" height="246" alt="image" src="https://github.com/user-attachments/assets/90b86844-6282-44c8-a167-f3da18bcc13e" />

## OUTPUT
sed -n -e '1,5p' file23
<img width="631" height="180" alt="image" src="https://github.com/user-attachments/assets/1bf141bc-3638-4cfb-9e2f-75146f519d18" />

## OUTPUT
sed -n -e '2,/Joe/p' file23
<img width="633" height="122" alt="image" src="https://github.com/user-attachments/assets/cf478bcc-ef7b-4cf1-9caa-5621f233eebe" />

## OUTPUT
sed -n -e '/tom/,/Joe/p' file23
<img width="642" height="103" alt="image" src="https://github.com/user-attachments/assets/de50e995-1358-4df2-9ea8-777a65ac544b" />

## OUTPUT
seq 10 
<img width="678" height="295" alt="image" src="https://github.com/user-attachments/assets/e0b6d2de-fce9-4008-8cc2-bd3e4352b17d" />

## OUTPUT

seq 10 | sed -n '4,6p'
<img width="661" height="130" alt="image" src="https://github.com/user-attachments/assets/96cf98f3-5236-4198-8c6d-b54f80245c5c" />

## OUTPUT
seq 10 | sed -n '2,~4p'
<img width="635" height="128" alt="image" src="https://github.com/user-attachments/assets/cfc71773-0fcb-4d72-9dbf-1f3c7fd6d0fa" />


## OUTPUT
seq 3 | sed '2a hello'
<img width="677" height="137" alt="image" src="https://github.com/user-attachments/assets/d931baf0-6894-4a8c-a0a8-2fff779eed7e" />

## OUTPUT

seq 2 | sed '2i hello'
<img width="677" height="161" alt="image" src="https://github.com/user-attachments/assets/14bfa215-06ac-4b82-ad0f-b2f3530450ad" />

## OUTPUT
seq 10 | sed '2,9c hello'
<img width="651" height="122" alt="image" src="https://github.com/user-attachments/assets/4f9b6215-6542-49be-b73b-a32ebb0b71f7" />

## OUTPUT
sed -n '2,4{s/^/$/;p}' file23
<img width="648" height="130" alt="image" src="https://github.com/user-attachments/assets/de7ff75c-d3cd-45cc-b7f8-a3f838dabdb4" />

## OUTPUT
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

<img width="626" height="115" alt="image" src="https://github.com/user-attachments/assets/baf21932-abe1-4b72-a966-e5cd4c2b0a5b" />
<img width="646" height="173" alt="image" src="https://github.com/user-attachments/assets/16571647-f9c3-4960-abd1-7bbe7647fa31" />
<img width="646" height="168" alt="image" src="https://github.com/user-attachments/assets/a20cab74-bae0-4d01-92e2-9873afc9a69f" />


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
<img width="826" height="367" alt="image" src="https://github.com/user-attachments/assets/71b13dd1-5ce2-426c-8940-33b683f2f01d" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="676" height="251" alt="image" src="https://github.com/user-attachments/assets/8bc7424d-6814-4b2e-add2-6b745a62144e" />

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

<img width="682" height="376" alt="image" src="https://github.com/user-attachments/assets/bdeeec69-2667-4b0e-9374-8e3b8d4676f4" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
#Backup commands
tar -cvf backup.tar *
<img width="647" height="125" alt="image" src="https://github.com/user-attachments/assets/e2c9a840-def5-4e01-845c-925e826507ac" />

## OUTPUT
<img width="716" height="397" alt="image" src="https://github.com/user-attachments/assets/a1734d1e-3139-4055-af17-b591a7b32671" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
tar -xvf backup.tar
<img width="827" height="252" alt="image" src="https://github.com/user-attachments/assets/0f598376-277b-4d79-a947-98423ab5bd4b" />

## OUTPUT
gzip backup.tar
ls .gz
<img width="782" height="190" alt="image" src="https://github.com/user-attachments/assets/747871eb-e8e8-4b17-96f5-7d7f441c8e96" />

## OUTPUT

gunzip backup.tar.gz
<img width="645" height="52" alt="image" src="https://github.com/user-attachments/assets/a6cd9ae1-ce72-4fdb-801c-dcafe7b1e573" />

## OUTPUT

 <img width="643" height="141" alt="image" src="https://github.com/user-attachments/assets/cff911f8-e265-4368-81fa-ef1074e0eef4" />

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT


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
<img width="717" height="627" alt="image" src="https://github.com/user-attachments/assets/d391fb81-d90b-4772-9da3-daddd66fbce0" />


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
 <img width="638" height="413" alt="image" src="https://github.com/user-attachments/assets/63308836-63b0-4659-842e-c812d6afc956" />

chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT

 
ls file1
<img width="637" height="91" alt="image" src="https://github.com/user-attachments/assets/c1746fd9-f2aa-4310-b143-2b4a882f34f5" />

## OUTPUT

echo $?
<img width="630" height="65" alt="image" src="https://github.com/user-attachments/assets/094a5b47-3898-4532-a72c-a783c8118396" />

## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
<img width="635" height="150" alt="image" src="https://github.com/user-attachments/assets/711e3e91-5d02-4ca2-8266-28633a4ba021" />

## OUTPUT 
 
abcd
 
echo $?
<img width="653" height="142" alt="image" src="https://github.com/user-attachments/assets/9ba29581-80f3-457a-8edc-3a4abb86819d" />

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
##OUTPUT



chmod 755 strcomp.sh
 
./strcomp.sh 
<img width="662" height="550" alt="image" src="https://github.com/user-attachments/assets/221d3bd5-b055-4f32-ad0b-58db4e1fee50" />
<img width="676" height="161" alt="image" src="https://github.com/user-attachments/assets/04a64b71-f6c1-497b-8009-04e5606dec17" />

## OUTPUT


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
****<img width="680" height="641" alt="image" src="https://github.com/user-attachments/assets/a25f2424-10da-4cf5-ad8c-0271e431dfb8" />

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

<img width="673" height="467" alt="image" src="https://github.com/user-attachments/assets/1b6faaf9-aed7-42d3-be10-d52b454038be" />
<img width="652" height="543" alt="image" src="https://github.com/user-attachments/assets/b12047a0-5ab2-46cd-b88f-ba1430bf1edb" />


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
<img width="726" height="637" alt="image" src="https://github.com/user-attachments/assets/1fe1953d-b833-450c-b3e5-1780554e4626" />

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
<img width="638" height="453" alt="image" src="https://github.com/user-attachments/assets/708bfe5a-c060-4d8c-bcdf-72d924783d8a" />
<img width="662" height="472" alt="image" src="https://github.com/user-attachments/assets/b0e0679d-bfff-4cd5-828d-1d6f20146cad" />
<img width="631" height="147" alt="image" src="https://github.com/user-attachments/assets/879c2cf6-99c7-4c30-bfd7-ad56479dbab3" />

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
<img width="702" height="487" alt="image" src="https://github.com/user-attachments/assets/253187b0-102b-4b99-a728-b84e239b4026" />
<img width="731" height="568" alt="image" src="https://github.com/user-attachments/assets/67a157da-0e5d-4787-8007-ab339076fa4f" />


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
<img width="730" height="343" alt="image" src="https://github.com/user-attachments/assets/121da2f8-edae-4aeb-af35-dbff13122ef3" />

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
 <img width="687" height="322" alt="image" src="https://github.com/user-attachments/assets/735951a3-31c4-4e82-a56d-603abaaec675" />

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

<img width="702" height="442" alt="image" src="https://github.com/user-attachments/assets/6f4068b3-2893-46e6-bda2-ccced6babfc6" />
<img width="662" height="242" alt="image" src="https://github.com/user-attachments/assets/98431ad2-3fb7-4974-9bf9-7ceab78f9d22" />
<img width="742" height="617" alt="image" src="https://github.com/user-attachments/assets/4c9acf29-6098-4807-923a-1970ce73ddfb" />
<img width="802" height="642" alt="image" src="https://github.com/user-attachments/assets/3f61b5e6-1c35-4bcb-8335-8add440913f4" />

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
<img width="707" height="113" alt="image" src="https://github.com/user-attachments/assets/c5f5b97c-de24-46e8-9ffd-bac7b28ea392" />

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
<img width="722" height="192" alt="image" src="https://github.com/user-attachments/assets/fcec4ce2-98e9-435a-a2c3-3b74c259b30d" />

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

 <img width="695" height="98" alt="image" src="https://github.com/user-attachments/assets/0920f83d-8f55-4a71-bfee-36b277264442" />

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
 <img width="695" height="98" alt="image" src="https://github.com/user-attachments/assets/f52d0b1e-8132-45fa-8f47-c69771b3a954" />

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

<img width="673" height="92" alt="image" src="https://github.com/user-attachments/assets/1e8b4a72-bc97-4f07-bc7e-72d15f6a11e4" />

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="653" height="122" alt="image" src="https://github.com/user-attachments/assets/6c07b65e-c5fd-4f10-acf9-5b013432bc24" />


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

 <img width="637" height="127" alt="image" src="https://github.com/user-attachments/assets/8ca23856-1289-45b7-93c5-65ee336f2002" />

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
 <img width="706" height="390" alt="image" src="https://github.com/user-attachments/assets/19ff12e9-c0a1-4600-b303-63d0f0a0730b" />

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
 <img width="667" height="382" alt="image" src="https://github.com/user-attachments/assets/b9a8a06d-33d7-4189-8dd8-f46331008067" />

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

<img width="723" height="602" alt="image" src="https://github.com/user-attachments/assets/6c26960b-947e-466e-aa27-ad678ad6ea0d" />

# RESULT:
The Commands are executed successfully.
