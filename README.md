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

<img width="508" height="169" alt="Screenshot 2026-01-30 102911" src="https://github.com/user-attachments/assets/f00264a8-f90e-4d88-8d91-b92037b776ca" />


cat < file2
## OUTPUT
<img width="491" height="186" alt="Screenshot 2026-01-30 102918" src="https://github.com/user-attachments/assets/90ee85da-f9fd-46e0-a2ff-773e7e455330" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="561" height="58" alt="Screenshot 2026-01-30 102927" src="https://github.com/user-attachments/assets/f514e21b-ac59-4d38-9a8c-40e4106ca703" />

comm file1 file2
 ## OUTPUT
<img width="569" height="298" alt="Screenshot 2026-01-30 102938" src="https://github.com/user-attachments/assets/6db08d57-58bc-4100-9827-7cc7412cdf0d" />

 
diff file1 file2
## OUTPUT
<img width="517" height="223" alt="Screenshot 2026-01-30 103005" src="https://github.com/user-attachments/assets/47232e30-3fea-4a1e-9050-ec745ca396f0" />


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

<img width="517" height="93" alt="Screenshot 2026-01-30 103015" src="https://github.com/user-attachments/assets/9b094fa8-45ed-4523-a881-2ac9c176d7df" />



cut -d "|" -f 1 file22
## OUTPUT
<img width="531" height="114" alt="Screenshot 2026-01-30 103021" src="https://github.com/user-attachments/assets/c2f5d4d5-5062-414d-a096-687b82020530" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="542" height="110" alt="Screenshot 2026-01-30 103028" src="https://github.com/user-attachments/assets/36f65e30-3fa8-4fea-b089-b793cc592507" />


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

<img width="559" height="41" alt="Screenshot 2026-01-30 103036" src="https://github.com/user-attachments/assets/a864e030-f204-4623-90c3-5e166f06a976" />


grep hello newfile 
## OUTPUT

<img width="526" height="64" alt="Screenshot 2026-01-30 103043" src="https://github.com/user-attachments/assets/dbae6953-be1c-412e-909b-5c7dbbd1673a" />



grep -v hello newfile 
## OUTPUT

<img width="555" height="68" alt="Screenshot 2026-01-30 103051" src="https://github.com/user-attachments/assets/fcd9183d-5156-48ca-990f-33629fdb3b9a" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="580" height="68" alt="Screenshot 2026-01-30 103058" src="https://github.com/user-attachments/assets/c7dd8981-13ec-4915-b2f6-b42a9503f5a9" />



cat newfile | grep -i -c "hello"
## OUTPUT


<img width="1023" height="306" alt="Screenshot 2026-01-30 103105" src="https://github.com/user-attachments/assets/f7a63a28-f2c2-4cf0-aa89-abe171ef29a5" />


grep -R ubuntu /etc
## OUTPUT
<img width="651" height="61" alt="Screenshot 2026-01-30 103116" src="https://github.com/user-attachments/assets/bce56020-1ff0-47f4-9cae-900987bbefc4" />



grep -w -n world newfile   
## OUTPUT

<img width="516" height="75" alt="Screenshot 2026-01-30 103123" src="https://github.com/user-attachments/assets/54d78347-165a-4b60-8100-59c4010b12f5" />

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


<img width="728" height="57" alt="Screenshot 2026-01-30 104103" src="https://github.com/user-attachments/assets/3fdc9336-9376-4034-b485-e4931e3c67c6" />



egrep -w '(H|h)ello' newfile 
## OUTPUT


<img width="490" height="52" alt="Screenshot 2026-01-30 104120" src="https://github.com/user-attachments/assets/82226990-89c7-4c9a-a4a6-71a10f5a900c" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="489" height="62" alt="Screenshot 2026-01-30 104127" src="https://github.com/user-attachments/assets/5c37bef0-4a6b-4123-9726-d06314d09d49" />




egrep '(world$)' newfile 
## OUTPUT



<img width="511" height="39" alt="Screenshot 2026-01-30 104135" src="https://github.com/user-attachments/assets/bbd3a226-db8c-4316-bec3-625c792a6e0e" />

egrep '(World$)' newfile 
## OUTPUT

<img width="451" height="39" alt="Screenshot 2026-01-30 104143" src="https://github.com/user-attachments/assets/e845c265-bdde-436b-a8a7-8a18bde34bcf" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="388" height="26" alt="Screenshot 2026-01-30 104151" src="https://github.com/user-attachments/assets/baa465bf-8017-4ac4-a6e7-ac200257984d" />



egrep '[1-9]' newfile 
## OUTPUT


