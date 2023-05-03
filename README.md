Download Link: https://assignmentchef.com/product/solved-cs2211a-lab-no-4-introduction-to-unix
<br>
The objective of this lab is:

o to practice Unix Shell Programming

If you would like to leave, and at least 30 minuteshave passed, raise your hand and wait for the TA.

Show the TA what you did. If, and only if, you did a reasonable effort during the lab, he/she will give you the lab mark.

<strong>==================================================================================== </strong>

<ol>

 <li>Consider the following shell script <strong>Q1</strong></li>

</ol>

#!/bin/sh x=$2

echo  $1      $x $* echo `$1      $x $*` echo ”$1      $x $*” echo ’$1      $x $*’ echo $# shift

echo  $1      $x $* echo `$1      $x $*` echo ”$1      $x $*” echo ’$1      $x $*’

echo $#

Understand and trace the script using –x and –xv options when calling it with the following arguments (try to expect the output before you execute the command):

<ol>

 <li>Q1 pwd echo</li>

 <li>Q1 echo pwd</li>

 <li>#!/bin/sh X=$1 echo $X shift while [ $# -gt 0 ]; do   echoConsider the shell script <strong>Q2</strong>: $1   if [ $1 -gt $X ]; then     X=$1     echo ”   &lt;&lt; $X”   fi   shift done echo ”—–”;  echo $X</li>

</ol>

Understand and trace the script using –x and –xv options when calling it with the following arguments (try to expect the output before you execute the command):

Q2 11 4 19 7 31 49 1 6




Copyright © 2015 Mahmoud El-Sakka.

<ol start="3">

 <li>Change your current shell to Bourne shell (by executing sh command). Delete any file or directory called ~/abc,  what is the <em>printable</em> <em>output</em> of the following Unix commands:</li>

</ol>

cd; mkdir abc;   ABC=abc;   echo “ls -a $ABC”;   echo `ls -a $ABC | wc -w`

<ol start="4">

 <li>Explain what happens when you execute the following shell script</li>

</ol>

#!/bin/sh # echo hour=`date +%H` if [ ”$hour” -lt 12 ] then

echo ”GOOD MORNING” elif [ ”$hour” -lt 18 ]   then

echo ”GOOD AFTERNOON”   else

echo ”GOOD EVENING” fi echo




If you decided not to use “elif”, what you should change in the program to keep it works the same way.

<ol start="5">

 <li>Consider you executed the following command:</li>

</ol>

(echo a b c; echo 1 2 3) &gt; data_file

Also consider that you have a shell script called script.sh as listed below:

#!/bin/sh while <strong>read a b</strong>  do

echo $a $a $b $b $c $c   echo $a $a $b $b $c $c done

Trace and explain the output of the following command: script.sh &lt; data_file | tr ’a-z’ ’A-Z’

<ol start="6">

 <li>Explain what happens when you execute the following commands: pwd rm –r new_dir mkdir new_dir cd new_dir</li>

</ol>




cat &lt;&lt;+ &gt; new_file

#!/bin/sh




echo ”I am inside new_file”

echo ”Current directory is `pwd`”




chmod u+x new_file

/bin/ls –l `/bin/ls` cd .. rm -r new_dir pwd

<ol start="7">

 <li>Write a Bourne shell script that takes a seconds as a positive integer argument (less than 86400) representing the number of seconds since midnight and returns the equivalent time in hours (0-23), minutes (0-59), and seconds (0-59), respectively.</li>

</ol>


