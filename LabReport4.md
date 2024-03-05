# Lab Report 4
## Step 4: logging to ieng6

![step4](step4.png)

no speed up commands were used.

## Step 5: cloning the fork of the repository

![step5](step5.png)
![step5](step6.1.png)

- I copied ssh of the repository from copy button in github
- Then ```command-v``` to paste the ssh url after git clone
- cd into lab7 by typing cd l then ```<tab><enter>``` to autofill lab7

## Step 6: Running tests

![step6](step6.2.png)

- I wrote ```bash t```
- Then used ```<tab>``` to autofill the name of the bash script that run the tests ```test.sh```

## Step 7: Editing ListExamples.java

![step7](step7.1.png)
![step7](step7.2.png)

- wrote ```vi L``` then ```<tab>```
- it autofilled till ```ListExamples``` so i wrote ```.java``` then ```<enter>```
- the window above showed. i used ```i``` to go in insert mode
- Then navigated using ```arrow down``` till the line that contains index1
- Then changed 1 to 2, Then ```ESC``` to go out of insert mode
- After fixing the bug, i used ```:wq``` to save the changes made and quit the vim insert mode

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
- Then checked current git status again by ```<up><up>``` it showed that im up to date with the remote version.