<img width="437" height="56" alt="Screenshot 2026-01-30 104159" src="https://github.com/user-attachments/assets/b5ff3d59-511c-4899-8269-d3a9e2a32887" />


egrep 'Linux.*world' newfile 
## OUTPUT


<img width="387" height="33" alt="Screenshot 2026-01-30 104207" src="https://github.com/user-attachments/assets/b2567e96-9186-44c7-baca-82eff34c1cdf" />

egrep 'Linux.*World' newfile 
## OUTPUT

<img width="537" height="47" alt="Screenshot 2026-01-30 104250" src="https://github.com/user-attachments/assets/1e42d739-0e6c-4b8d-9069-a6adafede552" />


egrep l{2} newfile
## OUTPUT


<img width="576" height="75" alt="Screenshot 2026-01-30 104312" src="https://github.com/user-attachments/assets/93acd12e-402c-474d-8675-6377fa907039" />


<img width="377" height="46" alt="Screenshot 2026-01-30 104304" src="https://github.com/user-attachments/assets/94cd8272-8101-49d7-8a3d-8150abbb94f0" />

egrep 's{1,2}' newfile
## OUTPUT 

<img width="576" height="75" alt="Screenshot 2026-01-30 104312" src="https://github.com/user-attachments/assets/b2f80927-744a-4a05-8687-9b126af3b70b" />


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


<img width="563" height="52" alt="Screenshot 2026-01-30 104322" src="https://github.com/user-attachments/assets/e3d7ddc8-4901-48b9-8114-4f37c1dbd5b7" />


sed -n -e '$p' file23
## OUTPUT


<img width="635" height="68" alt="Screenshot 2026-01-30 104330" src="https://github.com/user-attachments/assets/dd2c1e95-e7fd-40be-a2bb-f34dc6ecbb82" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT


<img width="694" height="230" alt="Screenshot 2026-01-30 104336" src="https://github.com/user-attachments/assets/1e98ee12-cf6e-4ea1-9d19-ad2940fa8e94" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT


<img width="675" height="231" alt="Screenshot 2026-01-30 104344" src="https://github.com/user-attachments/assets/34d2acba-c9cb-42b1-b8c0-0176f464c8ab" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT


<img width="676" height="225" alt="Screenshot 2026-01-30 104353" src="https://github.com/user-attachments/assets/0ad40da5-7ff5-4f62-ae6b-3764d76fde5f" />


sed -n -e '1,5p' file23
## OUTPUT


<img width="676" height="160" alt="Screenshot 2026-01-30 104400" src="https://github.com/user-attachments/assets/337c0f22-71f0-4ba4-b50e-b9e76de991e5" />


sed -n -e '2,/Joe/p' file23
## OUTPUT



<img width="659" height="116" alt="Screenshot 2026-01-30 104407" src="https://github.com/user-attachments/assets/efe697ed-302c-4859-8fad-db781511ab80" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT



<img width="661" height="91" alt="Screenshot 2026-01-30 104415" src="https://github.com/user-attachments/assets/69073241-64a5-49fc-ab91-a5e4861f3909" />

seq 10 
## OUTPUT


<img width="679" height="269" alt="Screenshot 2026-01-30 104423" src="https://github.com/user-attachments/assets/a08ff044-6974-4eef-b9f0-14ca669e9cc7" />


seq 10 | sed -n '4,6p'
## OUTPUT


<img width="660" height="124" alt="Screenshot 2026-01-30 104433" src="https://github.com/user-attachments/assets/b06f1744-5ab2-46ae-89a0-b43cc9931170" />


seq 10 | sed -n '2,~4p'
## OUTPUT


<img width="623" height="120" alt="Screenshot 2026-01-30 104439" src="https://github.com/user-attachments/assets/a25279e5-7e8b-4d45-9055-2ef2a9ee9245" />


seq 3 | sed '2a hello'
## OUTPUT


<img width="609" height="142" alt="Screenshot 2026-01-30 104446" src="https://github.com/user-attachments/assets/8fd0daf4-51b0-4a0e-b78f-20d19c97f13f" />


seq 2 | sed '2i hello'
## OUTPUT


<img width="680" height="117" alt="Screenshot 2026-01-30 104456" src="https://github.com/user-attachments/assets/0d018090-bc0c-4fb1-8456-531cc5a6db28" />

seq 10 | sed '2,9c hello'
## OUTPUT

<img width="627" height="122" alt="Screenshot 2026-01-30 104504" src="https://github.com/user-attachments/assets/68bd55ff-05aa-4809-a676-27b83edf6d87" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="631" height="124" alt="Screenshot 2026-01-30 104511" src="https://github.com/user-attachments/assets/06146967-3dc2-4525-a048-367954f5f2b2" />



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

