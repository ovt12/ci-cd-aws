# ci-cd-aws

![Recording](Recording%202023-01-25%20at%2015.35.29%20(1).gif)

## How have you use Jenkins to add Continuous integration with this project?
- We added continuous integration by building a test enviroment that would catch errors in the code if erros found it would not push to the main branch if successfull it would integrate into the main branch
​
### How did you allow Jenkins access to the Github repo?
- In the Jenkins configuration we ticked a box called "github project" & entered our project URL.
- By using the private ssh keys using we created using the command "Ssh-keygen -t rsa"
​
### How did you get the Github repo to trigger the build?
- In source-code manaement we also ticked the git box and added our URL's again using our private ssh keys we generated
- Implemented a Github webhook and also entered a payloadURL with a jenkins URL. This is then triggered through an event such as a push / pull.
​
---
​
## How have you use Jenkins to add Continuous delivery with this project?
- On a successfull test build through CI. In the post build section of Jenkins there was an option to 'trigger only if build is stable'. If success than it will build & intergrate into the main branch.
​
### How did you allow Jenkins access to the EC2 instance?
- Added our EC2 Public IP to the nology proxy configure file and we also had to include our AWS key to the abuntu VM.

​
### How did you get the CI project to trigger the CD build?
- If successfull a post-build action would be in place to trigger the CD build.
​
---

