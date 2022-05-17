# **Week 6 Lab Report**
___
## Streamling ssh Configuration

Making an ssh key to login onto the ieng6 server account really speeds up the login process. Still, it takes quite a bit of time to type out the full username and hostname (i.e. `ssh cs15lsp22xxx@ieng6.ucsd.edu`). This can be further configured to streamline the login process via a config file in the `.ssh` directory. 

Below is my `.ssh/config` file created and edited using VScode:
![config file](ssh_config.png)

Then I ran a test by loggin into my remote server account using the alias:
![alias login](streamlined_login.png)

Final test used `scp` command to copy a file from my pc onto the remote server using the alias:
![alias used scp](alias_scp.png)

___
## Setup Github Access from ieng6

This process was a little more challenging then the rest but it goes by first creating a ssh key on your remote account if one does not already exist and copying the contents of the `.pub` key. Then one would go onto github, settings, SSH and GPG keys, then click New SSH Key and pasting the contents of the `.pub` file into the key.

Here's the key in Github:
![github key](git_key.png)

And here's the key location in the remote server:
![remote key](remote_key.png)

Then after gettting that set up, I made a repository, and created a test file to commit and push a change onto Github via the ieng6 account:
![first ss](commit_first.png)
![last ss](commit_last.png)

Finally heres the commit on Github itself:
https://pahsuleyk.github.io/cse15l-lab-reports/
![github commit](result_commit.png)

___
## Copy whole directories with `scp -r`