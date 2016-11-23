# Public Maven Repository

## Improvement hints

* restrict artifacts to be overridden
* fail build if git fails
* verify artifact upload success
* http://jeroenmols.com/blog/2016/02/05/wagongit/
* extend usage documentation with more details

## Usage 

* setup ssh key in git bash (github guide: https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/)

```sh
# generates keypair and asks for private passphrase
$ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"

# start ssh agent in background and add private key to list
$ eval "$(ssh-agent -s)"
$ ssh-add ~/.ssh/id_rsa

# Copies the contents of the id_rsa.pub file to your clipboard
$ clip < ~/.ssh/id_rsa.pub
```

* invoke ssh connection to a github repository, this permanently adds github ssh key to trusted list (otherwise wagon-git will be unable to upload artifacts due to host key verification failure)
* add ssh key public in github settings
* setup pom extension, distribution, repository (wagon-git guide)
