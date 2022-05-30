QUESTIONS



0)

0. Hello World

mandatory

Write a script that prints “Hello, World”, followed by a new line to the standard output.



Repo:



GitHub repository: alx-system_engineering-devops

Directory: 0x02-shell_redirections

File: 0-hello_world



#!/bin/bash

echo "Hello, World"





chmod u+x 0-hello_world



1) 1. Confused smiley

mandatory

Write a script that displays a confused smiley "(Ôo)'.



julien@ubuntu:/tmp/h$ ./1-confused_smiley 

"(Ôo)'

julien@ubuntu:/tmp/h$ 

Repo:



GitHub repository: alx-system_engineering-devops

Directory: 0x02-shell_redirections

File: 1-confused_smiley



#!/bin/bash

echo "\"(Ôo)'"



chmod u+x 1-confused_smiley







2. Let's display a file

mandatory

Display the content of the /etc/passwd file.



Example:



$ ./2-hellofile

##

# User Database

#

# Note that this file is consulted directly only when the system is running

# in single-user mode. At other times this information is provided by

# Open Directory.

#

# See the opendirectoryd(8) man page for additional information about

# Open Directory.

##

nobody:*:-2:-2:Unprivileged User:/var/empty:/usr/bin/false

root:*:0:0:System Administrator:/var/root:/bin/sh

daemon:*:1:1:System Services:/var/root:/usr/bin/false

_uucp:*:4:4:Unix to Unix Copy Protocol:/var/spool/uucp:/usr/sbin/uucico

_taskgated:*:13:13:Task Gate Daemon:/var/empty:/usr/bin/false

_networkd:*:24:24:Network Services:/var/networkd:/usr/bin/false

_installassistant:*:25:25:Install Assistant:/var/empty:/usr/bin/false

_lp:*:26:26:Printing Services:/var/spool/cups:/usr/bin/false

_postfix:*:27:27:Postfix Mail Server:/var/spool/postfix:/usr/bin/false

_scsd:*:31:31:Service Configuration Service:/var/empty:/usr/bin/false

_ces:*:32:32:Certificate Enrollment Service:/var/empty:/usr/bin/false

_mcxalr:*:54:54:MCX AppLaunch:/var/empty:/usr/bin/false

_krbfast:*:246:-2:Kerberos FAST Account:/var/empty:/usr/bin/false

$

Repo:



GitHub repository: alx-system_engineering-devops

Directory: 0x02-shell_redirections

File: 2-hellofile



#!/bin/bash

/etc/passwd





chmod u+x 2-hellofile



3. What about 2?

mandatory

Display the content of /etc/passwd and /etc/hosts



Example:



$ ./3-twofiles

##

# User Database

#

# Note that this file is consulted directly only when the system is running

# in single-user mode. At other times this information is provided by

# Open Directory.

#

# See the opendirectoryd(8) man page for additional information about

# Open Directory.

##

nobody:*:-2:-2:Unprivileged User:/var/empty:/usr/bin/false

root:*:0:0:System Administrator:/var/root:/bin/sh

daemon:*:1:1:System Services:/var/root:/usr/bin/false

##

# Host Database

#

# localhost is used to configure the loopback interface

# when the system is booting. Do not change this entry.

##

127.0.0.1   localhost

255.255.255.255 broadcasthost

::1 localhost

$

Repo:



GitHub repository: alx-system_engineering-devops

Directory: 0x02-shell_redirections

File: 3-twofiles





#!/bin/bash

cat /etc/passwd /etc/hosts







chmod u+x 3-twofiles





4)

4. Last lines of a file

mandatory

Display the last 10 lines of /etc/passwd



Example:



$ ./4-lastlines

_assetcache:*:235:235:Asset Cache Service:/var/empty:/usr/bin/false

_coremediaiod:*:236:236:Core Media IO Daemon:/var/empty:/usr/bin/false

_launchservicesd:*:239:239:_launchservicesd:/var/empty:/usr/bin/false

_iconservices:*:240:240:IconServices:/var/empty:/usr/bin/false

_distnote:*:241:241:DistNote:/var/empty:/usr/bin/false

_nsurlsessiond:*:242:242:NSURLSession Daemon:/var/db/nsurlsessiond:/usr/bin/false

_nsurlstoraged:*:243:243:NSURLStorage Daemon:/var/empty:/usr/bin/false

_displaypolicyd:*:244:244:Display Policy Daemon:/var/empty:/usr/bin/false

