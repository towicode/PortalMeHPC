###############################
Uploading your key with Windows
###############################

GIT is a set of tools used by developers to share projects.
We will not actually be using GIT for this project, but the installer
contains a useful tool that we will be using.

To start off visit the `git for windows`_ page and download the installer.

.. _git for windows: https://git-for-windows.github.io/

Download the installer.

.. image:: images/a.png

Run the installer. Most, if not all, the options we are just going to leave as default)

.. image:: images/b.png
.. image:: images/c.png
.. image:: images/d.png
.. image:: images/e.png
.. image:: images/f.png
.. image:: images/g.png
.. image:: images/h.png
.. image:: images/i.png

Once GIT has been sucesfully installed open the folder where
you have downloaded your :code:`private.key` and your :code:`public.key` file.

This is normally in your downloads folder.

.. image:: images/j.png

Right click somewhere in the folder and click "Git Bash Here"

.. image:: images/k.png

A black windows should pop up, similar to below. this is a terminal. A basic text based interface.

Next we are going to rename our files so the software can recognize them. To do this we are going to be using the `mv` command.
Once you are ready type the following into the terminal window. Press the enter key to send commands.

:code:`mv private.key id_rsa`

**press enter**

:code:`mv public.key id_rsa.pub`
   
.. image:: images/l.png

Finally we are going to run the :code:`ssh-copy-id` command to upload our public key to the server.
The command takes a few arguments.

   1. -f Forces the command to attempt to upload
   2. -i lets up provide our own key (in this case id_rsa.pub)
   3. the final argument is our username@hpc.arizona.edu

Once you are ready type the following into the terminal window.

**MAKE SURE TO FILL IN YOUR OWN USERNAME BELOW**

:code:`ssh-copy-id -f -i id_rsa.pub USERNAME@hpc.arizona.edu`

.. image:: images/o.png
