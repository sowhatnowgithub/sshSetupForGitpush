This is a basic guide on how to set up a git connect to your github repo


GENERATING A SSH KEY
```
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

U are prompted with passphrase enter a password and press enter to skip the password authentication


When u enter this u will be prompted on where to save ssh key, default place is good(~/.ssh/id_rsa) , if u want a new one as a name change id_rsa to ur prefered one

ACTIVATE SSH KEY
```
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_rsa
```

ADD SSH KEY TO GITHUB

1.COPY THE KEY

```
cat ~/.ssh/id_rsa.pub
```

If u set name of ur key as different one, like sup_sshkey, then inplace of id_rsa.pub put sup_sshkey.pub

Then navigate to settings in the github profile, under ssh and GPA press new ssh key then add this key there and save


