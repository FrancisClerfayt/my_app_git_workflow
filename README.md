mkdir my_app_git_workflow/
ls -al
cd my_app_git_workflow/
git init .
git config --local "clerfayt.francis@popschool.fr"
touch index.html
touch style.css
touch script.js
mkdir images/
touch images/.keep
git add .
git commit -m "added .keep file in images"
git checkout -b feature/navbar
atom index.html
git add .
git commit -m "added navbar"
git checkout -b develop
git branch -a
git checkout -b feature/footer
git stash
atom index.html
git stash
git checkout -b hotfix/navbar
git merge feature/navbar
atom index.html
git add .
git commit -m "hotfix id my_menu nav ul"
git checkout feature/navbar
git merge hotfix/navbar
git checkout master
git merge hotfix/navbar
git checkout feature/footer
git config --global color.ui auto
git stash pop
git add .
git commit -m "ajout footer"
git checkout master
git checkout develop
git merge feature/navbar
git merge feature/footer
atom index.html
git add .
git commit -m "merge feature/footer"
git status
git checkout develop
git checkout -b feature/content
atom index.html
git status
git add .
git commit -m "added content"
git checkout develop
git merge feature/content
git checkout -b release
git status
git merge feature/navbar
git merge feature/footer
git merge feature/content
touch .gitignore
nano .gitignore
