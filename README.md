BASIC GUIDE ON HOW TO SETUP GIT CONNECTION TO GITHub REPO   

THE STEPS INVOLVED ARE:

Generation a ssh key, to make connection to the git hub repo, we will use terminal inbuilt ssh tools for this purpose

Then adding the ssh to our fingerprints, which means we will now access the git hub with this

Then adding the generated ssh key to ur github page 


GENERATING A SSH KEY

Open a terminal and enter the following command

```
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

U are prompted with Please enter a passphrase, enter a password or press enter to skip the password authentication for future uses

When u enter this u will be prompted on where to save ssh key, default place is good(~/.ssh/id_rsa) , if u want a new another name change id_rsa to ur prefered one


ACTIVATE SSH KEY
```
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_rsa
```
inplace of the id_rsa , use the name of the ssh key


ADD SSH KEY TO GITHUB

1.COPY THE KEY

```
cat ~/.ssh/id_rsa.pub
```

If u set name of ur key as different one, like sup_sshkey, then inplace of id_rsa.pub put sup_sshkey.pub

ADD SSH KEY TO GITHUB

Then navigate to settings in the github profile, under ssh and GPA press new ssh key then add this key there and save


