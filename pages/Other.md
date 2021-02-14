---
layout: page
title: Other Projects
---

# Unity Scripts

![Unity Scripts repository]({{'images/unity_scripts.png' | absolute_url}})

With the introduction of Unity's Package system, it became possible to easily share code between different Unity projects. I created the UnityScripts repository as a home for all the Unity scripts I had written that were generic enough to be used in multiple projects. The repository is designed to be used as a Unity package. It can either be installed into a project as a standalone package, or used as a local package that exists outside of the project itself. When used this way, it means that any changes to code in the package will be visible to any project on the local machine that uses it. This has been invaluable when implementing new features into my Unity projects in the lab.

As of right now, the package contains many scripts designed to streamline the Unity workflow. Various design patterns have been implemented such as the state machine and command patterns. A system that supports file input/output for various filetypes using Scriptable Objects makes it easy for other Unity scripts to interact with any file in the project. An input system using Scriptable Objects for polling buttons uses generics, so that buttons from one controller (e.g. a keyboard) can be replaced with buttons from another (e.g. an Oculus Touch controller) without the underlying script having to know.

# Ice Cube Virtual Reality Experience

![Ice Cube in virtual reality]({{'images/ice_cube.png' | absolute_url}}) 

I did some work porting the lab's existing [IceCube virtual reality experience](https://pvre.discovery.wisc.edu/) to the latest version of Unity, as well as submitting it to the Oculus Store as a free app. This involved some bug fixes and code updates, as well as adding menu functionality to meet store submission requirements. A version was also made for the Oculus Go and Oculus Quest standalone headsets.
