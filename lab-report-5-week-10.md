# Lab Report 5
## How I Found Different Results

I ran a bash script for loop for the test files for each markdown-parser implementation and redirected the outputs into a text file of which I then used `vimdiff` in order to check for differences between the two text files.

---
# [The First Test File](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/14.md)

* For this test-file neither implementations were correct
* ![LabReport5 1](https://user-images.githubusercontent.com/103228609/172095150-9e0a1860-b524-46fd-81ae-47646499cba1.png)
* The expected output should be `[]`
* The bug in the implementations is that they are ignoring the backslash charcater `\` in the parser which makes charcters literal rather than made into markdown syntax. As such, even when the brackets are supposed to be taken literally, the parser implementations treats it as an ordinary link. A simple fix for this bug would be to include the blackslash `\` within the conditions to check, and if a backslash were present, then the code would move on to check for the next bracket pair.
* Ideally this would be where the fix occurs:
* ![LabReport5 2](https://user-images.githubusercontent.com/103228609/172095845-e3ad7b48-170a-4f3d-9f71-be9c608da488.png)

# [The Second Test File](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/192.md?plain=1)

* For this test-file, my implementation was correct and the other implementation produced a wrong output.
* ![LabReport5 3](https://user-images.githubusercontent.com/103228609/172096410-b2c3f86a-0b8b-4248-9e6f-532e3627caaa.png)
* The expected output should be `[ "/url"]`
* The bug in the implementation is that the `:` character is being ignored as a valid way of creating a link in Markdown. Even if theres a colon after the brackets, the implementation continues checking for the existence of parentheses when there is none due the syntax of that link format.
* Ideally this would be where the fix occurs:
* ![LabReport5 4](https://user-images.githubusercontent.com/103228609/172103379-eb683a57-1409-4689-81b2-2df3c03deeb5.png)
 
