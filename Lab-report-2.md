# Lab Report 2
---
## First Change
![test4fix](https://user-images.githubusercontent.com/103228609/165015447-3d84ad6c-7bcf-4b43-8bd0-1628ba8f5510.png)
[Test file with the error](https://github.com/A1yip/markdown-parser/blob/030758ccadd3ac705dc55a603066c40a8c46b1a4/test-file4.md)

Failing output: 
![test4error](https://user-images.githubusercontent.com/103228609/165016067-cbd0bf70-24a6-4e9d-9046-dd2baceef3be.png)

The bug that this program seems to be exhibiting is the fact that its not properly getting the links from the markdown file and putting them in the `ArrayList`, this bug is cauased by an infinite loop which is the symptom of the code. As such the failure inducing input associated with the file was the existence or lack of a parentheses following the brackets which indicated there was no list. However, the code can't discern whether or not there were even parentheses ad as such the failure inducing input came from the fact that it kept looping while not being able to find the parentheses.

## Second Change
![test6 fix](https://user-images.githubusercontent.com/103228609/165017673-ed916e20-f8cb-4773-850f-a0a98e21c2aa.png)
[Test file with the error](https://github.com/A1yip/markdown-parser/blob/1f612bd7fd729ab304432bfc1a35708ae449b2a6/test-file6.md)

Failing output: 

![test6error](https://user-images.githubusercontent.com/103228609/165017999-e5be16be-752b-40ec-9217-94ca44d9ab2a.png)

The bug here is a logic error due to the fact that the `ArrayList` should return nothing if there is a space between the brackets and the parentheses. The symptom here is an incorrect output since it still returns the links inside the parentheses despite it not needing to. The failure inducing input file has text in between the parentheses and the brackets which should indicate that there should be no links returned for that particular block.

## Third Change
![test7 fix](https://user-images.githubusercontent.com/103228609/165018823-598efc37-f812-47da-aee0-b4013684d007.png)
[Test file with the error](https://github.com/A1yip/markdown-parser/blob/3bdd0f7cca7f2a85dbf8956de43841e1fb5a15c1/test-file7.md)

Failing output:
![test7 error](https://user-images.githubusercontent.com/103228609/165018873-cb152ee2-b27f-4dfc-a484-2a2c8e70740e.png)

The bug here is also a logic error since the `getLinks` method should not return anything for this case since the `!` character indicates that the markdown text is actually an image rather than the link. The symptom shown is an incorrect output as the correct input should return an empty `ArrayList`. However, one thing to note is that this bug might be up for interpretation since one implementation may consider the the image a proper link while another implmentation may consider it as not a link. In the second case, the failure inducing input would come from the fact that there is an `!` in the markdown text file.
