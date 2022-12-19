# textual-astview

![](img/astview.png)

## Introduction

This is a combination of a [Textual](https://textual.textualize.io/) widget
library and also a command line too. The aim is to provide tools for
displaying and exploring the [Python
AST](https://docs.python.org/3/library/ast.html).

## It's early days

This is a very early release of this code, it's still very much a work in
progress. This means things may change and break; it's also sitting atop
Textual which is, of course, still undergoing rapid development. As much as
possible I'll try and ensure that it's always working with the latest stable
release of Textual.

Also, because it's early days... while I love the collaborative aspect of
FOSS, I'm highly unlikely to be accepting any non-trivial PRs at the moment.
Developing this is a learning exercise for me, it's a hobby project, and
it's also something to help me further test Textual (disclaimer for those
who may not have gathered, I am employed by
[Textualize](https://www.textualize.io/)).

On the other hand: I'm *very* open to feedback and suggestions so don't
hesitate to engage with me in the issues. I can't and won't promise that
I'll take everything on board (see above about hobby project, etc), but
helpful input should help make this as useful as possible in the longer
term.

## Installing

The package can be installed with `pip` or related tools, for example:

```sh
$ pip install textual_astview
```

As well as the library (which I'll give some minimal documentation for below
-- hopefully more comprehensive documentation will follow eventually), a
command is also installed called `astare`. This can be used to load up and
explore a Python source file.

## The library

In the library you'll find the following Textual widgets:

### `ASTView`

This is the main AST tree view. Create it by passing a Python `Path` object
for the file you want it to display.

### `Source`

This is a widget that shows the source code for a Python file. Create this
by also passing it a Python `Path` object for the file you want it to
display. It, of course, only really makes sense to have it show the same
file as the `ASTView` it'll work in concert with.

### `NodeInfo`

This is a widget that is intended to be used as a footer bar, of sorts,
giving a summary of where an `ASTView` is focused.

## Putting the widgets together

The way they all work is far from final, so the best way to get an idea of
how to use them, right now, is to take a look at [the code for
`astare`](./textual_astview/app/astare.py). There's not a whole lot to it
(right now anyway) so hopefully it'll be easy enough to follow.

## TODO

- [ ] Add some actual error checking around loading the file.
- [ ] Test on Windows.
- [ ] Test on GNU/Linux.
- [ ] Dial in the colour and style until I'm really happy with it.
- [ ] More navigation features.
  - [ ] Lots of keyboard navigation coverage.
  - [ ] Searching.
- [ ] Extend and test all the styling options.
- [ ] Allow loading another file without leaving the app.
- [ ] A more "rainbow" approach to highlighting the source and tree position.
- [ ] Keep on having fun hacking on it.
- [ ] Other stuff. I'm sure there's other stuff.

[//]: # (README.md ends here)