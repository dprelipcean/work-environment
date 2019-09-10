1. Open your .bashrc.
---------------------
Your .bashrc file is located in your user directory. Open it in your favorite text editor.

.. code-block:: console

    $ vim ~/.bashrc

2. Go to the end of the file.
-----------------------------

In vim, you can accomplish this just by hitting “G” (please note that it is capital).

3. Import aliases from a separate file
--------------------------------------
You may want to put all your additions into a separate file like
*~/.bash_aliases*, instead of adding them in the *.bashrc* directly.
See */usr/share/doc/bash-doc/examples* in the *bash-doc* package.

.. code-block:: console

    if [ -f ~/.bash_aliases ]; then
        . ~/.bash_aliases
    fi


4. Add the aliases
------------------
A simple way to chain commands in Linux is to use the *&&* operator.
This operator will run a set of commands and only continue to the next command
if the previous one was successful. The basic format is:

.. code-block:: console

    alias aliasname='commands'

One gotcha is that there cannot be a space between the “aliasname” and the
EQUAL sign. Also, there can’t be a space between the EQUAL sign and the opening
quote for the command.

5. Install the .bashrc.
------------------------
The new *.bashrc* would be installed the next time you log out and log back in,
but if you are impatient like me and just want it installed now, you can just
source the file.

.. code-block:: console

    $ source ~/.bashrc

