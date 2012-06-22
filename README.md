atipaday
========

Here is my tips list to make my life as a developer easier.
Every day, I should learn a new tip.
My subjects will likely be: python, django, git, vim, IDE, linux.

Day 2
-----
Tags: vi
Stuck while trying to edit a file in vi without having the permission.

Just do:

:w !sudo tee %

and that's saved

Day 1
-----

Tags: Environment, virtualenv.
The first day should start with my most usefull tip.
When you work on multiple project, you have to remember the project, the dev machine, the prod machine ...
An easy win is to set a convention in your virtualenv postactivate (ENV_DIR/<virtual_env>/bin/postactivate):

  alias prj="alias cd ~/workspace/my_project/"
  
  alias dev="ssh me@devserver.com"
  
  alias prod="ssh me@prodserver.com"
  
  prj
  
This was, you just have to

  workon my_env

And you are in the right directory, dev or prod, and you are in the right machine.