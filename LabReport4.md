# Lab Report 4
## Step 4: logging to ieng6

![step4](step4.png)

no speed up commands were used.
I just wrote ```ssh galruwais@ieng6.ucsd.edu``` and ```enter```
to log in the virtual device ieng6
logged in using the saved ssh keys without a passcode

## Step 5: cloning the fork of the repository

![step5](step5.png)
![step5](step6.1.png)

- I forked the repository using the ```fork``` button in github
- I copied ssh of the repository from copy button in github
- Using the ssh link of the repository allow you to push your changes to the remote repository on github
- Then ```command-v``` to paste the ssh url after git clone
- cd into lab7 by typing cd l then ```<tab><enter>``` to autofill lab7
- The ```<tab>``` autofills the name of the repository if it is unique like lab7.
    - if it is not unqiue then i can type till the unique part and use ```<tab>``` example having lab712 and lab7 when you press ```<tab>``` it will autofill till lab7 then i can type 1 and use ```<tab>``` again and it will autofill till lab712

## Step 6: Running tests

![step6](step6.2.png)

- I typed ```bash t```
- Then used ```<tab>``` to autofill the name of the bash script that run the tests ```test.sh```
- pressing ```enter``` runs the tests and print the output on the terminal

## Step 7: Editing ListExamples.java

![step7](step7.1.png)
![step7](step7.2.png)

- wrote ```vi L``` then ```<tab>```
- it autofilled till ```ListExamples``` because ListExamples is not unique (there exists another file in the repository that starts with ListExamples) so i wrote ```.java``` then ```<enter>```
- the window above showed. i used ```i``` to go in insert mode
- insert mode allows you to modify files from the command line using vim
- Then navigated using ```<down>``` till the line that contains index1
- Then changed 1 to 2 by ```Ctrl-W``` then i wrote ```index2```, Then ```ESC``` to go out of insert mode
- After exiting insert mode, im still in the vim window so i need to quit vim to return to the command line
- i used ```:wq``` to save the changes made and quit vim

## Step 8: Running tests
  
![step8](step8.png)
- ```<up> <up>``` to go above two lines to the previous code in step 6
- ```<enter>``` to compile and check the tests again.

## Step 9: commit and push changes

![step9](step9.1.png)
![step9](step9.2.png)
![step9](step9.3.png)
- Tried to commit directly without adding ```LinkedList.java``` first so it didn't work
- Then typed git add L ```<tab>``` and it automatically filled ListExamples.java ```<enter>```
- Then typed ```<up><up>``` to go above to the failed commit and then i fixed the comment to "bug fixed" then```<enter>```
- checked current git status
- Then types git push o ```<tab><enter>``` and pushed current changes to remote directory
- Then checked current git status again since i already typed check status before i just need to go ```<up><up>``` till git status and then ```enter```it showed that im up to date with the remote version.
