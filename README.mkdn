[Android Ice Cold Project for Oppo R7Plus](http://aicp-rom.com)
==========================================


Download the Source
===================

Please read the [AOSP building instructions](http://source.android.com/source/index.html) before proceeding.

Initializing Repository
-----------------------

Repo initialization:

    $ repo init -u https://github.com/AICP/platform_manifest.git -b mm6.0


Add device specific files and repo changes (local manifest)

    $ mkdir .repo/local_manifests
    $ curl -o .repo/local_manifests/r7plus.xml https://raw.githubusercontent.com/teemodk/manifest/aicp/local_manifests/r7plus.xml
     

sync repo (download it all) :

    $ repo sync



Building
--------

After the sync is finished, please read the [instructions from the Android site](http://s.android.com/source/building.html) on how to build.

    $ . build/envsetup.sh
    $ lunch aicp_r7plus-userdebug

    $ mka bacon 
      or
    $ make -j# bacon
    
    replace # with number of cpu threads you want to use