_astris:*:245:245:Astris Services:/var/db/astris:/usr/bin/false

_krbfast:*:246:-2:Kerberos FAST Account:/var/empty:/usr/bin/false



Tips: “Thinks of it as a cat, what is at the end of it?”



Repo:



GitHub repository: alx-system_engineering-devops

Directory: 0x02-shell_redirections

File: 4-lastlines





#!/bin/bash

tail /etc/passwd





chmod u+x 4-lastlines



5. I'd prefer the first ones actually

mandatory

Display the first 10 lines of /etc/passwd



Example:



$ ./5-firstlines

##

# User Database

#

# Note that this file is consulted directly only when the system is running

# in single-user mode. At other times this information is provided by

# Open Directory.

#

# See the opendirectoryd(8) man page for additional information about

# Open Directory.

##

$

Repo:



GitHub repository: alx-system_engineering-devops

Directory: 0x02-shell_redirections

File: 5-firstlines



#!/bin/bash

head /etc/passwd



chmod u+x 5-firstlines



6. Line #2

mandatory

Write a script that displays the third line of the file iacta.



The file iacta will be in the working directory



You’re not allowed to use sed

julien@ubuntu:/tmp/h$ cat iacta 

Alea iacta est



Alea iacta est ("The die is cast") is a Latin phrase attributed by Suetonius

(as iacta alea est) to Julius Caesar on January 10, 49 BC

as he led his army across the Rubicon river in Northern Italy. With this step,

he entered Italy at the head of his army in defiance of the Senate and began

his long civil war against Pompey and the Optimates. The phrase has been

adopted in Italian (Il dado è tratto), Romanian (Zarurile au fost aruncate),

Spanish (La suerte está echada), French (Les dés sont jetés), Portuguese (A

sorte está lançada), Dutch (De teerling is geworpen),

German (Der Würfel ist gefallen), Hungarian (A kocka el van vetve) and many other languages to

indicate that events have passed a point of no return.



Read more: https://en.wikipedia.org/wiki/Alea_iacta_est

julien@ubuntu:/tmp/h$ ./6-third_line 

Alea iacta est ("The die is cast") is a Latin phrase attributed by Suetonius

julien@ubuntu:/tmp/h$ 

Note: The output will differ, depending on the content of the file iacta.



Repo:



GitHub repository: alx-system_engineering-devops

Directory: 0x02-shell_redirections

File: 6-third_line





#!/bin/bash

head -n 3 iacta | tail -n 1       wrong







chmod u+x 6-third_line



7. It is a good file that cuts iron without making a noise

mandatory

Write a shell script that creates a file named exactly \*\\'"Best School"\'\\*$\?\*\*\*\*\*:) containing the text Best School ending by a new line.



julien@ubuntu:~/shell$ ls && ./7-file && ls -l && cat -e \\*

0-mac_and_cheese 7-file 7-file~ Makefile

total 20

-rwxrw-r-- 1 julien julien 79 Jan 20 06:24 0-mac_and_cheese

-rwxrw-r-- 1 julien julien 90 Jan 20 06:40 7-file

-rwxrw-r-- 1 julien julien 69 Jan 20 06:37 7-file~

-rw-rw-r-- 1 julien julien 14 Jan 20 06:38 Makefile

-rw-rw-r-- 1 julien julien 17 Jan 20 06:40 '\*\\'"Best School"\'\\*$\?\*\*\*\*\*:)'

Best School$

julien@ubuntu:~/shell$

Repo:



GitHub repository: alx-system_engineering-devops

Directory: 0x02-shell_redirections

File: 7-file







#!/bin/bash

echo "Best School" | cat > '\*\\'\''"Best School"\'\''\\*$\?\*\*\*\*\*:)'







chmod u+x 7-file





8. Save current state of directory

mandatory

Write a script that writes into the file ls_cwd_content the result of the command ls -la. If the file ls_cwd_content already exists, it should be overwritten. If the file ls_cwd_content does not exist, create it.



julien@ubuntu:/tmp/h$ ls -la

total 20

drwxrwxr-x  2 julien julien 4096 Sep 20 18:18 .

drwxrwxrwt 13 root   root   4096 Sep 20 18:18 ..

-rwxrw-r--  1 julien julien   36 Sep 20 18:18 8-cwd_state

-rw-rw-r--  1 betty  julien   23 Sep 20 14:25 hello

