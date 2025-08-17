## Initial setup

1. GitHub
   * Sign up for [GitHub](https://github.com/) if not already signed
     up. Pick default (free plan).
   * [Create ssh key](https://help.github.com/articles/generating-ssh-keys/) and link it with GitHub:
     - Ensure that you've created an SSH key if you do not already have one. (`ed25519` keys are recommended)
     - Make sure your public SSH keys are added to your GitHub account and that you can use them to access git repos
     - Do Not Share Your Private Key, in any circumstance
   * [Fork](https://help.github.com/articles/fork-a-repo/) and create a [pull request](https://help.github.com/articles/using-pull-requests/) on [students repository](https://github.com/fdac25/students) so I
      can add you to the to the GitHub group for the course.
      
     - Start by [**forking** the students repository](https://github.com/fdac25/students)
     - Add your utk net id as NETID.md (click on '+' - add 
               new file next to the https://github.com/fdac19/students/ link)
     - Click on Create Pull Request (do not create NETID.md, but replace NETID by your netid in all lowercase, e.g. `bklein3.md` or `audris.md`)
    
     - If you receive a `Permission denied: publickey ` error, Add this to your ssh/config file:
       ```
       Host github.com
         IdentityFile ~/.ssh/[your ssh key file]
       ```
       note: Your SSH key file is the one that doesn't end in `.pub`
1. Familiarize yourself with GitHub workflow
   * Walk through [workflow](#workflow) 
    
## Typical workflow
1. To start, [**fork** the repository][forking] for the test project (found under [github.com/fdac25](https://github.com/fdac25))
1. [**Clone**][ref-clone] the repository to your computer.
1. View, create, and edit your files
1. [**commit**][ref-commit] changes to complete your solution.
1. [**Push**][ref-push]/sync the changes up to GitHub.
1. [Create a **pull request**][pull-request] on the original repository

## Learn how to access your githup repo in collab notebook
### Option 1
Open a line code in your notebook in google colab and run this :
```
from google.colab import drive
drive.mount('/content/drive')
```

Go to your Files in Google.colab and create a new folder with your repository name with this path :
```
Files/Content/"YOUR TEMPLATE NAME"
```
Then follow these steps:

- open google colab and create a notebook.ipynb OR use that notebook you using currently.

- open code and type
```
! apt-get install git
!git clone https://github.com/"YOUR USER NAME"/"YOUR GITHUB REPOSITORY WANT TO ADD "
```
You can find the right path of your repository from this path :
- open your GitHub
- go to the repository you want to clone
- click on CODE ( the green button ) on the right corner of your repository and then click on HTTPS
- you will see the URL then click on Copy
- It will clone all of your data and everything that you want from GitHub to Google.colab

### Option 2
Create a personal access token as mentioned [here]().

Once done, just run in your notebook
```
pat = 'Token here'
!git clone https://{pat}@github.com/username/repo.git
```
### Option 3
You can simply go to Google Colab and you can choose 'GitHub' on the box which you can see when you just go to the Colab site and login. Colab will automatically redirect you to github in order to authorize your github account. Then you can choose repository to use at Google Colab!


<!-- Links -->
[deliberate-practice]:http://www.psy.fsu.edu/faculty/ericsson/ericsson.exp.perf.html
[pull-request]:https://help.github.com/articles/creating-a-pull-request
[create-repo]: https://help.github.com/articles/create-a-repo
[forking]: https://guides.github.com/activities/forking/
[ref-clone]: http://gitref.org/creating/#clone
[ref-commit]: http://gitref.org/basic/#commit
[ref-push]: http://gitref.org/remotes/#push
[pull-request]: https://help.github.com/articles/creating-a-pull-request
[raw]: https://raw.githubusercontent.com/education/guide/master/docs/forks.md
