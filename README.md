Building tg_jellybean
======================

1) Initialize (or re-initialize) your aosp repository to use the 
tg_jellybean manifest.

    repo init -u https://github.com/tg-endeavoru-jellybean/android.git -b jb

note: you should be safe to initialize over any aosp repository, however this 
will overwrite some of the aosp repos, and shouldn't be done if you're
planning on building another aosp tree on the same repo in future. It is 
perfectly safe to copy an existing aosp repo and re-initialize it with this manifest.

2) Sync with the remote repository.

    repo sync

This downloads all of the latest changes to your working directory

3) Build. I'm not going to go into too much detail here, as the source.android.com
website has a far more in depth guide, but the following commands should get you
built.

    . build/envsetup.sh
    lunch tg_endeavoru-userdebug
    make otapackage

For more info regarding building android, check out the official android guides
http://source.android.com/source/initializing.html
