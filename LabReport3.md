# Lab Report 3

## Part 1 


## Part 2
### grep -l
#### overview 
grep -l displays the names of the file that contains the specific pattern given
#### grep -l "pattern" *
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
#### grep -l "pattern" "specificFiles"
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
- 

