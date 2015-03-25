The LBNE Far-Site Detector Closeout document.
====

Related documents and links
---

* [The LBNE Far Detector Closeout](https://github.com/DUNE/lbne-fd-closeout)
* [The ELBNF (name subject to change) CDR](https://github.com/DUNE/lbn-cdr)
* [Proposal for a Full-Scale, Single-Phase Prototype at CERN](https://github.com/DUNE/cern-prototype-proposal)
* [CD-1 Preparation Page](https://web.fnal.gov/project/LBNF/ReviewsAndAssessments/CD-1Preparation/SitePages/CD-1%20Preparation%20Home.aspx)

Guidance
---

The definitive source for guidance for CDR authors is available in the
document:

  volume-readme.pdf

which is part of the https://github.com/DUNE/lbn-cdr repository.  You can find a recent copy in the [lbn-cdr release area](https://github.com/DUNE/lbn-cdr/releases)

Releases
---

Fixed releases of this document with PDFs are available from the [release area](https://github.com/DUNE/lbne-fd-closeout/releases) as zip or tar.gz archives.

An auto-built PDF is made shortly after each commit and is available [here](https://dune.bnl.gov/tmp/).

Getting started
---

Clone the repository:

    git clone https://github.com/DUNE/lbne-fd-closeout.git
    cd lbn-fd-closeout

To build the documents you need `pdflatex` and `bibtex`.

    pdflatex lbne-fd-closeout
    bibtex lbne-fd-closeout
    pdflatex lbne-fd-closeout
    pdflatex lbne-fd-closeout

Unless references change, it is usually sufficient for subsequent
builds to run only:

    pdflatex lbne-fd-closeout
    pdflatex lbne-fd-closeout

You may need the second run to get the paging and numbering correct.

The technical editors are responsible for producing a final version
free of any editing markup.  This is produced by replacing each
of the `pdflatex lbne-fd-closeout` commands above with:

    pdflatex "\def\isfinal{1} \input{lbne-fd-closeout}"

Repository
---

It is strongly recommended that you use Git to make a clone of this
repository, to commit your changes to your clone and to push those
changes back to GitHub.

To get "push" access to this repository send your GitHub user name to
Brett (see contacts below).

General git procedure.  

    cd lbne-fd-closeout/
	git pull

Before editing it's good to `git pull` to update your working area
with any commits that other authors have made.  When you finish your
editing session commit your work.  Commits are always and only local.

    git commit -a -m "Some commit message"

If you have made any new file you must first add it:

    git add the-new-file.tex
    git commit -a -m "Some commit message"

You can see what git thinks of your working directory with:

    git status

Commits are always local.  To share them you must push the commits
back to GitHub. 

    git push

Sometimes other people may have pushed their commits since you last
did a `git pull`.  If that happens the `git push` will fail with a
message telling you so.  Just do a pull and a push:

    git pull
	git push


From time to time if someone else changed the same line of text as you
have then a git pull will lead to a conflict.  To resovle conflicts,
edit the conflicting files and look for lines like:

    <<<< HEAD
	your text
	====
	their text
	>>>> somelabel

Edit away the markers, keeping the text you want to keep and then

    git add the-conflicting-file.tex
    git commit -a -m "Fixed conflict"
    git pull

## If you are unable to use Git

If you are unable to use Git, your contributions will still be accepted
but will lead to additional effort for the technical editors.  To
minimize that additional effort we ask that you **please** follow these steps:

* Start editing from the most recent
  [tagged release](https://github.com/DUNE/lbn-fd-closeout/releases) or the
  specific release you may be requested to use.
* Unpack the release archive (.zip or .tar.gz) on your computer.
* Make your edits inside the directory/folder that is created.
* When you have finished, remove any generated files (eg, `volume-*.pdf`).
* Repack the directory (as `.zip` or `.tar.gz`).
* Upload this archive to the [document library](https://web.fnal.gov/project/LBNF/ReviewsAndAssessments/CD-1Preparation/Shared%20Documents/Forms/AllItems.aspx). (FNAL
[Services account](https://fermi.service-now.com/kb_view.do?sysparm_article=KB0010542) required)

Note: the technical editors must know the release version that you
started with.  This should be part of the unpacked directory/folder
name so do not strip it out.

If you are unable to edit in LaTeX, please talk to Anne (see contacts below).

Contacts
---

* Anne Heavey <aheavey@fnal.gov> 630-840-8039 (technical editor, content)

* Brett Viren <bv@bnl.gov> (technical editor, LaTeX machinery and repository)
