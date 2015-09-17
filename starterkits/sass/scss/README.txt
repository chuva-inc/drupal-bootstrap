The following files are simply duplicates from the Bootstrap library. With
modifications in where to reference the imports. In theory, you could replace
them if you update the Bootstrap framework by copying them from that framework
again. Just make sure to modify the import paths to reference the
`./bootstrap/scss` folder at:
```
./scss/bootstrap.scss
```

The `./scss/bootstrap.scss` file is the one responsible to reference all scss
files from the bootstrap library. Generally speaking, you won't touch this file
unless it's necessary to remove any functionality you don't want to be present
on your theme. Keep in mind that due to how SASS works with variables, you must
keep the `./scss/variables.scss` file at the beggining of the @imports.

The `./scss/variables.scss` file is generally where you will spend most of
your time customizing the various Bootstrap settings. Feel free to manually
edit it.

The `./scss/overrides.scss` file contains various Bootstrap and Drupal fixes. It
may contain a few enhancements, feel free to edit this file as you see fit.

The following files are relatively blank (they may contain some code for the
inital sub-theme), but this is where you will actually spend most of your time
specifying specific styling for your sites configuration.
```
./scss/header.scss
./scss/content.scss
./scss/footer.scss
```

And finally, the `./scss/style.scss` file is the glue that holds it all
together and compiles everything into one file. Generally, you will not need
to modify this file unless you need to add or remove imported files. For
example. If you are a file hierarchy wizard and need to separate your theme
into multiple files, insert additional `@import '...';` lines.
