# Garbage Script for Linux

Instead of using rm and risk loosing an important file, this script can be aliased to rm to have files and directories automatically moved to a specified directory to be removed later.

# Setup

In your .bashrc, use the following line to remove files in the garbage that are older than 30 days:

find ~/.garbage -mtime +30 -mindepth 1 -exec \rm -Rf {} \; 2> /dev/null

Also, make an alias to rm.  Something like
alias rm='~/bin/garbage'

