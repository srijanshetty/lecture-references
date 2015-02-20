papers
======

A git-annex repository of resources for learning a multitude of topics.

Using
-----

First install `git` and `git-annex`. Then:

```sh
git clone git://github.com/srijanshetty/lecture-references
git-annex init local
git-annex get .
```

If you want just some particular lecture:

```
git-annex get databases/normalization/bcnf-3nf.pdf
```

Please open an issue if you cannot download any lecture so that I can mirror them.

How I created this?
-------------------

```sh
cd papers
git init
git remote add origin git@github.com/srijanshetty/lecture-references
git-annex init laptop
git annex addurl --file=databases/normalization/bcnf-3nf.pdf http://www2.cs.sfu.ca/CourseCentral/354/jpei/slides/BCNF-3NF.pdf
git-annex add .
git commit -m "lectures"
git config remote.origin.annex-ignore true  # Because GitHub doesn't store annexed content.
git push origin master git-annex
```
