0

Create a script that switches the current user to the user betty.

#!/bin/bash

su betty



chmod u+x 0-iam_betty



1

Write a script that prints the effective username of the current user.



#!/bin/bash

whoami



chmod u+x 1-who_am_i



2)

Write a script that prints all the groups the current user is part of.

2-groups



#!/bin/bash

groups



chmod u+x 2-groups



3) Write a script that changes the owner of the file hello to the user betty.

3-new_owner



#!/bin/bash

sudo chown betty hello



chmod u+x 3-new_owner





4) Write a script that creates an empty file called hello.



4-empty



#!/bin/bash                              

touch hello



chmod u+x 4-empty



5)

Write a script that adds execute permission to the owner of the file hello.

5-execute



#!/bin/bash

chmod u+x hello



chmod u+x 5-execute





6)

Write a script that adds execute permission to the owner and the group owner, and read permission to other users, to the file hello.

6-multiple_permissions



#!/bin/bash

chmod ug+x,o+r hello



chmod u+x 6-multiple_permissions



7)

Write a script that adds execution permission to the owner, the group owner and the other users, to the file hello

7-everybody



#!/bin/bash

chmod ugo+x hello



chmod u+x 7-everybody



8



Write a script that sets the permission to the file hello as follows:

Owner: no permission at all

Group: no permission at all

Other users: all the permissions



8-James_Bond



#!/bin/bash

chmod 007 hello



chmod u+x 8-James_Bond



9



Write a script that sets the mode of the file hello to this:

-rwxr-x-wx 1 julien julien 23 Sep 20 14:25 hello

9-John_Doe





#!/bin/bash

chmod 753 hello



chmod u+x 9-John_Doe





10



Write a script that sets the mode of the file hello the same as olleh’s mode.



The file hello will be in the working directory

The file olleh will be in the working directory



10-mirror_permissions



#!/bin/bash

chmod --reference=olleh hello



chmod u+x 10-mirror_permissions





11

Create a script that adds execute permission to all subdirectories of the current directory for the owner, the group owner and all other users. Regular files should not be changed.



11-directories_permissions



#!/bin/bash

chmod -R +111 */



chmod u+x 11-directories_permissions



12

Create a script that creates a directory called my_dir with permissions 751 in the working directory.



12-directory_permissions



#!/bin/bash

mkdir -m 751 my_dir



chmod u+x 12-directory_permissions



13

Write a script that changes the group owner to school for the file hello



13-change_group



#!/bin/bash

chgrp School hello



chmod u+x 13-change_group





14

Write a script that changes the owner to vincent and the group owner to staff for all the files and directories in the working directory.

100-change_owner_and_group



#!/bin/bash

chown -h vincent:staff *



chmod u+x 100-change_owner_and_group





15

Write a script that changes the owner and the group owner of _hello to vincent and staff respectively.



The file _hello is in the working directory

The file _hello is a symbolic link



101-symbolic_link_permissions



#!/bin/bash

chown -h vincent:staff _hello



chmod u+x 101-symbolic_link_permissions



16

Write a script that changes the owner of the file hello to betty only if it is owned by the user guillaume.



The file hello will be in the working directory



102-if_only



#!/bin/bash

chown --from=guillaume betty hello



chmod u+x 102-if_only





17



Write a script that will play the StarWars IV episode in the terminal.

103-Star_Wars



#!/bin/bash

telnet towel.blinkenlights.nl

telnet tower.blinkenlights.nl







chmod u+x 103-Star_Wars













git add .

git commit -m "commit"

git push


