Example-Session for creating a modern LaTeX document from scratch
using LaTeX.

The repository contains the most important concepts. The example document
`paper.tex` is extended in chronological order.

Starting from scratch, each revision introduces a new concept and
is compilable via `pdflatex`.

## Usage ##

After cloning the repository, checkout each revision in
chronological order, look at the changed `paper.tex` in your
favourite text editor, compile the file via `pdflatex` and view
the result in a PDF-viewer.

For example using these commands:

    $ git checkout master~11  # where 17 is the number of commits
    $ git show                # should display the 'from scratch' rev
    $ git checkout master~10
    $ git show                # and reload in editor
    $ pdflatex paper          # and (automatically) reload in PDF-viewer
    $ git checkout master~9
    $ git show
    $ pdflatex paper
    ...

At the bibliography session you need to call:

    $ pdlatex paper
    $ bibtex paper
    $ pdflatex paper

Some changes need two runs of `pdflatex` (e.g. inserting a
reference).

After changing the babel-language you probably need to delete
`paper.aux` before running `pdflatex` (else `pdflatex` errors out
with a not quite intuitive message).

## Contact ##

Georg Sauthoff <gsauthof@techfak.uni-bielefeld.de>
