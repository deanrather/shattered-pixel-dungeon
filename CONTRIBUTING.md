# Contributing

## Get the Codebase

1. Click the "fork" button to fork the repo
~ 2. Clone the repo down to your workstation
~ 3. Check out a new branch

## Ubuntu Dev Env Setup

1. Install [Android Studio](https://developer.android.com/studio/index.html)

- Click the big green button on the homepage
- Follow the instructions to install & download default packages
- Choose `Check out Project from Version Control` -> GitHub -> shattered-pixel-dungeon
- in `Import Project from Gradle` leave all the default values
SDL location not found error :(
  - restart android studio
  - choose import project
  - navigate to where it downloaded it to earlier
  - open it from there
  - doesn't crash, but fives a gradle sync error: failed to find target with hash string android-25
  - click install missing platform(s) and sync project
  - finish the quickfix wizard
  - still doesn't work... goto logcat tab, click `please configure android sdk`
  - set compile sdk version to api 25, and built tools version to 26
  - click "ok", see more could not find method android() error..
  - set android home restarted
  - open android studio, click settings, sdkmanager, tick android 7.1.1 (api level 25) click ok, done, finish



2. Install [Java](http://openjdk.java.net)

    ~sudo apt-get install -y openjdk-9-jre~
    sudo apt-get install -y openjdk-9-jdk

3. Install [SDKMan](http://sdkman.io)

    curl -s "https://get.sdkman.io" | bash
    source "/home/d/.sdkman/bin/sdkman-init.sh"

4. Install [Gradle](https://gradle.org)

    sdk install gradle 4.0.1
    sdk install gradle 3.3
    sdk install gradle 2.3.2


uninstall / forcibly remove jdk, gradle, sdkman, projects. restart studio. try letting it get everything
same issue
try messing w/ version numbers in config files..
notice NDK is required, go tick that from settings->system->sdk
still errored.. restarted, said there was an gradle update, clicked ok... works now??
click play, setup virtual device, I chose Pixel, chose Nougart 25 as system

wowzers it works!

changing /home/d/StudioProjects/shattered-pixel-dungeon/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java STARTING_STR to 15, hitting play, making new char. hs 15 hp.

build -> build APK
result in: ~/StudioProjects/shattered-pixel-dungeon/core/build/outputs/apk/

copy to your phone
open it
settings -> security -> enable unknown sources

hooley dooley! this works too!


---

## TODO

- [ ] Tidy this document. It's a hot mess.
- [ ] Check whether that change to build.gradle was actually required..