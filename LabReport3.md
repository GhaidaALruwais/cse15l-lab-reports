# Lab Report 3

## Part 1 


## Part 2
### grep -l
### overview 
grep -l displays the names of the file that contains the specific pattern given
### grep -l "pattern" *
returns the names of the files that contain "pattern" in the current directory.
```
ghida04@MacBook-Pro-5 docsearch % cd technical
ghida04@MacBook-Pro-5 technical % cd biomed
ghida04@MacBook-Pro-5 biomed % grep -l "clinical trials" *
1468-6708-3-1.txt
1468-6708-3-4.txt
1468-6708-3-7.txt
1471-2105-3-26.txt
1471-2180-1-28.txt
1471-2199-3-12.txt
1471-2253-1-1.txt
1471-2288-2-10.txt
1471-2288-2-11.txt
1471-2288-2-4.txt
1471-230X-2-17.txt
1471-2326-2-4.txt
1471-2334-3-10.txt
1471-2350-3-1.txt
1471-2369-3-9.txt
1471-2369-4-1.txt
1471-2377-2-6.txt
1471-2377-3-4.txt
1471-2407-1-19.txt
1471-2407-2-11.txt
1471-2407-2-17.txt
1471-2407-2-19.txt
1471-2407-2-23.txt
1471-2407-3-3.txt
1471-2415-3-4.txt
1471-2474-4-8.txt
1471-5945-1-3.txt
1472-6831-3-1.txt
1472-684X-1-5.txt
1472-6882-1-12.txt
1472-6963-3-14.txt
1475-2867-3-3.txt
1476-4598-2-1.txt
1477-7525-1-12.txt
1477-7525-1-9.txt
ar104.txt
ar309.txt
ar778.txt
bcr273.txt
cc103.txt
cc1498.txt
cc2167.txt
cc2190.txt
cc991.txt
cvm-2-1-038.txt
cvm-2-4-180.txt
cvm-2-4-187.txt
cvm-2-6-278.txt
cvm-2-6-286.txt
gb-2001-2-10-research0041.txt
gb-2002-3-5-research0022.txt

```
In the code block above the path to the current directory is "/technical/biomed". I aim to find where the pattern
"clinical trials" exist in "biomed" by using grep -l "clinical trials" \*. The \* is an indicator for the grep -l command to
search all the files in "biomed" directory. The result was a list of file names that contain "clinical trials".
- The grep -l option is crucial when you want to edit files that contain a certain pattern. For example, if a specific IOS version is outdated, you use grep -l to search for all the files that use the outdated version
and then you can substitute it with the new supported version.
### grep -l "pattern" "specificFiles"
returns the names of the given files that contain "pattern" in the current directory.
```
ghida04@MacBook-Pro-5 docsearch % cd technical
ghida04@MacBook-Pro-5 technical % cd biomed
ghida04@MacBook-Pro-5 biomed % grep -l "clinical trials" 1468-6708-3-1.txt ar750.txt cc105.txt
1468-6708-3-1.txt

```
In the code block above the path to the current directory is "/technical/biomed". I aim to find which 
of these three files contains clinical trials by using the pattern "clinical trials". Instead of using \* as the example
before, I listed the files that I want the grep -l command to search. The result was the name of the file that contained 
"clinical trials".
- if the specified files are not in the current working directory, an error will show saying that there is no file called "... "
- if there are no files that match the pattern given, no name will be returned.
- The grep -l "pattern "files" option is crucial when you want to edit a set/ collection of files that contain a certain pattern. For example, if you are building an app and you need to update files from last year that contain
functionality that is no longer supported in the new IOS version. You already know the functionality that is no longer supported and the set of files from previous years, for example, the files with a name that contains 2020. You
can use grep -l "pattern" "files" to look for the specific files that implement the outdated functionality.
### sources
- https://www.geeksforgeeks.org/grep-command-in-unixlinux/
- ChatGPT:
  - Supplying a set of files to the grep -l "pattern" "files" command allows you to search for a pattern ("pattern") across multiple files simultaneously and obtain a list of filenames that contain the pattern. Here's how it can be useful:

      - Batch Processing: When you have a collection of files and you want to quickly identify which ones contain a certain pattern, grep -l allows you to perform this search efficiently in one command. This is especially useful when dealing with large datasets or directories with many files.

      -  Selective Action: After identifying the files that contain the pattern, you can perform further actions on these files selectively. For example, you might want to process or analyze only those files that match a specific criterion.

      - Logging and Monitoring: In system administration or monitoring tasks, you may want to check logs or specific files for certain patterns. grep -l allows you to automate this process and obtain a list of files that match the criteria, which can then be further analyzed or monitored.

      - Integration with Other Commands: grep -l can be combined with other commands in pipelines to perform complex operations. For example, you can use it in conjunction with xargs to process the matching files or with find to search recursively through directories.

      - Overall, supplying a set of files to grep -l "pattern" "files" provides a versatile and efficient way to search for patterns across multiple files and obtain a list of filenames that match the pattern, enabling further analysis or action as needed.

