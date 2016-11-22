# Public Maven Repository

## Improvement hints

* restrict artifacts to be overridden
* fail build if git fails
* verify artifact upload success
* http://jeroenmols.com/blog/2016/02/05/wagongit/
* extend usage documentation with more details

## Usage 

* setup ssh key (github guide)
* invoke ssh connection to a github repository, this permanently adds github ssh key to trusted list (otherwise wagon-git will be unable to upload artifacts due to host key verification failure)
* setup pom extension, distribution, repository (wagon-git guide)
