# Lab Report 4
## My Markdown Implementation
[Repository Link](https://github.com/A1yip/markdown-parser)
## Week 7 Reviewed Implementation
[Repository Link](https://github.com/hsflores7/markdown-parser.git)

## Snippet 1
Expected output: ```["url.com","`google.com", "google.com"]```

Test Case: ![LabReport4 3](https://user-images.githubusercontent.com/103228609/169754147-e35d3664-ae14-47e5-b7a5-7a3c9e082bad.png)
My implementation passed.

Reviewed Implmentation: ![image](https://user-images.githubusercontent.com/103228609/169754535-25d7d2ef-992f-4fdb-9ea7-242d3d163123.png)

## Snippet 2
Expected output: ```["b.com", "a.com(())", "example.com"]```

Test Case: ![LabReport4 5](https://user-images.githubusercontent.com/103228609/169754951-518094d9-9ac5-4678-8bb0-5d6fc0139b8b.png)

My Implementation: 

![LabReport4 6](https://user-images.githubusercontent.com/103228609/169755156-78d911bd-dad9-4bcb-a593-457cc5c3f084.png)

Reviewed Implementation: ![LabReport4 7](https://user-images.githubusercontent.com/103228609/169755193-514d4b2e-cd45-414b-844b-48c9923ea8e1.png)

## Snippet 3
Expected Output: ```["https://www.twitter.com", "https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule","(https://cse.ucsd.edu/" + "\n" + "\n" +"\n"]```

Test Case: ![LabReport4 8](https://user-images.githubusercontent.com/103228609/169755387-83738fb1-0558-4c7f-ac87-46deb4210a69.png)

My Implementation: 

![LabReport4 9](https://user-images.githubusercontent.com/103228609/169755681-35aba885-5edc-47eb-b299-18cec8cacce1.png)

Reviewed Implementation: ![LabReport4 10](https://user-images.githubusercontent.com/103228609/169755714-4708d8c8-cc77-40d6-8709-c709c24321e4.png)

## Questions
1. I believe my implementation passed here because it was only concerned with the parentheses and brackets and no other cases. It didnt particularly check for the backticks and it only really checked iff each bracket pair was followed by the parentheses pair.
2. I think in this instance it could either take a few lines of code (checking for negative indexes, or some other case) to fix it or it could take much more lines of code depending on whether the first change fixes it. Im quite sure, however, that the nested brackets and nested parentheses would be enough for my code to fail and as such I can say that it will definetly take more than 10 lines to fix this case.
3. Contrary to the last case, I do think this test case could be accounted for in less than 10 lines such, since my code should in theory account for the new lines and if it doesn't for any particular case, then I could fix it to do so. However, a small issue may come with determining the last link since it has a nested link.





