
## Introduction

This is a fork of the official [PortableApps.com Launcher][1]. I forked this project because I wanted to incorporate some ideas I had that I believe would better this project in its entirety. So instead of going to [PortableApps.com][2] and sharing my ideas ([a superfluous attempt][3] was already made; to what seemed like no avail), I feel it would be much more advantageous on my part to just implement these ideas instead. 

I have no real expectations that any of these ideas will actually be pulled into the official version of __PAL__ (_PortableApps.com Launcher_) but if any of them do than kudos.. lol. If anyone is actually reading this and does find some of these concepts to be useful then maybe support my effort in supporting their cause. 

I should say that what I'm going to be adding to this variant of PAL is what works for me and my environment. All the concepts that you find here should work with any other environment unless explicitly expressed otherwise. So like I say in a recent motto I have recently just adopted, _"Port and let portable!"_ — You see what I did there? Lol. If you don't, no worries; I guess I should just _live and let live_.

## Feature Concepts

Here's a small list of a few ideas that I want to try and implement with this project. These are just things I plan on working on in my spare time and while the ideas listed below are not recognized by PortableApps.com please be aware that using some of the things you find in this variant of PAL can and most likely will be buggy. 

* __Support for NSIS3__
Well, support for [NSISPortable][4] rather which is packaged with the latest release of NSIS. The current official release of PAL is using NSIS v2.46.5-Unicode which is actually packaged with the project. So I would like to completely remove the need for this dependency entirely.

* __Manifest Support__
The correct way to mark a program in regards for UAC permissions is to embed an _application manifest_. This lets the host PC know how to handle what the program needs in regards for permission levels. Developers can specify their programs level of execution or better known as `requested execution level`.

* __.NET Handling__
I'll just be adding a means for checking a system for the required version of the .NET Framework because John T. Haller [explains][5] in great detail how the .NET Framework has no real practical means for portability when it comes to Portable Apps. He ends his article with, "_...applications based on .NET simply can't be considered portable due to the fact that the files they need can't be bundled portably and won't be on a large number of PCs you encounter in the wild._"

* __Support Registering Libraries__
The official release of PAL has no native support for registering libraries (DLLs), so I will try to add support for registering files. Be aware though that a program developer has complete control over what happens when you call _RegSvr32_ which is what is used by `RegDLL` (the native command used by NSIS for registering files). With that being said, my ideas on this topic may be buggy.

* __Support Services__
The support for services is by default disabled in the official builds of PAL. In the source code it states that they might be unstable and the plugin is large in size. I plan on not using a plugin to support services, instead I plan on dealing with this by using the command line with a few functions and macros to try and keep things simple.

* __Etc. Etc. And So On__
Other things could follow depending on my availability, interest.. and of course the interest and support from others. So with that being said, this little project might not even see the light of day. Lol.

## Added Features

I've only just forked this project and have barely started writing this little readme file so nothing has been added to this project just yet but bare with me and be patient!

## Contributors

This forked project has been started by [demon.devin][author] and hopefully maintained on a regular basis. However, if you would like to be a part of this then please do not hesitate on getting involved! I'm always open to new ideas and a willingness for the betterment of all things code. =)


[1]: https://github.com/GordCaswell/portableapps.comlauncher "PortableApps.com Launcher"
[2]: http://portableapps.com/ "PortableApps.com/"
[3]: https://portableapps.com/node/56500 "A Superfluous Discussion"
[4]: https://portableapps.com/apps/development/nsis_portable "NSIS Portable"
[5]: http://johnhaller.com/useful-stuff/dot-net-portable-apps ".NET Availability and Viability With Portable Apps"
[author]: https://softables.tk/ "Softables.tk/"