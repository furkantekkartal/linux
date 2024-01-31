# Bash | Command Line Interface (CLI) command in the learning process

## General Codes

### Basic commands

* "*" is joker character zero or more character
* "?" is joker character only 1 character
* Control key may be described in many ways, including Ctrl-X, Control-X, and ^X.
* The shell does not have a trash bin: once something is deleted, 

```
whoami (Return username)
pwd (print working directory)
clear (delete everything on screen)
```


### ls commands
```
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
ls Desktop (list a subdirectory if it exist)
ls --help (We can pass a --help option to any command)
man ls (We can read its manual with man)
```

### cd commands

```
cd Desktop (Change directory)
cd Desktop/shell-lesson-data
cd .. (go to one level up)
cd (go to home directory)
cd /home/ftekkartal/Desktop/shell-lesson-data (absolute path)
cd ~/Desktop/shell-lesson-data (~ means /home/ftekkartal)
cd - (go to previous directory)
```

### Tab completion;
```
  cd ~/Desktop/shell-lesson-data
  "ls nor" + press tab => "ls north-pacific-gyre/"
  double tab => list all items in that directory
  "ls north-pacific-gyre/g" + press tab => "ls north-pacific-gyre/goo"
  double tab => list all item begins with goo
```

### Create and delete files and directories;
* mkdir [path] creates a new directory.
* mkdir -p [path]  creates any intermediate subdirectories as required.
* rm [path] removes (deletes) a file.
* rm -r [path] removes (deletes) a directory.

```
pwd => /home/ftekkartal/Desktop/shell-lesson-data/exercise-data/writing
  mkdir thesis (crete a new directory named "thesis" in this directory ~/Desktop/shell-lesson-data/exercise-data/writing)
  mkdir -p ../project/furkan ../project/tekkartal (crete 2 new directories named "furkan" and "tekkartal' in this directory ~/Desktop/shell-lesson-data/exercise-data/project)

  ls -R ../project (List all nested subdirectories)

cd thesis
nano draft.txt (create a new text file)
touch my_file.txt (generate a blank text file)


rm my_file.txt (remove the file without asking)
rm -i my_file.txt (remove the file with asking)
rm -r -i thesis (remove the directory)

```

### Move and copy;

* mv [old] [new] moves (renames) a file or directory.
* cp [old] [new] copies a file.

```
mv thesis/draft.txt thesis/quotes.txt (The first argument tells mv what we’re ‘moving’, while the second is where it’s to go)

pwd => ~/Desktop/shell-lesson-data/exercise-data/writing
mv thesis/quotes.txt . (move file from /exercise-data/writing/thesis to /exercise-data/writing)

An example of moving;
  pwd => ~/Desktop/shell-lesson-data/exercise-data/writing
  ls -a furkan     => . .. a.txt b.txt
  ls -a tekkartal  => . ..

  cd furkan
  mv a.txt b.txt ../tekkartal

  cd ../
  ls -a furkan     => . .. 
  ls -a tekkartal  => . .. a.txt b.txt


An example of copying;
  pwd => ~/Desktop/shell-lesson-data/exercise-data/writing
  ls -a furkan     => . .. 
  ls -a tekkartal  => . .. a.txt b.txt

  cd tekkartal
  cp a.txt ../furkan

  cd ../
  ls -a furkan     => . .. a.txt
  ls -a tekkartal  => . .. a.txt b.txt

pwd => ~/Desktop/shell-lesson-data/exercise-data/writing
cp quotes.txt thesis/quotations.txt (copy a single file)
cp -r thesis thesis_backup (copy all content)

* cp needs directory name as the last argument.
```
### Word count
```
wc *.txt (word count | 4 column = line + character + words + file name)
wc -l *txt (line number + file name)
wc -m *txt (character number + file name)
wc -w *txt (word number + file name)
```

### Other commands (cat + less + sort + head + tail + echo + cut)

*This codes are not change the file, just affect on the screen

```
cat lengths.txt (concatenate(join together) files and show on screen)
```
```
less lengths.txt  (same as cat bur list only a screenful of the file (like first page))
    (Space -> next page)
    (b -> back pace)
    (q -> quit) 
```
```
sort number.txt (sort alphanumerical)
sort -n number.txt (sort numerical)
```
```
head -n 1 number.txt (take 1 line from top)
```
```
tail -n 1 number.txt (take 1 line from bottom)
```
```
echo The echo command prints text
```

```
cut -d , -f 2 animals.csv

  * cut means remove or ‘cut out’
  *  -d means use delimiter (if we not use -d parameter, standart delimiter would be TAB)
  *   , means komma will be used as delimiter
  *  -f means column
  *   2 means 2nd column
```


### To the file

">" =  overwritte the file

```
echo hello > testfile01.txt
echo world > testfile01.txt

cat testfile01.txt
    Output: world
```

">>" = add new line to the file
```
echo hello >> testfile02.txt
echo world >> testfile02.txt

cat testfile02.txt
    Output:  hello
             world
```

### Pipes and Filters
* Use "|" sybol to run more than 1 command.
* Left command's output will be right command's input.

For example;
![computer information](./images/2024-02-01_01-24-35.png)


```
cat animals.csv | head -n 5 | tail -n 3 | sort -r > final.txt
```
  * show animals.csv on the screen BUT THEN
    * Take first 5 line of the list BUT THEN
      * Take last 3 line of the new list BUT THEN
         * Reverse alphabetical sort the newer list BUT THEN
            * Write it to final.txt





