# README-repo-update.txt
# 07/20/26

The directory--
  /GliderWinchItems/docs-common/scripts/gitpull
has scripts for cloing or updating the repos in the two
github groups GliderWinchItems and GliderWinchCommons

This scripts assume there are two directories present and
at the same level, e.g.
  $HOME/GliderWinchCommons
  $HOME/GliderWinchItems

To execute the scripts need to be present, which means
at least one clone is needed, e.g. --
  cd $HOME/GliderWinchIetms
  git clone ssh://git@github.com/GliderWinchItems/docs-common
To execute the cloning--
  cd $HOME/GliderWinchItems
  $HOME/GliderWinchItems/docs-common/scripts/gitpull/gitgroupupdate

This should result in stepping through two lists of repos stored in
e.g.
 $HOME/GliderWinchItems/docs-common/scripts/gitpull/gitpullitems.txt 
 $HOME/GliderWinchItems/docs-common/scripts/gitpull/gitpullcommons.txt
These two lists have the names of the repos on github to be cloned, or
updated with a "git pull".

To simplify the running of the scripts, place a script in
  $HOME/bin
(Which should be in the PATH look up) 
A script for the for when the G*Items and G*Commons are in a different partition,
would be--
  echo "cd /mnt/*fd/home/deh; GliderWinchItems/docs-common/scripts/gitpull/gitgroupupdate" > ~/bin/repoupdate; chmod +x ~/bin/repoupdate
This results in a 'repoupdate' in ~/bin that will execute from anywhere 
by entering--
  repoupdate

  



