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



cat < file2
## OUTPUT
<img width="499" height="134" alt="2" src="https://github.com/user-attachments/assets/161e7c65-b5d4-4a5e-9036-984c6ca3eb7a" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="465" height="56" alt="Screenshot from 2026-01-29 21-14-14" src="https://github.com/user-attachments/assets/362d2e63-c6c8-47c9-b7ca-e1a221529657" />

comm file1 file2
 ## OUTPUT
 <img width="473" height="184" alt="Screenshot from 2026-01-29 21-14-38" src="https://github.com/user-attachments/assets/f0b166df-ce30-4e89-92c4-8e367db2125a" />


 
diff file1 file2
## OUTPUT
<img width="478" height="232" alt="Screenshot from 2026-01-29 21-14-59" src="https://github.com/user-attachments/assets/f17ef415-b7e3-46d7-8ff0-99f88f0f742e" />


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

<img width="476" height="79" alt="Screenshot from 2026-01-29 21-16-59" src="https://github.com/user-attachments/assets/cb53b1b6-5b7f-4bb8-8b95-8e8270630dcd" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="475" height="101" alt="Screenshot from 2026-01-29 21-17-26" src="https://github.com/user-attachments/assets/8fc97c8d-b8f4-4d9e-a066-6a9e87804393" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="475" height="101" alt="Screenshot from 2026-01-29 21-17-26" src="https://github.com/user-attachments/assets/9e3ad37f-cad4-4a12-aece-e8741ba426bb" />


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

<img width="475" height="77" alt="Screenshot from 2026-01-29 21-18-40" src="https://github.com/user-attachments/assets/836a1d97-3388-4a68-8b98-7ca04bfee981" />


grep hello newfile 
## OUTPUT

<img width="475" height="77" alt="Screenshot from 2026-01-29 21-19-51" src="https://github.com/user-attachments/assets/b04a8d12-1edb-4d2a-b5a7-c81c210ffe7c" />



grep -v hello newfile 
## OUTPUT

<img width="475" height="77" alt="Screenshot from 2026-01-29 21-19-51" src="https://github.com/user-attachments/assets/1ca3d08c-0823-4d86-bbef-caf3e7c16932" />


cat newfile | grep -i "hello"
## OUTPUT




cat newfile | grep -i -c "hello"
## OUTPUT


<img width="531" height="57" alt="Screenshot from 2026-01-29 21-23-38" src="https://github.com/user-attachments/assets/a4a381f7-ef78-462d-b283-f6d282996acc" />


grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT
<img width="534" height="80" alt="Screenshot from 2026-01-29 21-24-44" src="https://github.com/user-attachments/assets/c2c0de9d-995e-4cb9-9cab-e9d1169a536a" />


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

<img width="534" height="80" alt="Screenshot from 2026-01-29 21-26-35" src="https://github.com/user-attachments/assets/68054a97-af99-4680-83f3-43115d739f91" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="534" height="80" alt="Screenshot from 2026-01-29 21-26-35" src="https://github.com/user-attachments/assets/19c1d230-8d43-4c0d-ada7-604e4514df5c" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="534" height="80" alt="Screenshot from 2026-01-29 21-27-20" src="https://github.com/user-attachments/assets/e0760159-d227-4749-a539-3ee714c70ddc" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="549" height="57" alt="Screenshot from 2026-01-29 21-28-54" src="https://github.com/user-attachments/assets/ecaad08d-68c6-475e-8d56-1e1eae44576a" />



egrep '(world$)' newfile 
## OUTPUT

<img width="534" height="80" alt="Screenshot from 2026-01-29 21-27-50" src="https://github.com/user-attachments/assets/2d758036-d8cb-46cb-a8dd-8b1536427c12" />


egrep '(World$)' newfile 
## OUTPUT


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="552" height="78" alt="Screenshot from 2026-01-29 21-29-35" src="https://github.com/user-attachments/assets/605aff5d-d76f-4850-877d-07fe73c4e770" />



egrep '[1-9]' newfile 
## OUTPUT

<img width="565" height="56" alt="Screenshot from 2026-01-29 21-29-55" src="https://github.com/user-attachments/assets/3268f78a-18b1-40ce-9a53-7375f5e7e88b" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="562" height="77" alt="Screenshot from 2026-01-29 21-30-29" src="https://github.com/user-attachments/assets/4edf1370-8dac-4c69-b0f1-f614f7a68bca" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="562" height="77" alt="Screenshot from 2026-01-29 21-30-29" src="https://github.com/user-attachments/assets/aa434059-1ee4-484a-9146-ce1d57720915" />



