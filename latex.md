#LaTeX
## Tip: Sum Symbol
When using `\sum_{k=1}^{n}`, it shows the limits (k=1 and n) in the same line, if you want to see them above and under the sum symbol, you must put `\displaystyle` before `\sum`.

## Problem: tlmgr - TeX Live Manager doesn't work
`tlmgr install package-name' gives the error:
(running on Debian, switching to user mode!)
cannot setup TLPDB in /home/USER/texmf at /usr/bin/tlmgr line 5308.

### Solution [NOT FIXED YET]
The error is generated when tlmgr was not initialized.
To do it, enter:

$ tlmgr init-usertree

This command will create a folder named texmf folder inside your home directory.

If you want to hide the folder created in your home directory:

export TEXMFHOME=$HOME/.texmf
kpsewhich -var-value TEXMFHOME

And then proceed to rename the folder:

mv ~/texmf ~/.texmf

But even after this the could be an unmet dependency with 'xzdec', enter:

sudo apt-get install xzdec

And in order to use `tlmgr --gui' there's another unmet dependency
with `perl-tk':

sudo apt-get install perl-tk