-rw-rw-r--  1 julien julien  926 Sep 20 17:52 iacta

julien@ubuntu:/tmp/h$ ./8-cwd_state 

julien@ubuntu:/tmp/h$ ls -la

total 24

drwxrwxr-x  2 julien julien 4096 Sep 20 18:18 .

drwxrwxrwt 13 root   root   4096 Sep 20 18:18 ..

-rwxrw-r--  1 julien julien   36 Sep 20 18:18 8-cwd_state

-rw-rw-r--  1 betty  julien   23 Sep 20 14:25 hello

-rw-rw-r--  1 julien julien  926 Sep 20 17:52 iacta

-rw-rw-r--  1 julien julien  329 Sep 20 18:18 ls_cwd_content

julien@ubuntu:/tmp/h$ cat ls_cwd_content 

total 20

drwxrwxr-x  2 julien julien 4096 Sep 20 18:18 .

drwxrwxrwt 13 root   root   4096 Sep 20 18:18 ..

-rwxrw-r--  1 julien julien   36 Sep 20 18:18 8-cwd_state

-rw-rw-r--  1 betty  julien   23 Sep 20 14:25 hello

-rw-rw-r--  1 julien julien  926 Sep 20 17:52 iacta

-rw-rw-r--  1 julien julien    0 Sep 20 18:18 ls_cwd_content

julien@ubuntu:/tmp/h$ 

Repo:



GitHub repository: alx-system_engineering-devops

Directory: 0x02-shell_redirections

File: 8-cwd_state



#!/bin/bash









chmod u+x 8-cwd_state



8. Save current state of directory

mandatory

Write a script that writes into the file ls_cwd_content the result of the command ls -la. If the file ls_cwd_content already exists, it should be overwritten. If the file ls_cwd_content does not exist, create it.



julien@ubuntu:/tmp/h$ ls -la

total 20

drwxrwxr-x  2 julien julien 4096 Sep 20 18:18 .

drwxrwxrwt 13 root   root   4096 Sep 20 18:18 ..

-rwxrw-r--  1 julien julien   36 Sep 20 18:18 8-cwd_state

-rw-rw-r--  1 betty  julien   23 Sep 20 14:25 hello

-rw-rw-r--  1 julien julien  926 Sep 20 17:52 iacta

julien@ubuntu:/tmp/h$ ./8-cwd_state 

julien@ubuntu:/tmp/h$ ls -la

total 24

drwxrwxr-x  2 julien julien 4096 Sep 20 18:18 .

drwxrwxrwt 13 root   root   4096 Sep 20 18:18 ..

-rwxrw-r--  1 julien julien   36 Sep 20 18:18 8-cwd_state

-rw-rw-r--  1 betty  julien   23 Sep 20 14:25 hello

-rw-rw-r--  1 julien julien  926 Sep 20 17:52 iacta

-rw-rw-r--  1 julien julien  329 Sep 20 18:18 ls_cwd_content

julien@ubuntu:/tmp/h$ cat ls_cwd_content 

total 20

drwxrwxr-x  2 julien julien 4096 Sep 20 18:18 .

drwxrwxrwt 13 root   root   4096 Sep 20 18:18 ..

-rwxrw-r--  1 julien julien   36 Sep 20 18:18 8-cwd_state

-rw-rw-r--  1 betty  julien   23 Sep 20 14:25 hello

-rw-rw-r--  1 julien julien  926 Sep 20 17:52 iacta

-rw-rw-r--  1 julien julien    0 Sep 20 18:18 ls_cwd_content

julien@ubuntu:/tmp/h$ 

Repo:



GitHub repository: alx-system_engineering-devops

Directory: 0x02-shell_redirections

File: 8-cwd_state



#!/bin/bash

ls -la > ls_cwd_content





chmod u+x 8-cwd_state





9. Duplicate last line

mandatory

Write a script that duplicates the last line of the file iacta



The file iacta will be in the working directory

julien@ubuntu:/tmp/h$ cat iacta 

Alea iacta est



Alea iacta est ("The die is cast") is a Latin phrase attributed by Suetonius

(as iacta alea est) to Julius Caesar on January 10, 49 BC

as he led his army across the Rubicon river in Northern Italy. With this step,

he entered Italy at the head of his army in defiance of the Senate and began

his long civil war against Pompey and the Optimates. The phrase has been

adopted in Italian (Il dado è tratto), Romanian (Zarurile au fost aruncate),

