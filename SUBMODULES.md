# How to convert:

```bash
# Clone the monolithic repo into a fresh directory (this will become the submodule)
git clone https://github.com/PhearZero/react-most-wanted.git

# remove the origin to avoid pushing to main branch
git remote rm origin

# Filter changes on a folder
git filter-branch --subdirectory-filter ./packages/base-shell/ -- --all

# Go to github.com and create your remotes for each package
git remote add origin https://github.com/NodeJunkie/rmw/.git
git push --set-upstream origin master
```