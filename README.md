# GitHub Collaboration Steps

## Forking and Cloning a Repository
1. Fork repository on GitHub
2. Open terminal and navigate to where you would like the project locally
3. Clone forked repository (in your account) 
    ```
    git clone https://github.com/{YOUR_ACCOUNT_NAME}/github_collab.git
    ```
4. Change into new directory
    ```
    cd git_collab
    ```
5. Make some changes to the repository
6. Add changes, commit changes, push changes to GitHub (origin remote)
    ```
    git add .
    git commit -m "my changes"
    git push origin main
    ```
7. On GitHub, create pull request with the original repository being the base and your repository being the head


## Syncing Fork with original Repository
1. Copy the url from the original repository
2. Add `upstream` remote to your local git repository
    ```
    git remote add upstream https://github.com/bstanton773/github_collab.git
    git remote -v (to verify)
    ```
3. On a clean branch, pull changes from the `upstream` remote into local repo with the branch name (usually main/master)
    ```
    git pull upstream main
    ```
4. (Potential) Resolve merge conflicts and commit merge
    ```
    git add .
    git commit -m "Merge upstream/main into main"
    ```
5. Push new commits to your `origin` repo
    ```
    git push origin main
    ```
