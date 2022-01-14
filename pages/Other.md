---
layout: page
title: Other Projects
---

# Unity Scripts

![Unity Scripts repository]({{'images/unity_scripts.png' | absolute_url}})

With the introduction of Unity's Package system, it became possible to easily share code between different Unity projects. I created the UnityScripts repository as a home for all the Unity scripts I had written that were generic enough to be used in multiple projects. The repository can either be installed into a project as a standalone package, or used as a local package that exists outside of the project. When used as a local package, it means that any changes to code in the package will be visible to any project on the local machine that uses it. Support for virtual realitty platforms is enabled by a define flag, to allow this package to be used by projects without VR support if necessary. Use of this package greatly increased development speed for all of the Unity projects I worked on in the Virtual Environments Group. I was the sole developer for this repository, but it was used by many lab members.

The package contains many scripts designed to streamline the Unity workflow. Various design patterns have been implemented such as the state machine and command patterns. Generic data structures have also been created, to serve as baselines for other scripts custom to each project. A system that supports file input/output for various filetypes using Scriptable Objects makes it easy for other Unity scripts to interact with any file in the project. An input system using ScriptableObjects has also been created, enabling easy drag and drop input setup for multiple platforms. Scripts can be written to accept input from a generic button type, and the specific button for desktop, VR, or other platforms can be chosen in the editor.

Check out the contents of this package on the [wiki](https://github.com/widVE/UnityScripts/wiki)!

# Ice Cube Virtual Reality Experience

![Ice Cube in virtual reality]({{'images/ice_cube.png' | absolute_url}}) 

I did some work polishing and porting the lab's existing [IceCube virtual reality experience](https://pvre.discovery.wisc.edu/) to the latest version of Unity, as well as submitting it to the Oculus Store for download as a free app. My work consisted of bug fixing and code updates, as well as adding menu functionality to meet store submission requirements. The main IceCube laboratory model was also recolored and optimized using Blender. A version was also made for the Oculus Go and Oculus Quest standalone headsets.
