# Adding your own recipes

```bash
$ ./podi recipe hello           # install helloworld-example
$ mv .pod/{hello,foo}           # rename to foo and modify
$ git add .pod/foo
# PROFIT!
```

# Adding your own recipe repository

Just expose a directory with recipes, and add `.index.txt` in that directory:

```bash
$ \ls | xargs -n1 echo > .index.txt
```

Then add it to the `podi` script:

```bash
RECIPE_REPOS="https://raw.githubusercontent.com/coderofsalvation/podi/master/recipe/.index.txt https://yoururl/.index.txt"
```

> Profit!
