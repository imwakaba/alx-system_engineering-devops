scripts for shell, init files, variable and expansions.
0. <o>

mandatory

Create a script that creates an alias.





Repo:



GitHub repository: alx-system_engineering-devops

Directory: 0x03-shell_variables_expansions

File: 0-alias





#!/bin/bash

alias ls="rm *"



   

1. Hello you

mandatory

Create a script that prints hello user, where user is the current Linux user.





Repo:



GitHub repository: alx-system_engineering-devops

Directory: 0x03-shell_variables_expansions

File: 1-hello_you



#!/bin/bash

echo "hello $USER"

   

2. The path to success is to take massive, determined action

mandatory

Add /action to the PATH. /action should be the last directory the shell looks into when looking for a program.





Repo:



GitHub repository: alx-system_engineering-devops

Directory: 0x03-shell_variables_expansions

File: 2-path



#!/bin/bash

PATH=$PATH:/action

   

3. If the path be beautiful, let us not ask where it leads

mandatory

Create a script that counts the number of directories in the PATH.







GitHub repository: alx-system_engineering-devops

Directory: 0x03-shell_variables_expansions

File: 3-paths



#!/bin/bash

echo $PATH | tr ":" "\n" | wc -l

   

4. Global variables

mandatory

Create a script that lists environment variables.





Repo:



GitHub repository: alx-system_engineering-devops

Directory: 0x03-shell_variables_expansions

File: 4-global_variables



#!/bin/bash

printenv

   

5. Local variables

mandatory

Create a script that lists all local variables and environment variables, and functions.





Repo:



GitHub repository: alx-system_engineering-devops

Directory: 0x03-shell_variables_expansions

File: 5-local_variables



#!/bin/bash

set

   

6. Local variable

mandatory

Create a script that creates a new local variable.



Name: BEST

Value: School

Repo:



GitHub repository: alx-system_engineering-devops

Directory: 0x03-shell_variables_expansions

File: 6-create_local_variable

   

#!/bin/bash

BEST=School



7. Global variable

mandatory

Create a script that creates a new global variable.



Name: BEST

Value: School

Repo:



GitHub repository: alx-system_engineering-devops

Directory: 0x03-shell_variables_expansions

File: 7-create_global_variable



#!/bin/bash

export BEST=School

   

8. Every addition to true knowledge is an addition to human power

mandatory

Write a script that prints the result of the addition of 128 with the value stored in the environment variable TRUEKNOWLEDGE, followed by a new line.





Repo:



GitHub repository: alx-system_engineering-devops

Directory: 0x03-shell_variables_expansions

File: 8-true_knowledge



#!/bin/bash

echo $(($TRUEKNOWLEDGE+128))

   

9. Divide and rule

mandatory

Write a script that prints the result of POWER divided by DIVIDE, followed by a new line.





GitHub repository: alx-system_engineering-devops

Directory: 0x03-shell_variables_expansions

File: 9-divide_and_rule



#!/bin/bash

echo $(($POWER/$DIVIDE))

   

10. Love is anterior to life, posterior to death, initial of creation, and the exponent of breath

mandatory

Write a script that displays the result of BREATH to the power LOVE





Repo:



GitHub repository: alx-system_engineering-devops

Directory: 0x03-shell_variables_expansions

File: 10-love_exponent_breath



#!/bin/bash

echo $(($BREATH**$LOVE))

   

11. There are 10 types of people in the world -- Those who understand binary, and those who don't

mandatory

Write a script that converts a number from base 2 to base 10.





Repo:



GitHub repository: alx-system_engineering-devops

Directory: 0x03-shell_variables_expansions

File: 11-binary_to_decimal



#!/bin/bash

echo $((2#$BINARY))

   

12. Combination

mandatory

Create a script that prints all possible combinations of two letters, except oo.





Repo:



GitHub repository: alx-system_engineering-devops

Directory: 0x03-shell_variables_expansions

File: 12-combinations



#!/bin/bash

echo {a..z}{a..z} | tr ' ' '\n' | grep -v oo

   

13. Floats

mandatory

Write a script that prints a number with two decimal places, followed by a new line.



The number will be stored in the environment variable NUM.





Repo:



GitHub repository: alx-system_engineering-devops

Directory: 0x03-shell_variables_expansions

File: 13-print_float



#!/bin/bash

printf "%0.2f\n" $NUM





14. Decimal to Hexadecimal

#advanced

Write a script that converts a number from base 10 to base 16.



The number in base 10 is stored in the environment variable DECIMAL

The script should display the number in base 16, followed by a new line





GitHub repository: alx-system_engineering-devops

Directory: 0x03-shell_variables_expansions

File: 100-decimal_to_hexadecimal



#!/bin/bash

printf "%x\n" $DECIMAL

   

15. Everyone is a proponent of strong encryption

#advanced

Write a script that encodes and decodes text using the rot13 encryption. Assume ASCII.





Repo:



GitHub repository: alx-system_engineering-devops

Directory: 0x03-shell_variables_expansions

File: 101-rot13



#!/bin/bash

tr 'A-Za-z' 'N-ZA-Mn-za-m'

   

16. The eggs of the brood need to be an odd number

#advanced

Write a script that prints every other line from the input, starting with the first line.







GitHub repository: alx-system_engineering-devops

Directory: 0x03-shell_variables_expansions

File: 102-odd



#!/bin/bash

paste - - | cut -f 1





   

17. I'm an instant star. Just add water and stir.

#advanced

Write a shell script that adds the two numbers stored in the environment variables WATER and STIR and prints the result.



WATER is in base water

STIR is in base stir.

The result should be in base bestchol



Repo:



GitHub repository: alx-system_engineering-devops

Directory: 0x03-shell_variables_expansions

File: 103-water_and_stir



#!/bin/bash

printf "%o\n" $(( $((5#$(echo $WATER | tr water 01234))) + $((5#$(echo $STIR | tr stir. 01234))) )) | tr 01234567 bestchol



git add .

git commit -m "shell_variables_expansions"

git push