egrep l{2} newfile
## OUTPUT



egrep 's{1,2}' newfile
## OUTPUT 
<img width="552" height="75" alt="Screenshot from 2026-01-29 21-32-14" src="https://github.com/user-attachments/assets/a14c26fa-cf9d-4f01-b3d7-18c9dc994556" />


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

<img width="573" height="53" alt="Screenshot from 2026-01-29 21-35-15" src="https://github.com/user-attachments/assets/f25bf9a7-2439-4b44-a9bd-3dec61de4fe1" />


sed -n -e '$p' file23
## OUTPUT



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="570" height="182" alt="Screenshot from 2026-01-29 21-36-05" src="https://github.com/user-attachments/assets/6fa5da8a-06a6-4911-8501-8539d809ac1c" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="570" height="182" alt="Screenshot from 2026-01-29 21-36-36" src="https://github.com/user-attachments/assets/a8397668-f383-4943-baf4-215fa52864a4" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="582" height="145" alt="Screenshot from 2026-01-29 21-37-20" src="https://github.com/user-attachments/assets/49999bde-5562-4b6c-8a46-2b55d63e1cb8" />


sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="603" height="75" alt="Screenshot from 2026-01-29 21-37-45" src="https://github.com/user-attachments/assets/be6dd381-eede-4688-bf08-c7eed42f2cee" />





sed -n -e '/tom/,/Joe/p' file23
## OUTPUT



seq 10 
## OUTPUT
<img width="559" height="246" alt="Screenshot from 2026-01-29 21-39-06" src="https://github.com/user-attachments/assets/f6dba686-5d62-4559-978f-180479822715" />



seq 10 | sed -n '4,6p'
## OUTPUT



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="602" height="93" alt="Screenshot from 2026-01-29 21-45-19" src="https://github.com/user-attachments/assets/e4878c48-0f2d-44f0-bdbf-1ae4aaf6936d" />




seq 3 | sed '2a hello'
## OUTPUT
<img width="598" height="123" alt="Screenshot from 2026-01-29 21-45-44" src="https://github.com/user-attachments/assets/ac153dee-6ba8-40b6-8698-518fde7df937" />




seq 2 | sed '2i hello'
## OUTPUT
<img width="607" height="97" alt="Screenshot from 2026-01-29 21-46-08" src="https://github.com/user-attachments/assets/5e6a6d05-3bba-4b6b-9500-8e4c4e301edc" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="602" height="93" alt="Screenshot from 2026-01-29 21-44-41" src="https://github.com/user-attachments/assets/d6d6f7a1-f4fc-46bc-b0a1-9f30b222b42f" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="607" height="97" alt="Screenshot from 2026-01-29 21-47-04" src="https://github.com/user-attachments/assets/46079d7f-be82-4a22-8324-d585e42ca3f3" />



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
<img width="607" height="97" alt="Screenshot from 2026-01-29 21-47-30" src="https://github.com/user-attachments/assets/78f201d7-8bf4-43cc-adc7-02fe3fa5119d" />



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

<img width="598" height="139" alt="Screenshot from 2026-01-29 21-51-33" src="https://github.com/user-attachments/assets/57c7c96d-e64d-43d8-b0e6-7b07fcc412fd" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="574" height="190" alt="Screenshot from 2026-02-04 21-49-18" src="https://github.com/user-attachments/assets/0083019a-c0c0-48a9-a530-54a5f6646283" />

cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT
<img width="611" height="96" alt="Screenshot from 2026-02-04 21-50-50" src="https://github.com/user-attachments/assets/17081ad1-e095-4880-90b9-6ce960d17876" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="611" height="96" alt="Screenshot from 2026-02-04 21-52-09" src="https://github.com/user-attachments/assets/41a42556-27fd-4e0a-addd-ad89ce529bc6" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="615" height="205" alt="Screenshot from 2026-02-04 21-52-51" src="https://github.com/user-attachments/assets/8d7aed13-0dfe-4a83-8d1e-f6986aba75a7" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="615" height="205" alt="Screenshot from 2026-02-04 21-53-28" src="https://github.com/user-attachments/assets/a524b8ac-89e7-451d-82d2-38b2416fe721" />



