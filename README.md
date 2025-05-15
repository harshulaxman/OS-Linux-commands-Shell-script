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
![Screenshot 2025-05-12 215745](https://github.com/user-attachments/assets/443a7577-6739-466c-900f-b531bec57baf)


cat < file2
## OUTPUT
![Screenshot 2025-05-12 215819](https://github.com/user-attachments/assets/a9d36818-421e-448b-981a-61e6c0d068a9)


# Comparing Files
cmp file1 file2
## OUTPUT
![Screenshot 2025-05-12 215856](https://github.com/user-attachments/assets/9ac5a990-9625-42e5-a64a-9803af55c646)

 
comm file1 file2
 ## OUTPUT
  ![Screenshot 2025-05-12 215920](https://github.com/user-attachments/assets/e08935a6-4245-4353-a755-f0925d386e19)

 
diff file1 file2
## OUTPUT
![Screenshot 2025-05-12 220028](https://github.com/user-attachments/assets/0977aafb-4a81-4413-a783-665fad4d4eac)



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
![Screenshot 2025-05-12 220125](https://github.com/user-attachments/assets/f85470f9-2ed8-4ff5-bec6-d75f28651db8)




cut -d "|" -f 1 file22
## OUTPUT
![Screenshot 2025-05-12 220157](https://github.com/user-attachments/assets/d13f6f9e-f8cb-47d4-8af4-71433bd56756)



cut -d "|" -f 2 file22
## OUTPUT
![Screenshot 2025-05-12 220332](https://github.com/user-attachments/assets/13c72370-0df8-464e-825e-066dc03985f6)


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
![Screenshot 2025-05-12 220403](https://github.com/user-attachments/assets/99b81561-c98b-4be1-91ce-92858b4bb560)



grep hello newfile 
## OUTPUT
![Screenshot 2025-05-12 220440](https://github.com/user-attachments/assets/f494c7d1-50c2-45fe-9bc2-40eea2c8fd11)




grep -v hello newfile 
## OUTPUT
![Screenshot 2025-05-12 220712](https://github.com/user-attachments/assets/2bc07266-d73a-4e40-9d55-dffd1d7bb306)



cat newfile | grep -i "hello"
## OUTPUT
![Screenshot 2025-05-12 220740](https://github.com/user-attachments/assets/466d45b0-806e-47af-8e47-96ab958a44d3)




cat newfile | grep -i -c "hello"
## OUTPUT
![Screenshot 2025-05-12 220809](https://github.com/user-attachments/assets/f7f18d90-b388-41dc-95d4-00e70e56b275)




grep -R ubuntu /etc
## OUTPUT
![Screenshot 2025-05-12 220848](https://github.com/user-attachments/assets/e72f7d0f-4f96-4bc8-b608-9196a2d644b1)



grep -w -n world newfile   
## OUTPUT
![Screenshot 2025-05-12 220912](https://github.com/user-attachments/assets/9521eaa8-22dc-4949-996f-895bf4a0d5e7)


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
![Screenshot 2025-05-12 220938](https://github.com/user-attachments/assets/0fa3814a-d3ac-4fa1-9e13-4d60c45b48e0)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![Screenshot 2025-05-12 221028](https://github.com/user-attachments/assets/4315e409-75c0-44bf-9918-148fa53f345d)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
 ![Screenshot 2025-05-12 221101](https://github.com/user-attachments/assets/9287fb22-e6be-4d96-956d-d2fbe4dc9c13)




egrep '(^hello)' newfile 
## OUTPUT
![Screenshot 2025-05-12 221128](https://github.com/user-attachments/assets/c91134fc-fd0a-4d55-8b96-55a8fba0cb9a)



egrep '(world$)' newfile 
## OUTPUT
![Screenshot 2025-05-12 221228](https://github.com/user-attachments/assets/6a50204c-d91f-4340-b4ac-9937b96d6aee)



egrep '(World$)' newfile 
## OUTPUT
 ![Screenshot 2025-05-12 221327](https://github.com/user-attachments/assets/bbafd92a-405d-40bd-87a2-922d49f0e12a)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![Screenshot 2025-05-12 221349](https://github.com/user-attachments/assets/b215938d-ed67-441d-9e06-0ff6db5ac348)



egrep '[1-9]' newfile 
## OUTPUT
![Screenshot 2025-05-12 221411](https://github.com/user-attachments/assets/3fb56ad6-d4e6-4f41-ad98-1532c5a0ca92)



egrep 'Linux.*world' newfile 
## OUTPUT
![Screenshot 2025-05-12 221432](https://github.com/user-attachments/assets/abeb803f-f0fd-4963-9f2c-64cd1dde8fb8)


egrep 'Linux.*World' newfile 
## OUTPUT
![Screenshot 2025-05-12 221523](https://github.com/user-attachments/assets/e9e63212-bace-44a8-b4ca-ef34f41401fb)


egrep l{2} newfile
## OUTPUT
![Screenshot 2025-05-12 221545](https://github.com/user-attachments/assets/d9e53e56-b77f-4e4d-8da4-26693c6829aa)




egrep 's{1,2}' newfile
## OUTPUT 
![Screenshot 2025-05-12 221928](https://github.com/user-attachments/assets/5dfd5231-0e4d-420e-8582-fd0db0b395b5)



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
![Screenshot 2025-05-12 222007](https://github.com/user-attachments/assets/80386ba8-0087-4100-aa4c-b458f1c0b58d)



sed -n -e '$p' file23
## OUTPUT
 ![Screenshot 2025-05-12 222033](https://github.com/user-attachments/assets/1b621b24-33f7-4df4-aca6-388f51ded144)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![Screenshot 2025-05-12 222101](https://github.com/user-attachments/assets/7604a6ce-c17c-43a7-92cb-21bd028cfc9c)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
 ![Screenshot 2025-05-12 222123](https://github.com/user-attachments/assets/06a1728b-d616-4fe9-9ee6-eb8af6b9108a)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
 ![Screenshot 2025-05-12 222152](https://github.com/user-attachments/assets/cfa3c17f-bf7d-43a8-8471-cdab7cc2d518)



sed -n -e '1,5p' file23
## OUTPUT
 ![Screenshot 2025-05-12 222228](https://github.com/user-attachments/assets/606db099-ba44-4ab5-b8bb-b0c96d57e6cb)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![Screenshot 2025-05-12 222300](https://github.com/user-attachments/assets/1078c081-e84d-4e7a-96a0-68f45dd24342)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![Screenshot 2025-05-12 222323](https://github.com/user-attachments/assets/49635ce4-a16b-424a-bfdb-2a7fc4446ece)
 


seq 10 
## OUTPUT
![Screenshot 2025-05-12 222346](https://github.com/user-attachments/assets/d9172bf3-5bb9-4900-b07d-255cd931d4df)



seq 10 | sed -n '4,6p'
## OUTPUT
 ![Screenshot 2025-05-12 222430](https://github.com/user-attachments/assets/6b5ddb61-01c7-4d2e-8cfd-bd86d222902b)



seq 10 | sed -n '2,~4p'
## OUTPUT
 ![Screenshot 2025-05-12 222453](https://github.com/user-attachments/assets/f7d1cb6d-43f3-4a17-8e97-0c8c8100b014)



seq 3 | sed '2a hello'
## OUTPUT
 ![Screenshot 2025-05-12 222516](https://github.com/user-attachments/assets/aef1d8e6-d4ff-4971-abf8-9d52ea96cbd9)



seq 2 | sed '2i hello'
## OUTPUT
![Screenshot 2025-05-12 222540](https://github.com/user-attachments/assets/17e44063-09cf-482b-a219-94f711d2d235)


seq 10 | sed '2,9c hello'
## OUTPUT
![Screenshot 2025-05-12 222612](https://github.com/user-attachments/assets/a8dcc4d4-0d22-4700-aba2-5720bafdbc3d)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
 ![Screenshot 2025-05-12 222653](https://github.com/user-attachments/assets/f9a7ee25-9dfc-439b-8ec7-b879b3b0a296)



sed -n '2,4{s/$/*/;p}' file23
![Screenshot 2025-05-12 222715](https://github.com/user-attachments/assets/bb6e5a48-a9c6-4f22-8bc3-4ce5070bbb50)


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
![Screenshot 2025-05-12 222741](https://github.com/user-attachments/assets/dac978c9-06ab-45ca-bc12-cc1e393f08f2)


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
 ![Screenshot 2025-05-12 222838](https://github.com/user-attachments/assets/748f16d2-beea-4ac1-a49b-87df3d551e05)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
  ![Screenshot 2025-05-12 222918](https://github.com/user-attachments/assets/869b6e3d-90a6-4730-bf90-04c385e88e54)

  
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
  ![Screenshot 2025-05-12 223016](https://github.com/user-attachments/assets/ad88a2ca-0f55-418f-bf15-8dcd0a7e5ddf)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
 ![Screenshot 2025-05-12 223050](https://github.com/user-attachments/assets/f7977587-a6a2-4028-90b9-942698f96db4)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![Screenshot 2025-05-12 223135](https://github.com/user-attachments/assets/c1c970d8-7edc-4e0b-97c8-58abffcbbb84)


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
 ![Screenshot 2025-05-12 223254](https://github.com/user-attachments/assets/f343579d-e2ed-4391-83b2-da000f18389a)


tar -xvf backup.tar
## OUTPUT
![Screenshot 2025-05-12 223324](https://github.com/user-attachments/assets/6898dffa-17d0-4e75-990e-811e68ca45d6)

 
gzip backup.tar

ls .gz
## OUTPUT
![Screenshot 2025-05-12 223349](https://github.com/user-attachments/assets/4b9794f2-8995-4a6c-b0b0-fde54959eb41)

 
gunzip backup.tar.gz
## OUTPUT
![Screenshot 2025-05-12 223414](https://github.com/user-attachments/assets/d6fe626d-4ffd-40ee-a1e1-46fb698e38fd)


 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![Screenshot 2025-05-12 223504](https://github.com/user-attachments/assets/c4ec3fbc-5a74-41e2-8373-28090b658675)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![Screenshot 2025-05-12 223540](https://github.com/user-attachments/assets/fcda1420-d295-4670-a170-0d474c99c2d8)



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
![Screenshot 2025-05-12 223609](https://github.com/user-attachments/assets/f0951e3a-988f-4f58-8716-9d75e548511b)



 
ls file1
## OUTPUT
![Screenshot 2025-05-12 223631](https://github.com/user-attachments/assets/5aa47fce-683e-4ed4-9095-288185a44834)


echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
![Screenshot 2025-05-12 223708](https://github.com/user-attachments/assets/fc7190c6-2b72-46ea-8d43-f9054a6fc67a)

 
abcd
 
echo $?
 ## OUTPUT
 ![Screenshot 2025-05-12 223801](https://github.com/user-attachments/assets/78eec919-e374-44e6-8e07-bcb7689c17e8)



 
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
![Screenshot 2025-05-12 223827](https://github.com/user-attachments/assets/73a9ec46-6028-4e11-ae64-4eb8105dc314)




chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![Screenshot 2025-05-12 223858](https://github.com/user-attachments/assets/872fc34b-484f-4d19-a2a5-e62d652d93ca)



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
![Screenshot 2025-05-12 223931](https://github.com/user-attachments/assets/8c4d3709-1ed1-42d8-8b08-c42ab5ec7c51)


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
![Screenshot 2025-05-12 223959](https://github.com/user-attachments/assets/da8d8ab3-0c97-4954-a371-65fa560dbd16)




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
![Screenshot 2025-05-12 224034](https://github.com/user-attachments/assets/d02866bb-24d1-400a-823c-42c8662bd604)


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
![Screenshot 2025-05-12 224109](https://github.com/user-attachments/assets/408e1caa-85aa-4d74-8a1e-4827af4afea2)


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
![Screenshot 2025-05-12 224137](https://github.com/user-attachments/assets/fbe5a8f7-6d13-4fd6-801f-c8989b43ef08)



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
![Screenshot 2025-05-12 224207](https://github.com/user-attachments/assets/8761c168-61ac-4c63-8aa9-7a009366acbe)


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
![Screenshot 2025-05-12 224248](https://github.com/user-attachments/assets/de215232-a4bc-48a0-8e0c-83c499c761db)

 
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
![Screenshot 2025-05-12 224357](https://github.com/user-attachments/assets/7a14a89a-f818-42a8-b2b5-09b7e4b3a2d9)

 
 
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
![Screenshot 2025-05-12 224505](https://github.com/user-attachments/assets/09020424-3095-4871-a983-a4f4f7e99f4c)

 
 
 
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
![Screenshot 2025-05-12 224534](https://github.com/user-attachments/assets/1ecc65f4-9f42-469c-b421-d94eab6b9f10)

 
 
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
![Screenshot 2025-05-12 224809](https://github.com/user-attachments/assets/a5b03ac3-15fb-4364-9ae2-39297bdd856d)

 
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
![Screenshot 2025-05-12 224658](https://github.com/user-attachments/assets/c979d796-b569-4618-8a21-fab3cc31cf70)

 
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
![Screenshot 2025-05-12 224913](https://github.com/user-attachments/assets/b3960c00-106d-4287-9b26-79c8a39ea9b7)

 
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
![Screenshot 2025-05-12 230118](https://github.com/user-attachments/assets/722cbcf0-98ca-4311-895f-a399479f415c)

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
![Screenshot 2025-05-12 230042](https://github.com/user-attachments/assets/b9b6b9d1-ba59-4b74-8047-83851c621b8b)

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
![Screenshot 2025-05-12 230018](https://github.com/user-attachments/assets/2aa458b1-7034-44e6-b6d5-f7741fd3975d)



 
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
![Screenshot 2025-05-12 225913](https://github.com/user-attachments/assets/c3b4eedf-3e9e-43ef-8b94-653c4f48ed8f)


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
 ![Screenshot 2025-05-12 225850](https://github.com/user-attachments/assets/bcd9098a-865b-4ac6-81ff-cf1c3fed1357)

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
![Screenshot 2025-05-12 225825](https://github.com/user-attachments/assets/d2b8d30d-e395-435d-b79e-8a9d6dc4f2e3)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
![Screenshot 2025-05-12 225750](https://github.com/user-attachments/assets/34929f49-3aac-4fab-b20e-b6d946b6af3f)



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

## OUTPUT
$ ./argshift.sh 1 2 3
![Screenshot 2025-05-12 225728](https://github.com/user-attachments/assets/2925c9f3-e88c-4270-a168-900d2f5f190b)

 
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
![Screenshot 2025-05-12 225500](https://github.com/user-attachments/assets/10f4b8e6-ce5a-4152-a534-a138289baf16)

 
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
![Screenshot 2025-05-12 225434](https://github.com/user-attachments/assets/8dce2079-1a34-4224-a4da-502edbee6f7e)



# RESULT:
The Commands are executed successfully.
