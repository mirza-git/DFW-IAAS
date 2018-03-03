![alt text](https://camo.githubusercontent.com/fb782da4019ab66eeea35cc9b9ce73b2438b1688/687474703a2f2f646f632e72756c746f722e636f6d2f696d616765732f6769746875622d6c6f676f2e706e67 "Logo Title Text 1")

# GIT tutorial

##### *Note: Git client or GUI should be installed on client workstation - all git command*

Create a repo.
Make sure there is at least one file in it (even just the README)
Generate ssh key:
```
ssh-keygen -t rsa -C "your_email@example.com"
```
Copy the contents of the file ~/.ssh/id_rsa.pub to your SSH keys in your GitHub account settings.
Test SSH key:
```
ssh -T dfwmtc@github.com
clone the repo:
git clone git://github.com/dfwmtc/DFW-IAAS.git
```
Now cd to your git clone folder and do:
```
git remote set-url origin dfwmtc@github.com:dfwmtc/DFW-IAAS.git
```
Now try editing a file (try the README) and then do:

```
git add -A
git commit -am "my update msg"
git push
```
