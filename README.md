BoronRom
===========
Blazing fast, Rock-Hard stability. 

Getting Started
---------------
To get started with the Yuanwei sources, you'll need to get
familiar with [Git and Repo](http://source.android.com/source/version-control.html).


Create the Directories
----------------------

You will need to set up some directories in your build environment.

To create them run:

    mkdir -p ~/bin
    mkdir -p ~/BoronRom


Install the Repository
----------------------

Enter the following to download the "repo" binary and make it executable:

    curl http://commondatastorage.googleapis.com/git-repo-downloads/repo > ~/bin/repo && chmod a+x ~/bin/repo

You may need to reboot for these changes to take effect. 
Now enter the following to initialize the repository:

    cd ~/BoronRom


Initializing the BoronRom Source:
---------------

For initializing repo use:

    repo init -u https://github.com/BoronRom/android_manifest.git -b 8.x

Syncing repo:

    repo sync -j8


Compiling BoronRom
---------------

Set up environment:

    . build/envsetup.sh
    
If your device is officially supported by BoronRom, you can do now:

    breakfast <device_codename>
    
...to automatically pull all missing repositories. Then:

    brunch <device_codename>
    
...to start compilation process.


brorn.dependencies sample
----------

    [
      {
        "repository": "android_kernel_<name>",
        "target_path": "kernel/path"
      },
      {
        "repository": "proprietary_vendor_<name>",
        "target_path": "vendor/path"
      },
      {
        "repository": "android_device_<name>-common"
        "target_path": "device/path"
      }
    ]
