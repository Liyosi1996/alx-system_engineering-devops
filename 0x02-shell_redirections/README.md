This is a readme file on 0x02-shell_redirections
0. 0-hello_world :we write a command that displays 'Hello,World' ie echo 'Hello, World'
1. 1-confused_smiley : we write a command that displays a confused smile.use the command echo
2. 2-hellofile : we use the command cat to display the contents of the file .ie cat 'file name'
3. 3-twofiles : use the command "cat " to display the content of more than one file ie cat 'filename 1' 'filename 2'
4. 4-lastlines : use the command "tail -n 10 filename" to display the last 10 lines
5. 5-firstlines :use the command 'head -n 10 file name' to display the first 10 lines
6. 6-third_line :used the command 'head -3 filename ' to display the first three lines, using (|) which sends the output from one command to the input of another command ,use the command 'tail -1 ' to display the last line
7. 7-file : we use the command [echo Best School" | cat > '\*\\'\'''Best  School"\'\''\\*$\?\*\*\*\*\*:)'] to display  the contents of a file which were redirected 
8. 8-cwd_state:we use the command { ls -la > ls_cwd_content } ites into the file ls_cwd_content the result of the command ls -la. If the file ls_cwd_content already exists, it should be overwritten. If the file ls_cwd_content does not exist, create it
9. 9-duplicate_last_line:  we use the command  [tail -n 1 iacta | cat >> iacta] to write the duplicates of the last line of the file iacta
 10. 10-no_more_js : we use the command [find . -name "*.js" -type f -delete] to delete all the regular files (not the directories) with a .js extension that are present in the current directory and all its subfolders.
11. 11-directories : we use the command [find . -mindepth 1 -type d | wc -l] to  count the number of directories and sub-directories in the current directory.
 12. 12-newest_files :Is a  a script that displays the 10 newest files in the current directory.[ls -t | head]
13. 13-unique : Is a  a script that takes a list of words as input and prints only words that appear exactly once[ort | uniq -u]
14. 14-findthatword : Is a script that Display lines containing the pattern “root” from the file /etc/passwd [grep root /etc/passwd]
15. 15-countthatword :Is a script that Display the number of lines that contain the pattern “bin” in the file /etc/passwd [grep -c bin /etc/passwd]
16. 16-whatsnext : Is a script that Display lines containing the pattern “root” and 3 lines after them in the file /etc/passwd [cat /etc/passwd | grep -A 3 "root"]
17. 17-hidethisword file Display all the lines in the file /etc/passwd that do not contain the pattern “bin”.[grep -v bin /etc/passwd]
18. 18-letteronly file Display all lines of the file /etc/ssh/sshd_config starting with a letter.[grep ^[[:alpha:]]  /etc/ssh/sshd_config]
19. 19-AZ file Replace all characters A and c from input to Z and e respectively.[tr 'Ac' 'Ze']
20. 20-hiago file Create a script that removes all letters c and C from input[tr -d 'Cc']
21. 21-reverse file Write a script that reverse its input.[rev]
22. 22-users_and_homes file Write a script that displays all users and their home directories, sorted by users.[cut -d":" --fields=1,6 /etc/passwd | sort]
23. 100-empty_casks file Write a command that finds all empty files and directories in the current directory and all sub-directories.[find . -empty -printf "%f\n"]
24. 101-gifs file Write a script that lists all the files with a .gif extension in the current directory and all its sub-directories.[find . -type f -name "*.gif" -printf "%f\n"| rev | cut -d '.' -f2- | rev | LC_ALL=C sort -f]
25. 102-acrostic file Create a script that decodes acrostics that use the first letter of each line.[echo -ne $(cut -c-1 | tr -d '\n')'\n']
26. 103-the_biggest_fan file Write a script that parses web servers logs in TSV format as input and displays the 11 hosts or IP addresses which did the most requests[tail -n +2 | cut -f1 | sort | uniq -c | sort -nr -k 1,1 | cut -c 9- | head -11]
