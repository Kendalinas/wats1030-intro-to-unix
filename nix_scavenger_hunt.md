# *nix Scavenger Hunt

Complete the following challenges using the command-line interface on your favorite
Unix or Linux operating system. You are welcome and encouraged to consult any
additional documentation online or in books.

Please add your answers/responses/text pastes to the document after each prompt.

Note: For some of the challenges you will need to reference files included with
this repository, so you will need to fork the repo into your own Github account
and then clone it to your development environment.

## The Challenges

### Navigating the Filesystem

* Get an idea of where you are in the operating system. Use the `pwd` command to find your "path to working directory"--your current location in the filesystem of your devbox. *Paste the output of the `pwd` command here:*/home/cabox/workspace
* Discover more about this filesystem. Use `ls` (the "list" command)to see what is in this directory. *What directories and files do you see when you run `ls`?*LICENSE    challenge_files        nix_scavenger_hunt_stretch.md
README.md  nix_scavenger_hunt.md  super_scavengers.md
* You can use *options* to modify how a command runs. Try using `ls -alh` to see the contents of your current directory. total 40K
drwxrwxr-x 4 cabox cabox 4.0K Apr 11 15:53 .
drwxr-xr-x 7 cabox cabox 4.0K Apr 11 15:53 ..
drwxrwxr-x 8 cabox cabox 4.0K Apr 11 15:53 .git
-rw-rw-r-- 1 cabox cabox 1.1K Apr 11 15:53 LICENSE
-rw-rw-r-- 1 cabox cabox 2.7K Apr 11 15:53 README.md
drwxrwxr-x 7 cabox cabox 4.0K Apr 11 15:53 challenge_files
-rw-rw-r-- 1 cabox cabox 5.6K Apr 11 15:59 nix_scavenger_hunt.md
-rw-rw-r-- 1 cabox cabox  317 Apr 11 15:53 nix_scavenger_hunt_stretch.md
-rw-rw-r-- 1 cabox cabox  191 Apr 11 15:53 super_scavengers.md*How are the results different when you use the `-alh` options?* -bash: -alh: command not found
* The `man` ("manual") command tells you more about how any given command works. (*WARNING:* CodeAnywhere does not support the man command. You can click the following link to complete this task: http://man.he.net/). Run `man` to see instructions about how to use `man`. Then use `man` to learn what the `a`, `l`, and `h` options mean when used with the `ls` command. man ls
           Display the manual page for the item (program) ls.
           man -a intro
           Display,  in  succession,  all  of the available intro manual pages
           contained within the manual.  It is possible to quit  between  suc-
           cessive displays or skip any of them.
           man -l -Tdvi ./foo.1x.gz > ./foo.1x.dvi
           This  command  will  decompress  and format the nroff source manual
           page ./foo.1x.gz into a device independent (dvi) file.   The  redi-
           rection is necessary as the -T flag causes output to be directed to
           stdout with no pager.  The output could be viewed  with  a  program
           such  as  xdvi or further processed into PostScript using a program
           such as dvips.
           Man -h is the browser *Write down what those options do?*
* Commands can also take *arguments*, which are usually the names of files or locations that you want the command to work with. Try running `ls /` to see what files are in the *root* directory of the filesystem. 
kendals-MBP:wats1030-intro-to-unix kendalsmith$ ls
LICENSE                         challenge_files                 nix_scavenger_hunt_stretch.md
README.md                       nix_scavenger_hunt.md           super_scavengers.md
boot  etc  home      lib64  mnt    proc  run   srv   tmp  var/home/cabox*What files and directories do you see listed?*
* A Unix filesystem has a few special shortcuts to refer to specific locations. `/` indicates the *root* of the filesystem, meaning the top-most directory in the filesystem hierarchy. Use the `cd` ("change directory") command to move to the root directory. (Hint: Use `man` to look up the `cd` command if you have any issues) *Then run `pwd` and paste the output here:*  /Users/kendalsmith

* Another special shortcut in Unix is the `~` location. This indicates the *user root* directory, meaning the top-most directory in the hierarchy that comes below your user account. Use `cd` to move to `~`. *Run `pwd` and paste the response here:* /Users/kendalsmith

* Change directory into the `challenge_files` directory. Use `ls` to find only the files with a `.` pattern. *How many files do you find?* 10 files total

* Use the `cd` command to move "up" one directory. *Where are you in the filesystem now?*

* Press the up arrow on your keyboard. *What just happened?*
it showed the last command I typed
* Press the up arrow a few more times. *What do you see?*
It is a history of what i typed
* Run the `history` command. *What do you see?*cabox@box-codeanywhere:~$ history
    1  git clone
    2  ls
    3  mkdir projects
    4  cd projects
    5  git config --global user.name "Kendal Smith"
    6  git config --global user.email kendalinas@gmail.com
    7  ssh-keygen -t rsa -b 4096 -C "kendalinas@gmail.com"
    8  eval "$(ssh-agent -s)"
    9  nano ~/.ssh/config
   10  ssh-add -K ~/.ssh/id_rsa
   11  pbcopy < ~/.ssh/id_rsa.pub
   12  pwd
   13  git clone git@github.com:Kendalinas/wats3020-sandwich-machine.git
   14  ls
   15  git clone git@github.com:Kendalinas/wats1030-intro-to-unix.git
   16  ls
   17  ln -sv "/Applications/Sublime Text.app/Contents/SharedSupport/bin/subl" /usr/local/bin/subl
   18  ls /usr
   19  ls /usr/local
   20  mkdir /usr/local/bin
   21  sudo mkdir /usr/local/bin
   22  ln -sv "/Applications/Sublime Text.app/Contents/SharedSupport/bin/subl" /usr/local/bin/subl
   23  sudo ln -sv "/Applications/Sublime Text.app/Contents/SharedSupport/bin/subl" /usr/local/bin/subl
   24  ls
   25  cd wats3020-sandwich-machine/
   26  git status
   27  subl .
   28  python -m SimpleHTTPServer
   29  python -m SimpleHTTPServer
   30  code
   31  cd projects
   32  pwd
   33  git colne git@github.com:Kendalinas/wats1030-intro-to-unix.git
   34  ls
   35  code wats1030-intro-to-unix/
   36  git status
   37  git pull
   38  git status
   39  git add .
   40  git commit -m "changes"
   41  git push
   42  git status
   43  which code
   44  code
   45  git status
   46  man
   47  ls
   48  cd
   49  man
   50  cd
   51  pwd
   52  ~
   53  cd
   54  pwd
   55  ls
   56  .
   57  ls
   58  projects
   59  challenge_files
   60  cd
   61  cdls
   62  ls
   63  cd
   64  challenge_files
   65  cd
   66  history
kendals-MBP:~ kendalsmith$

### Observing the System

* Discover what account you are logged into using the `whoami` command. *What username are you currently using?* kendalsmith

* Discover who else is on your system with the `who` command. *Are any other users using your system? If so, list them here:*
kendalsmith console  Apr  6 13:19, no just me
* How long has your system been running? Use `uptime` to see, and *paste the result here:*
19:34  up 5 days,  6:16, 1 user, load averages: 1.90 1.94 1.86
* Run `ps aux` and review the results. (Hint: Use `man` to learn more about the `ps` command and options.) *How do you interpret what you see here?* The time and date of exactly what terminal commands took place and by whom.
* Run `top` and review the results. (Hint: You may need to use `ctrl-c` to get out of this app.) *How do you interpret what you see here?* I believe these are the extensions running at this time.

### Finding and Viewing Files

* Make sure you are in the `challenge_files` directory. Use the `*` wildcard to find all the files that have the word "credit" in the filename. *How many files did you find?* 2

* Use the `more` command to view one of the `credit_cards` files you just discovered. (Hint: Type `q` to quit viewing the file. Press the `spacebar` to page down. Use your keyboard arrows to move up/down.) *What is the date in the file you have viewed?* 1-15-2015
* Use the `find` command to search for files more effectively. Search the sub-directories under `challenge_files` to find the location of the file named `modi_laboriosam.txt`. *Where is that file located?*
* Use the `grep` command to search for text within a file. Use `grep` on all the `.user` files in `challenge_files` to find which files contain "WA" (the abbreviation for Washington state). *How many files did you find?* 23 in 20 files
* Use the `-r` option of `grep` to *recursively* find the text "Waldo" hidden in a file somewhere under the `challenge_files` directory. *Paste the result showing the file and line where the word "Waldo" shows up.*eaque_molestiae.txt maiores quia autem. Nisi modi Waldo se...

### Pipes and Connecting Commands

* Sometimes it's useful to output the results of a command to a text file for further analysis, reference, or processing. Try running `ls > files.txt`. Notice that the file `files.txt` was created. View that file using `more`. *What do you see in the `files.txt` file?*
* Notice that if you run `ls -alh` in the `challenge_files` directory, the files scroll by very quickly. Sometimes it would be better to get the results in a paginated format. Try running `ls -alh | more`. *Describe what you see when you run `ls -alh | more`.*
* Earlier, when you viewed the list of active processes on your devbox using `ps aux`, the list was probably really long. You can make this list more manageable by using the pipe (`|`) to filter the results of `ps` using `grep`. Run `ps aux | grep <your_username>` to see what processes are running for your specific user. *Paste the list of processes that reference your username here:*
kendals-MBP:wats1030-intro-to-unix kendalsmith$ /
bash: /: is a directory
kendals-MBP:wats1030-intro-to-unix kendalsmith$ ps
  PID TTY           TIME CMD
  613 ttys000    0:00.03 /bin/bash -l
kendals-MBP:wats1030-intro-to-unix kendalsmith$ ps aux| grep <kendal_smith>
bash: syntax error near unexpected token `newline'
kendals-MBP:wats1030-intro-to-unix kendalsmith$