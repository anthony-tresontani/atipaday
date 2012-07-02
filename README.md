atipaday
========

Here is my tips list to make my life as a developer easier.
Every day, I should learn a new tip.
My subjects will likely be: python, django, git, vim, IDE, linux.

Day 4
-----

Tags: git, tests

The best thing to do when you want to be sure you always deliver something usable is to run tests.
Sometimes, you may forget or fell lazy to run them. Git can do it for you. At every commit, tests are run.

To do that, in your root git directory (top level git directoy), edit `.git/hooks/pre-commit.sample` with:

  make -f <project_path>/makefile test
  
and rename it as `pre-commit`

Day 3
-----

Tags: linux

There is many command you run 50 times a day. Start your server, run your test, update your database...
To make that easier to remember and more consistant, you can simply create a makefile.
Here is a sample of what mine contains:

  test:
    python www/manage.py test --settings=settings_test
    
Then, whatever the environnement, the technology, etc... you always have the same commands to run similar action.

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