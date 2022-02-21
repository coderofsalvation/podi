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
$ find -type f | grep -v index.txt | sed 's/^\.\///g' > .index.txt
```

Then add the index-url to the `podi` script:

```bash
RECIPE_REPOS="https://raw.githubusercontent.com/coderofsalvation/podi/master/recipe/.index.txt https://yoururl/.index.txt"
```

> Profit!
