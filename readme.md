Octogen OS Powered by Android 8.0 Oreo
======================================

Create dirs, and install soft, libs
-----------------------------------

    sudo su
    add-apt-repository ppa:openjdk-r/ppa
    apt-get update
    apt-get install bison build-essential curl ccache flex lib32ncurses5-dev lib32z1-dev libesd0-dev libncurses5-dev libsdl1.2-dev libxml2 libxml2-utils lzop pngcrush schedtool squashfs-tools xsltproc zip zlib1g-dev git-core make phablet-tools gperf openjdk-8-jdk
    exit
    
    
Install repo
------------

    mkdir ~/bin
    PATH=~/bin:$PATH
    cd ~/bin
    curl http://commondatastorage.googleapis.com/git-repo-downloads/repo > ~/bin/repo
    chmod a+x ~/bin/repo
    

Create octogen folder
----------------------

    mkdir ~/octogen
    cd ~/octogen
    

GIT config (nickname, e-mail)
-----------------------------

    git config --global user.email "mail@domain.com"
    git config --global user.name "login"


Rsa key for github
------------------

    ssh-keygen
    [ENTER]
    [ENTER]


See rsa key
-----------

    cd ~/.ssh/


Copy public rsa key
-------------------

    cat ~/.ssh/id_rsa.pub

Go to GitHub
------------

    https://github.com/


Go to settings -> SSH keys
--------------------------

    https://github.com/settings/keys


Please click "New ssh key" button
---------------------------------
Title:
    
    Your Title

Key:
    
    Your Key (paste key and click add ssh key)


To initialize your local repository use
---------------------------------------

    repo init -u git@github.com:OctoDev-Project/octogen_manifest.git -b o
    

Then to sync up:
----------------

    repo sync -jX

Build command is
----------------

    cd ~/octogen
    . octogen.sh