### grep -c 
### Overview 
displays how many "pattern" exist in "file"
grep -c is useful when searching for a certain attribute in complex classes. It shows how many times the attribute was used in files.
### grep -c "pattern" *
```
ghida04@MacBook-Pro-5 911report % grep -c "someone" *
chapter-1.txt:6
chapter-10.txt:2
chapter-11.txt:1
chapter-12.txt:1
chapter-13.1.txt:3
chapter-13.2.txt:2
chapter-13.3.txt:1
chapter-13.4.txt:4
chapter-13.5.txt:0
chapter-2.txt:1
chapter-3.txt:3
chapter-5.txt:2
chapter-6.txt:3
chapter-7.txt:2
chapter-8.txt:6
chapter-9.txt:0
preface.txt:0
```
- the \* is used to indicate a search for all files in the directory
- Returns the count of pattern "someone" in all the files in the directory
### grep -c "patter" "file"
```
ghida04@MacBook-Pro-5 technical % cd government
ghida04@MacBook-Pro-5 government % cd media
ghida04@MacBook-Pro-5 media % grep -c "laws" 5_legal_Groups.txt
0
ghida04@MacBook-Pro-5 media % grep -c "law" 5_legal_Groups.txt
2
```
- returns the count of pattern in the given file/ files
- Grep -c doesn't work if your input is a directory instead of a file. It will indicate an error saying that \(...) is a directory
### sources used
- https://www.geeksforgeeks.org/grep-command-in-unixlinux/

