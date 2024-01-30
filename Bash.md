# Bash | Command Line Interface (CLI) command in the learning process

## 1. General Codes

### 1.1 Basic commands

```
whoami (Return username)
pwd (print working directory)
clear (delete everything on screen)

cd (Change directory)
help cd (use this grammar for others)

ls (list files )
ls -F (add file and directory names)
  / indicates directory
  @ indicates link
  * indicates executable
ls -h (human readable)
ls -l (long listing format)
ls -t (time last changed)
ls -r (reverse list)
ls -a (show all, including hidden files)
ls Desktop (list a subdirectory)
ls --help (We can pass a --help option to any command)
man ls (We can read its manual with man)

cd Desktop (Change directory)
cd Desktop/shell-lesson-data
cd .. (go to one level up)
cd (go to home directory)
cd /home/ftekkartal/Desktop/shell-lesson-data (absolute path)
cd ~/Desktop/shell-lesson-data (~ means /home/ftekkartal)
cd - (go to previous directory)

Tab completion;
  cd ~/Desktop/shell-lesson-data
  "ls nor" + press tab => "ls north-pacific-gyre/"
  double tab => list all items in that directory
  "ls north-pacific-gyre/g" + press tab => "ls north-pacific-gyre/goo"
  double tab => list all item begins with goo

pwd => /home/ftekkartal/Desktop/shell-lesson-data/exercise-data/writing
  mkdir thesis (crete a new directory named "thesis" in this directory ~/Desktop/shell-lesson-data/exercise-data/writing)
  mkdir -p ../project/furkan ../project/tekkartal (crete 2 new directories named "furkan" and "tekkartal' in this directory ~/Desktop/shell-lesson-data/exercise-data/project)

  ls -R ../project (List all nested subdirectories)

cd thesis
nano draft.txt (create a new text file)
touch my_file.txt (generate a blank text file)

```


