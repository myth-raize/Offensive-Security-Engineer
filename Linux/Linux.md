## Basic Linux

```bash
pwd (Print Working Directory)

cd (Change Directory)
cd NAME
cd /home/___
cd .. (Parent Directory, Moves you one level up to)
cd ~ (Home Directory)
cd - (Previous Directory, Back to the last directory)

ls (List Directories)
ls NAME
ls -a (Viewing Hidden Files)
ls -l (Getting Detailed Information)
ls -la
ls -r (Sorting in Reverse Order)

touch NAME (Creating New File)
touch NAME1 NAME2 NAME3 (Creating Multiple Files)
touch -r FILE1 FILE2 (Set file2 timestamp to match file1)
touch -d DATETIME NAME (Set the timestamp to a specific date and time "2023-01-01 12:30:00")

file NAME (To find out what kind of file)

cat (Concatenate, To display the content of a single file)
cat NAME1 NAME2 (Display both files)
cat > NEWFILE (Creating file, ">" Overwrite)
  -n (This option numbers all output lines)
  -b (This optino numbers only the non-empty output lines)

less (Display text in a paged format)
  -q (esit less)

history (Viewing your command history, "ctrl R" Searching)
clear ("ctrl L")

cp (Copy, cp SOURCE DESTINATION)
  * (Matches any sequence, "cp *.jpg /home")
  ? (Matches any single character)
  [] (Matches any one of the characters enclosed in the brackets)
cp -r DIRECTORY DIRECTORY (Copying directories)
  -i (Interactive flag which prompts for confirmation)
  -f (To force an overwrite without any prompts)
  -p (Preserving it's mode, ownership, timestamps)


```
