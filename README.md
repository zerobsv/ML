## Collection of all ML work

## Create the submodules

=> Organize the code into submodules:

$ git submodule add <path to git repo with code>

=> Add all the repos which contain individual modules using the above

=> Come back to the root of this repository in linux, and execute the status command

$ git status

=> Add the .gitmodules file, and the other submodules in the repo and create a commit

$ git add .gitmodules linear_regression logistic_regression
$ git status
$ git commit -m "Organizing the code into submodules"

=> Push a commit to the main repo, with all the changes

$ git push -u origin main


## Update each submodule after changes to individual modules

=> Run this command to update / pick up changes from the main branch of an individual submodule

$ git submodule update --remote logistic_regression

=> Add all the files to a commit after running the submodule update

$ git add <>
$ git commit -m "updated the xyz submodule"
$ git push -u origin main

=> For more advanced use cases, use a recursive submodule update (usually I do not prefer recursive submodules)

$ git submodule update --recursive --remote <submodule name>