Spanish (La suerte está echada), French (Les dés sont jetés), Portuguese (A

sorte está lançada), Dutch (De teerling is geworpen),

German (Der Würfel ist gefallen), Hungarian (A kocka el van vetve) and many other languages to

indicate that events have passed a point of no return.



Read more: https://en.wikipedia.org/wiki/Alea_iacta_est

julien@ubuntu:/tmp/h$ ./9-duplicate_last_line 

julien@ubuntu:/tmp/h$ cat iacta 

Alea iacta est



Alea iacta est ("The die is cast") is a Latin phrase attributed by Suetonius

(as iacta alea est) to Julius Caesar on January 10, 49 BC

as he led his army across the Rubicon river in Northern Italy. With this step,

he entered Italy at the head of his army in defiance of the Senate and began

his long civil war against Pompey and the Optimates. The phrase has been

adopted in Italian (Il dado è tratto), Romanian (Zarurile au fost aruncate),

Spanish (La suerte está echada), French (Les dés sont jetés), Portuguese (A

sorte está lançada), Dutch (De teerling is geworpen),

German (Der Würfel ist gefallen), Hungarian (A kocka el van vetve) and many other languages to

indicate that events have passed a point of no return.



Read more: https://en.wikipedia.org/wiki/Alea_iacta_est

Read more: https://en.wikipedia.org/wiki/Alea_iacta_est

julien@ubuntu:/tmp/h$ 

Repo:



GitHub repository: alx-system_engineering-devops

Directory: 0x02-shell_redirections

File: 9-duplicate_last_line





#!/bin/bash

tail -n 1 iacta >> iacta







chmod u+x 9-duplicate_last_line



10. No more javascript

mandatory

Write a script that deletes all the regular files (not the directories) with a .js extension that are present in the current directory and all its subfolders.

Repo:



GitHub repository: alx-system_engineering-devops

Directory: 0x02-shell_redirections

File: 10-no_more_js



#!/bin/bash



find . -name "*.js" -type f -delete





chmod u+x 10-no_more_js



11. Don't just count your directories, make your directories count

mandatory

Write a script that counts the number of directories and sub-directories in the current directory.



The current and parent directories should not be taken into account

Hidden directories should be counted



GitHub repository: alx-system_engineering-devops

Directory: 0x02-shell_redirections

File: 11-directories





#!/bin/bash



find . -mindepth 1 -type d | wc -l





chmod u+x 11-directories





12. What’s new

Create a script that displays the 10 newest files in the current directory.



Requirements:



One file per line

Sorted from the newest to the oldest



Repo:



GitHub repository: alx-system_engineering-devops

Directory: 0x02-shell_redirections

File: 12-newest_files



#!/bin/bash

ls -t | head







chmod u+x 12-newest_files





13. Being unique is better than being perfect

mandatory

Create a script that takes a list of words as input and prints only words that appear exactly once.



Input format: One line, one word

Output format: One line, one word

Words should be sorted



Repo:



GitHub repository: alx-system_engineering-devops

Directory: 0x02-shell_redirections

File: 13-unique



#!/bin/bash

sort | uniq -u



chmod u+x 13-unique





14. It must be in that file

mandatory

Display lines containing the pattern “root” from the file /etc/passwd



Repo:



GitHub repository: alx-system_engineering-devops

Directory: 0x02-shell_redirections

File: 14-findthatword



#!/bin/bash

grep root /etc/passwd



chmod u+x 14-findthatword





15. Count that word

mandatory

Display the number of lines that contain the pattern “bin” in the file /etc/passwd



Repo:



GitHub repository: alx-system_engineering-devops

Directory: 0x02-shell_redirections

File: 15-countthatword





#!/bin/bash

grep -c bin /etc/passwd

chmod u+x 15-countthatword





16. What's next?

mandatory

Display lines containing the pattern “root” and 3 lines after them in the file /etc/passwd.



Repo:



GitHub repository: alx-system_engineering-devops

Directory: 0x02-shell_redirections

File: 16-whatsnext



#!/bin/bash

cat /etc/passwd | grep -A 3 "root"





chmod u+x 16-whatsnext



17. I hate bins

mandatory

Display all the lines in the file /etc/passwd that do not contain the pattern “bin”.

Repo:



GitHub repository: alx-system_engineering-devops

Directory: 0x02-shell_redirections

File: 17-hidethisword



#!/bin/bash