### grep -n 
### Overview 
Given a certain file, it results in the line and line number that the "pattern" appears in.
Grep -n is useful when wanting context about the usage of "pattern" before editing the file
### grep -n "pattern" "directory\(\*)/ or files" 
```
ghida04@MacBook-Pro-5 technical % cd biomed
ghida04@MacBook-Pro-5 biomed % grep -n "clinical trial" * 
1468-6708-3-1.txt:280:        significantly greater than zero. A clinical trial of a
1468-6708-3-1.txt:332:          Implications for clinical trials
1471-2288-2-10.txt:404:          instrument for scoring a randomized clinical trial with
1471-2288-2-10.txt:464:          collection form for a meta-analysis of a clinical trial
1471-2407-3-3.txt:36:        focused on blood cell samples from oncology clinical trials
1471-2407-3-3.txt:75:          open-label, multicenter Phase III clinical trials
1471-2407-3-3.txt:494:          first clinical trial was used as the 'training' set and
1471-2407-3-3.txt:507:        blood RNA samples from a clinical trial of the signal
1471-2407-3-3.txt:562:        III clinical trials that used SU5416. Further exploration
cc103.txt:52:          clinical trials or meta-analyses of human studies.
cc103.txt:132:          As shown in Table 1, to date only two clinical trials
cc2167.txt:189:          for ongoing clinical trials, comparisons between clinical
cc2167.txt:208:          with drotrecogin alfa (activated) in clinical trials was
cc2167.txt:423:        and placebo patients enrolled in clinical trials of
cc2167.txt:483:        the ICH event rate in all clinical trials combined (1.1%)
cc2167.txt:549:        remained consistent over multiple clinical trials. The only
cc2190.txt:74:          type) or controlled clinical trials or clinical trials,
cc2190.txt:89:          design-randomized clinical trial; population -
cc991.txt:14:        of caregiver availability. Several clinical trials have
cvm-2-1-038.txt:9:        and the methods used in clinical trials. Magnetic resonance
cvm-2-1-038.txt:14:        One objective in all clinical trials is the selection of
cvm-2-1-038.txt:26:        modern era of stroke clinical trials by clinical criteria
cvm-2-1-038.txt:42:        clinical trials, a sample selected based on an imaging
cvm-2-4-187.txt:12:        clinical trials can be difficult, just as in clinical
cvm-2-6-278.txt:65:        Current clinical trials of angiogenesis factors were
cvm-2-6-278.txt:340:          systems can help predict the results of clinical trials,
cvm-2-6-278.txt:454:        strategies. Better designed studies and clinical trials
cvm-2-6-286.txt:57:        have been apparent in subset analyses of clinical trials,
gb-2001-2-10-research0041.txt:39:        evaluated in multiple cancer clinical trials [ 7, 9], and
gb-2001-2-10-research0041.txt:431:        clinical trials of flavopiridol.
gb-2002-3-5-research0022.txt:98:        sample size/power calculations in clinical trials and other
gb-2002-3-5-research0022.txt:1142:        clinical trials. However, because of the close relation
```
#### The list above has been cut down due to its size.
- Each line contains the file, line number, and the line that the "pattern" exists in
### grep -n "pattern" -r  "directory" 
```
ghida04@MacBook-Pro-5 technical % grep -n "clinical trial" -r *
biomed/cc991.txt:14:        of caregiver availability. Several clinical trials have
biomed/ar309.txt:45:        supported the initiation of a phase-I/II clinical trial in
biomed/bcr618.txt:333:        in this study come from a prospective clinical trial,
biomed/1471-2377-2-6.txt:16:        clinical trials compares with the results from clinical
biomed/1471-2377-2-6.txt:47:          randomised clinical trials of galantamine (Reminyl ®) [
biomed/1471-2377-2-6.txt:233:        In our study of patients recruited for clinical trials at
biomed/ar104.txt:165:        proven effective in clinical trials, and the US Food and
biomed/cvm-2-6-286.txt:57:        have been apparent in subset analyses of clinical trials,
biomed/cvm-2-4-187.txt:12:        clinical trials can be difficult, just as in clinical
biomed/1472-684X-1-5.txt:183:          management of pain outside of clinical trials [ 21 ] .
biomed/1472-684X-1-5.txt:248:          clinical trial before moving to more expensive
government/Alcohol_Problems/Session2-PDF.txt:412:clinical trials. Studies in these centers should demonstrate the
government/Alcohol_Problems/Session3-PDF.txt:325:insights from clinical trials should be gathered and made
government/Alcohol_Problems/Session3-PDF.txt:377:of these interventions, clinical trials are needed to confirm these
government/Alcohol_Problems/Session3-PDF.txt:1275:that none of the three clinical trials (Gentillelo's with trauma
government/Alcohol_Problems/Session3-PDF.txt:1417:Marilyn Sommers related her experience from two clinical trials
government/Alcohol_Problems/Session3-PDF.txt:1441:cautioned that not every study has to be a clinical trial focused
government/Alcohol_Problems/Session3-PDF.txt:1465:addressed by pooling data sets from existing clinical trials and
government/Alcohol_Problems/Session4-PDF.txt:268:moving beyond clinical trials to national dissemination.30 There is
government/Alcohol_Problems/Session4-PDF.txt:1294:a clinical trial.
government/Alcohol_Problems/Session4-PDF.txt:1295:Gentilello suggested that clinical trials are important because
plos/pmed.0020258.txt:42:        it; it would be interesting to know whether preclinical trials assessing vaccines or
plos/pmed.0020278.txt:22:        was an abject failure in two human clinical trials, including a trial of over 2,500
plos/pmed.0020055.txt:64:        clinical trials, but not yet for other medical research. An ultimate aim for reporting
plos/pmed.0010021.txt:80:          But clinical trials carried out in our National Institutes of Health–sponsored General

```
#### The list above has been cut down (lines that contain similar directories aren't shown due to the list's length)
- This command option shows all the calls to "clinical trial" in all files or directories of ./technical
- Each line shows the directory, file name, line number, and line contents that are associated with the pattern/ "clinical trial"
### sources used
- https://www.geeksforgeeks.org/grep-command-in-unixlinux/
- chatGPT:
  - what are the different inputs i can give for grep -n
    - Search in a Single File: You can specify the name of a single file to search in
    - Search in Multiple Files: You can specify multiple files to search in
    - Search in All Files in a Directory: You can use wildcards (*) to search in all files in a directory
    - Recursive Search in Subdirectories: You can perform a recursive search in all subdirectories of a directory using the -r or -R option
    - Search in Standard Input: You can pipe input to grep from another command and use - to represent standard input
    - Search in Output of Another Command: You can use the output of another command as input to grep

