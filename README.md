# gamedev-playground

Goal of this repo is to do some game development.

Currently exploring game development on manjaro linux, with intention to build WebGL games.

## unity

This video discussing how to Export Unity Games to WebGL was inspiration for creating this repo https://www.youtube.com/watch?v=JZqTHjjtQHM&ab_channel=Simmer.io

## Installing on manjaro linux

Download the AppImage from Unity site for linux

    yay -S appimagelauncher
    chmod u+x UnityHub.AppImage
    ./UnityHub.AppImage

Once Unity Hub is up and running, click on the Profile Icon and 'sign in' or register an account

After signing in:
- click 'License Management'
- click 'Activate New License'
    - select 'Unity Personal' if using for personal projects
- After the license is active
    - go back to main Unity Hub menu
    - click 'Installs'
    - Add
    - select which release, 'Unity 2019.4.21f1 (LTS)
    - Then select which modules wanting to add on
        - Selected Linux, WebGL and Documentation.  Can add others later

The install process may take a little bit of time

After install finishes:
- Go back to main menu
    - Select 'Projects'
    - Click 'New', select Unity version
    - Select type of project, give it a name and create

Unity appears to install everything to `~/Unity`

Switching to exploring godot game engine, since unity, while it will run on my system, seems to have a lot of errors building game kits, and I am unable to successfully export to WebGL.

## godot

https://wiki.archlinux.org/index.php/Godot_Engine

Excellent list of questions about Godot, worth the read: https://docs.godotengine.org/en/stable/about/faq.html

Install latest dev version

~~`yay -S godot-git`~~

Compiling from scratch was unnecessary, and also problematic, as the built godot complained it could not detect compatible drivers for my gpu.

Solution was to just download the linux 64-bit godot from godot website.  This worked flawlessly.

Inside the godot editor there are demo projects to open and explore.  

I was able to successfully load a 2d game up, export it to html5, host http server locally using python `python -m http.server 8000 --bind 127.0.0.1` and everything just worked.  https://docs.godotengine.org/en/stable/getting_started/workflow/export/exporting_for_web.html

However testing html5 output is even easier than that, as there is an html5 button within the editor for running the project immediately without needing to export.


## exporting a godot game to html5 and hosting on github pages

https://posworkshop.space/posts/godot-deploy-web-export-to-github/
