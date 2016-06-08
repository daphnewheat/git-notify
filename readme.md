git-notify
========

This little bash script will watch your origin/master for updates every 60 seconds and uses notify-send to alert you of new commits.

I asked [this question](http://stackoverflow.com/questions/5082001/is-there-a-tool-to-watch-a-remote-git-repository-on-ubuntu-and-do-popup-notificat) on StackOverflow to find out if there was a tool to notify me of commits to remote git repositories, and the answer came back no!

Thus, git-notify was born!

Usage:
----------

    ~/code/some-git-repository $ git-notify

The script will run in the background. If you want to kill it later, you can do:

    ps aux | grep '[g]it-notify'

Which will output something like:

    jake      9541  0.0  0.0  12012  1392 pts/3    S    12:54   0:00 /bin/bash ./git-notify

Note the first number in the list, 9541, that is the PID of the script. You can now terminate it like so:

    kill 9541

Enable auto-update:
------------------------
~/code/some-git-repository $ ~/path-to-git-folder/git-notify/git-notify remote/branch remote

Make sure to be in the git repository the remote is from. Both remote/branch and remote must be included in that order to work. If updates are enabled then "Update" will be shown in the desktop notification.

Example:
Notification: ~/Documents/git $ ~/Documents/git/git-notify/git-notify upstream/develop
Update: ~/Documents/git $ ~/Documents/git/git-notify/git-notify upstream/develop upstream

Installation:
------------
Just download git-notify and put it somewhere in your path.

Jake Moffatt, jakeonrails@gmail.com