### Using ^ in grep
### Overview
using "^pattern" results in a list of lines that start with "pattern"
This option on grep is helpful when you want to delete the lines that don't/do start with a specific word from files.
### grep "^pattern" * or "files"
```
ghida04@MacBook-Pro-5 government % cd media
ghida04@MacBook-Pro-5 media % grep "^age" *
5_Legal_Groups.txt:agencies. All of the agencies can share the same reception area and
5_Legal_Groups.txt:agencies about $375,000 each year. My assistant, Charity
All_May_Have_Justice.txt:age. This campaign provides financial assistance to agencies that
Annual_Fee.txt:agencies throughout the state, including the Legal Assistance
BergenCountyRecord.txt:agency a proper hearing.
BergenCountyRecord.txt:agency's executive vice president, Randi Youells, sought the merger
City_Council_Budget.txt:agency to the Corporation Counsel's Office.
Farm_workers.txt:agency's pesticide project. 'Imagine in your own office if half the
Firm_to_the_Poor_Needs_Help.txt:agencies.
It_Pays_to_Know.txt:agents of Utah Nonprofit Housing to find out about her
Legal_Aid_campaign.txt:agency will receive $400,000 less in federal funds in 2003, because
Legal_services_for_poor.txt:agency's clients are poor, and many are elderly or disabled, he
New_Online_Resources.txt:agencies run more efficiently.
Owning_a_Piece.txt:agency's Church Street building in Lower Manhattan, which was
Owning_a_Piece.txt:agency would emphasize services for the elderly, housing
Paralegal_Honored.txt:agency was first opened to serve Lancaster, York and Reading.
Poverty_Lawyers.txt:agencies representing the indigent - including Legal Aid, the South
Providing_Legal_Aid.txt:agencies or subdivisions of the state, nor any colleges or
Raising_the_Bar.txt:agent and a full-time homemaker, he was educated at Catholic
Survey.txt:agencies in New York begin at slightly higher salaries.
```
- shows the directory, file name, and line that starts with "age"
- It is not accurate since it returns any word that starts with age such as agency
- If you want to show only lines that start with the word "age" then you need to add a space at the end "^age "

### grep "^pattern" -r directory/
```
ghida04@MacBook-Pro-5 technical % cd government 
ghida04@MacBook-Pro-5 government % grep "^someone" -r *
Gen_Account_Office/pe1019.txt:someone for even modest help (like minding a child for an hour) had
Gen_Account_Office/d01591sp.txt:someone who never saves will have no wealth.20 Conversely,
```
- Recursively searched the government directories and files for lines that start with "someone"
- Each line shows the directory, file name, and the line that starts with "pattern"
### sources used
- https://www.geeksforgeeks.org/grep-command-in-unixlinux/
- chatGPT:
  - what are the different inputs i can give for grep "^ "
    - Search in a Single File: You can specify the name of a single file to search in
    - Search in Multiple Files: You can specify multiple files to search in
    - Search in All Files in a Directory: You can use wildcards (*) to search in all files in a directory
    - Recursive Search in Subdirectories: You can perform a recursive search in all subdirectories of a directory using the -r or -R option
    - Search in Standard Input: You can pipe input to grep from another command and use - to represent standard input
    - Search in Output of Another Command: You can use the output of another command as input to grep


  

