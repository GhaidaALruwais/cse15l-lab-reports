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
"clinical trials" exist in "biomed" by using grep -l "clinical trials" \*. The \* indicates the grep -l command to
search all the files in "biomed" directory. The result was a list of file names that contain "clinical trials".
#### grep -l "pattern" "specificFilesToLookIn"