grep -v bin /etc/passwd







chmod u+x 17-hidethisword



18. Letters only please

mandatory

Display all lines of the file /etc/ssh/sshd_config starting with a letter.



include capital letters as well



Repo:



GitHub repository: alx-system_engineering-devops

Directory: 0x02-shell_redirections

File: 18-letteronly





#!/bin/bash

grep ^[[:alpha:]]  /etc/ssh/sshd_config







chmod u+x 18-letteronly





19. A to Z

mandatory

Replace all characters A and c from input to Z and e respectively.



Repo:



GitHub repository: alx-system_engineering-devops

Directory: 0x02-shell_redirections

File: 19-AZ



#!/bin/bash

tr 'Ac' 'Ze'



chmod u+x 19-AZ



20. Without C, you would live in hiago

mandatory

Create a script that removes all letters c and C from input.







GitHub repository: alx-system_engineering-devops

Directory: 0x02-shell_redirections

File: 20-hiago



#!/bin/bash

tr -d 'Cc'





chmod u+x 20-hiago



21. esreveR

mandatory

Write a script that reverse its input.







GitHub repository: alx-system_engineering-devops

Directory: 0x02-shell_redirections

File: 21-reverse



#!/bin/bash

rev



chmod u+x 21-reverse







22. DJ Cut Killer

mandatory

Write a script that displays all users and their home directories, sorted by users.



Based on the the /etc/passwd file



Repo:



GitHub repository: alx-system_engineering-devops

Directory: 0x02-shell_redirections

File: 22-users_and_homes



#!/bin/bash

cut -d":" --fields=1,6 /etc/passwd | sort



chmod u+x 22-users_and_homes



23. Empty casks make the most noise

#advanced

Write a command that finds all empty files and directories in the current directory and all sub-directories.



Only the names of the files and directories should be displayed (not the entire path)

Hidden files should be listed

One file name per line

The listing should end with a new line

You are not allowed to use basename, grep, egrep, fgrep or rgrep





Repo:



GitHub repository: alx-system_engineering-devops

Directory: 0x02-shell_redirections

File: 100-empty_casks



#!/bin/bash

find . -empty -printf "%f\n"





chmod u+x 100-empty_casks



24. A gif is worth ten thousand words

#advanced

Write a script that lists all the files with a .gif extension in the current directory and all its sub-directories.



Hidden files should be listed

Only regular files (not directories) should be listed

The names of the files should be displayed without their extensions

The files should be sorted by byte values, but case-insensitive (file aaa should be listed before file bbb, file .b should be listed before file a, and file Rona should be listed after file jay)

One file name per line

The listing should end with a new line

You are not allowed to use basename, grep, egrep, fgrep or rgrep

   

Repo:



GitHub repository: alx-system_engineering-devops

Directory: 0x02-shell_redirections

File: 101-gifs





#!/bin/bash

find . -type f -name "*.gif" -printf "%f\n"| rev | cut -d '.' -f2- | rev | LC_ALL=C sort -f





chmod u+x 101-gifs





25. Acrostic

#advanced

An acrostic is a poem (or other form of writing) in which the first letter (or syllable, or word) of each line (or paragraph, or other recurring feature in the text) spells out a word, message or the alphabet. The word comes from the French acrostiche from post-classical Latin acrostichis). As a form of constrained writing, an acrostic can be used as a mnemonic device to aid memory retrieval. Read more.



Create a script that decodes acrostics that use the first letter of each line.



The ‘decoded’ message has to end with a new line

You are not allowed to use grep, egrep, fgrep or rgrep



Repo:



GitHub repository: alx-system_engineering-devops

Directory: 0x02-shell_redirections

File: 102-acrostic



#!/bin/bash

echo -ne $(cut -c-1 | tr -d '\n')'\n'



chmod u+x 102-acrostic



26. The biggest fan

#advanced

Write a script that parses web servers logs in TSV format as input and displays the 11 hosts or IP addresses which did the most requests.



Order by number of requests, most active host or IP at the top

You are not allowed to use grep, egrep, fgrep or rgrep

Format:





Repo:



GitHub repository: alx-system_engineering-devops

Directory: 0x02-shell_redirections

File: 103-the_biggest_fan



#!/bin/bash

tail -n +2 | cut -f1 | sort | uniq -c | sort -nr -k 1,1 | cut -c 9- | head -11



chmod u+x 103-the_biggest_fan
