Ok to resolve Ela's changes I had to clone my repository into the command line with git clone

```
git clone https://github.com/erg55/Symbiosis-Evolution-group-Jagiellonian-University-exercise.git
cd Symbiosis-Evolution-group-Jagiellonian-University-exercise
```

```
git fetch origin
```

Load Ela's copy

```
git checkout -b ela-iwaszkiewicz-master master
```


```
git pull https://github.com/ela-iwaszkiewicz/Symbiosis-Evolution-group-Jagiellonian-University-exercise.git master
```
Trying to merge the copies results in an error because one file was renamed from .txt to .md and so it doesn't know to merege the files. 
So I edit this file manually on the command line how I want it to look with nano. And rem the older file.  

```
nano labmembersandcollaborators.md
git rm labmembersandcollaborators.txt
```

Next I have to commit the changes I made using the -a flag because I deleted a file and it needs to include some text about it with the -m flag 

```
git commit -a -m "deleted old txt file"
```

Finally I can use the pull command

```
git pull https://github.com/ela-iwaszkiewicz/Symbiosis-Evolution-group-Jagiellonian-University-exercise.git master
```

Now going back to the master branch.

```
git checkout master
```

And merge the branch now that it has no unresolvable conflicts again it must include some text 

```
git merge -m "merged" --no-ff ela-iwaszkiewicz-master
```

And finally push this local version to the web copy of the repository using your guthub username and login. 

```
git push origin master
```