tar -xvf backup.tar
## OUTPUT
<img width="615" height="205" alt="Screenshot from 2026-02-04 21-54-04" src="https://github.com/user-attachments/assets/6d1e003c-9a4f-4c22-997e-c5d9c7d1d72d" />

gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT

 <img width="1471" height="447" alt="image" src="https://github.com/user-attachments/assets/63dcc100-a986-4c7e-8eb0-e3cb6a686c28" />

# Shell Script
```
gunzip backup.tar.gz
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="573" height="51" alt="image" src="https://github.com/user-attachments/assets/2b7033b4-1966-4669-aa80-2c567d509b19" />


 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="530" height="141" alt="image" src="https://github.com/user-attachments/assets/0d4a65f0-e7d8-48f5-955b-43b5a73d9ab5" />

<img width="627" height="288" alt="image" src="https://github.com/user-attachments/assets/096c2d77-7c39-4960-9610-b6c8aa146262" />

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
<img width="627" height="288" alt="image" src="https://github.com/user-attachments/assets/06bf0c67-784d-4c51-8eac-c868df19b104" />

 
ls file1
## OUTPUT
<img width="680" height="56" alt="image" src="https://github.com/user-attachments/assets/756cf721-8798-49ae-820a-76fc0498c5c8" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="680" height="56" alt="image" src="https://github.com/user-attachments/assets/11193758-25aa-4374-9e0e-bf8656a9c0fd" />

abcd
 
echo $?
 ## OUTPUT


 <img width="679" height="183" alt="image" src="https://github.com/user-attachments/assets/91bb0107-7f4b-4590-a464-2af41f7db79f" />

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
<img width="670" height="107" alt="image" src="https://github.com/user-attachments/assets/e2bdc8d8-5604-42d1-88cd-a53fa5f5a4bd" />

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

<img width="670" height="107" alt="image" src="https://github.com/user-attachments/assets/1ba7c4c7-ced8-46f2-b45f-b2a704abbd52" />


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
<img width="663" height="139" alt="image" src="https://github.com/user-attachments/assets/d089da83-2a0b-4bd4-ad78-f26cc7f18af6" />


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
<img width="647" height="167" alt="image" src="https://github.com/user-attachments/assets/ecc1ad43-85ca-4151-bb00-fe76ab0f62f1" />

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
<img width="647" height="167" alt="image" src="https://github.com/user-attachments/assets/29285e1d-def2-48b3-bbde-175bc60ffad2" />

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
<img width="649" height="322" alt="image" src="https://github.com/user-attachments/assets/170d257f-ee42-47cb-ab3e-72971c5963b9" />

 
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
<img width="645" height="95" alt="image" src="https://github.com/user-attachments/assets/b139de8a-851c-4eaf-b942-1212abf02b96" />

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
 <img width="754" height="157" alt="image" src="https://github.com/user-attachments/assets/4bf003d4-27da-4cb9-b081-e2828f07267b" />

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
<img width="648" height="113" alt="image" src="https://github.com/user-attachments/assets/716415e2-dd25-424f-98a0-236d7c0b8442" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="445" height="125" alt="image" src="https://github.com/user-attachments/assets/48b3048b-d898-4b07-b675-4543f4f1793f" />


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
<img width="341" height="101" alt="image" src="https://github.com/user-attachments/assets/ddad96bc-b932-4f01-8f57-a1b0d876d0c3" />

 
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
 <img width="646" height="126" alt="image" src="https://github.com/user-attachments/assets/7e96c243-2051-4412-8b06-99090e12edb1" />

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
 <img width="646" height="126" alt="image" src="https://github.com/user-attachments/assets/6085ceed-aa0a-41c0-94b7-0852155fb120" />

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
 <img width="645" height="367" alt="image" src="https://github.com/user-attachments/assets/c3929128-ee2b-467d-8907-a0f9d6c77f51" />

 
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
 <img width="645" height="358" alt="image" src="https://github.com/user-attachments/assets/c7b1d23c-6d37-46da-a693-15a66f3a1e51" />

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
<img width="649" height="124" alt="image" src="https://github.com/user-attachments/assets/131bedaa-34f0-415e-81a1-fad9d67e4a51" />


# RESULT:
The Commands are executed successfully.
