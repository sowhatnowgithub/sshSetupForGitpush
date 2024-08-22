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

U are prompted with Please enter a passphrase, enter a password or press enter to skip the password authentication,

It is recommended to create a passphrase for security puprposes

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

U have successfully added ur git ssh, to verify this enter the following command in the terminal

```
ssh -T git@github.com
```

THis is will prompt a successfull authentication prompt which means u can now push ur commits directly to github

Basic setup on How to push changes

For this we intialize our project folder, then we will add our files in the project folder to staging area, then we will commit,

Since this is the first for our present folder to be added to our github repo,
will add our githubrepo link with git remote, 

Then we will push our files which are commited on the github repo

Initialise the present working directory for git
```
git init
```

Git add one file after another or multiple or all at the same time
```
git add filename
git add filename1 filename2 filename3
```

TO add all files
```
git add .
```

To commit our changes
```
git commit -m "message u want to have for the commit"
```

To add our repo to out git directory(this needs to be done once only)
```
git remote add origin git@github.com/user_id_git/repositry_name.git
```

To finally push our commits on to github

```
git push -u origin main
```

With this u can add, commit and push ur files onto github

HAPPY GITING :)