<img width="619" height="196" alt="Screenshot 2026-01-30 104524" src="https://github.com/user-attachments/assets/e8bc53df-01c6-4eed-8141-b84ca61c3f79" />


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



<img width="615" height="170" alt="Screenshot 2026-01-30 104530" src="https://github.com/user-attachments/assets/aa5281cc-3abe-4578-a663-256c88cd78a1" />

#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="664" height="236" alt="Screenshot 2026-01-30 104535" src="https://github.com/user-attachments/assets/6b09e53e-1c72-4f4a-b441-c476e93058c2" />

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


<img width="503" height="146" alt="Screenshot 2026-01-30 104542" src="https://github.com/user-attachments/assets/dd44c624-acf9-4a19-8cd5-92521ea8c831" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT


<img width="645" height="145" alt="Screenshot 2026-01-30 104549" src="https://github.com/user-attachments/assets/52180732-1993-4d9a-b13b-7f3aa5b90f6a" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="708" height="734" alt="Screenshot 2026-01-30 110327" src="https://github.com/user-attachments/assets/7be5ac00-2053-417a-900c-a3ee808d44dd" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="1025" height="711" alt="Screenshot 2026-01-30 110338" src="https://github.com/user-attachments/assets/b2e2fbf2-c505-4ac0-ad41-efb9e9da011b" />


tar -xvf backup.tar
## OUTPUT

<img width="1016" height="715" alt="Screenshot 2026-01-30 110351" src="https://github.com/user-attachments/assets/c69f92eb-3e8b-43a9-af64-85fcb9cbfe96" />

gzip backup.tar

ls .gz
## OUTPUT

<img width="971" height="67" alt="Screenshot 2026-01-30 110359" src="https://github.com/user-attachments/assets/aec891ff-fa07-4ce9-999f-94d5bb710b32" />
 
gunzip backup.tar.gz
## OUTPUT

<img width="1021" height="81" alt="Screenshot 2026-01-30 110410" src="https://github.com/user-attachments/assets/30cd56bf-82c0-48b5-b393-ad8a29e171bc" />

 
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


 
ls file1
## OUTPUT


echo $?
## OUTPUT 
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


<img width="803" height="248" alt="Screenshot 2026-01-30 110541" src="https://github.com/user-attachments/assets/f11660ce-b3af-4049-b19b-f56203e2cf6e" />


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

<img width="834" height="137" alt="Screenshot 2026-01-30 110551" src="https://github.com/user-attachments/assets/5936e5c9-386d-4d8c-9024-6c332133106d" />


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


<img width="906" height="195" alt="Screenshot 2026-01-30 110625" src="https://github.com/user-attachments/assets/6c340889-60ea-4b43-bb6b-13bfdeb00cc7" />

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


Screenshot 2026-01-30 110653
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

<img width="592" height="156" alt="Screenshot 2026-01-30 110707" src="https://github.com/user-attachments/assets/5bda88c9-d286-453d-a359-73663501eabb" />

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

<img width="596" height="167" alt="Screenshot 2026-01-30 110714" src="https://github.com/user-attachments/assets/dd705561-d4f5-4d2f-8e04-56caf35e6511" />
 
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

<img width="736" height="262" alt="Screenshot 2026-01-30 110721" src="https://github.com/user-attachments/assets/0378fd6f-3f10-4ac6-aa7d-17fee5d4ac95" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT



<img width="498" height="193" alt="Screenshot 2026-01-30 110729" src="https://github.com/user-attachments/assets/26b99893-b9df-41d6-b90f-bc15b22a86c9" />

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


 <img width="614" height="220" alt="Screenshot 2026-01-30 110735" src="https://github.com/user-attachments/assets/f441b733-90c6-4c6d-8802-f254e47b1d79" />

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

<img width="365" height="119" alt="Screenshot 2026-01-30 110741" src="https://github.com/user-attachments/assets/a65f3ce6-7d38-481e-b302-03be9c26f8c4" />

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

<img width="512" height="119" alt="Screenshot 2026-01-30 110748" src="https://github.com/user-attachments/assets/4fdd405c-53c6-47fe-8aa3-c900ef1e097e" />

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
 

 <img width="599" height="164" alt="Screenshot 2026-01-30 111634" src="https://github.com/user-attachments/assets/5ab09988-91df-45a6-8f9c-58ffe9e90562" />

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

 <img width="705" height="389" alt="Screenshot 2026-01-30 111654" src="https://github.com/user-attachments/assets/f83de40a-3b79-4e36-ada9-a53af79a31bc" />

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



# RESULT:
The Commands are executed successfully.
