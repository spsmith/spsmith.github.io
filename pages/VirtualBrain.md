---
layout: page
title: UW Virtual Brain Project
description: UW Virtual Brain Project
---

![Virtual Brain image]({{'images/brain_screenshot.png' | absolute_url}}) 

The **UW Virtual Brain Project** is an ongoing research project designed to test the effectiveness of virtual reality-based learning. It is developed in Unity and currently runs on Oculus headsets and PCs. I am the main programmer on this project and have assisted in the project's design since it's inception.

The project consists of a number of lessons, each of which guides the user through a tour of a single sensory system within the brain. Short videos of the Visual and Auditory systems are available below. The full experience of each system takes approximately five minutes to complete

<iframe src="https://player.vimeo.com/video/335913527?color=b90014&title=0&byline=0" width="640" height="360" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

<iframe src="https://player.vimeo.com/video/336153928?color=b90014&title=0&byline=0" width="640" height="360" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

For more information about the UW Virtual Brain Project, visit its website at <https://schlosslab.discovery.wisc.edu/projects/#Brain>.

## Platforms

The first Virtual Brain experiment was designed to run on both Oculus Rift CV1 headsets and traditional 2D displays. The exact same lesson can be experienced either in a headset or on a computer monitor. Additonally, lessons were ported to the Oculus Quest, Oculus Go, and Oculus Rift S headsets for display at demos and other events. In Spring 2019, 25 Oculus Go headsets were used in a lecture hall so the students could experience the Visual and Auditory system lessons during class time.

For the second experiment, the [Looking Glass autostereoscopic display](https://lookingglassfactory.com/) was added as a supported platform. This display was used in conjunction with the Oculus and PC experiences. The paper tests used in the first experiment were replaced by a virtual reality testing environment displayed in the Looking Glass, with controls accessed on an accompanying touchscreen display. A simplified view of the brain was displayed on the Looking Glass, and users could interact with it using their hands via a Leap Motion hand tracking system.

![Looking Glass and monitor]({{'images/lkg_and_monitor.jpg' | absolute_url}})

## Development

The Virtual Brain project is developed in Unity. Each lesson consists of a Unity scene including the necessary brain anatomy, interactive objects, and path layout. After the team writes the script for the lesson, work begins in Unity on laying out all the necessary pieces. A path is laid out for the user to follow, travelling through all the relevant brain regions for the lesson. Stations are placed along this path at various points. At each station, the user will stop and hear a voiceover explaining that region of the brain. At some stations, more complex visual effects can occur as well.

![Auditory System scene]({{'images/auditory_scene.png' | absolute_url}})

Each station uses a timeline system. This allows easy adjustment of the voice clips for each segment. Interactive effects and closed captions for each station are laid out on this same timeline.

![Station timeline]({{'images/station_timeline.png' | absolute_url}})

When complex effects are required, I have written several custom scripts to create them in Unity. Each script is written to be easily editable within the Unity editor itself. This allows members of the team to tweak the experience quickly and easily without having to dive into the code themselves. When possible, these scripts also include buttons to allow for testing in the editor, without having to run through the whole experience in a virtual reality headset.

![Audio Waveform script]({{'images/waveform_script.png' | absolute_url}})

Designing tests for the Looking Glass display added an extra layer of complexity. 

## Project Structure

The overall project is organized among several scenes. Each brain system lives in its own scene. Additionally, each display platform has its own scene as well. These scenes can be loaded in combination, meaning that the same lesson can be used with any display platform without requiring any editing of the lesson scene itself. Custom scripts have been written so that when scenes are loaded and unloaded, the correct connections are made between the necessary Unity objects.

For example, each of the VisualSystem or AuditorySystem scenes can be loaded and built with any of the Oculus scenes. Each Oculus scene contains slightly different control schemes and rendering settings in order to properly support each headset. A universal menu is in the works so that all of the display platforms can be supported by one exe, with the desired display platform chosen via command line or other methods.

![Scene structure]({{'images/scenes.png' | absolute_url}})

The scenes within the Virtual Brain make heavy use of Unity's Prefab system. The overall brain anatomy is contained in several nested prefabs. This allows the brain anatomy to remain consistent between scenes, while each individual scene contains only the specific brain regions it needs. Additonally, any edits made to the brain models or layout within the prefab will be propagated to the various scenes automatically.

![Brain prefab structure]({{'images/brain_prefab_structure.png' | absolute_url}})

Many other parts of each scene are implemented as prefabs as well. A nice side effect of this is that since a lot of the data within the scene is actually contained in the prefabs themselves, the project functions much better when it comes to version control systems. Individual pieces of the project are easy to revert when necessary, and complex merges happen much less often.

Unity's Scriptable Object system is used for configuration files within the project. As an example, the settings for transitions between solid and transparent materials are contained within scriptable objects, one per shader, so the same settings can be used across many objects in the scene.

![Shader Properties objects]({{'images/shader_properties.png' | absolute_url}})

The code for the Virtual Brain project uses lots of design patterns and inheritance to keep the code as streamlined as possible. Script files are kept small and modular, which has done wonders for keeping the project maintained across various Unity versions and project design overhauls. Additonally, much of the code in the project lives in its own Unity Package. This enables the code to be easily shared between multiple Unity projects. See the [Unity Scripts page](Other.html#Unity-Scripts) for more details.

### Tools Used

*Unity (various versions, from 2017.1 through 2019.3)*

*Programming languages used: C#, Python*
- All of the Unity scripts used in this project were written in C#.
- Python was used to write various scripts to assist in the research process. This included the script for running the Virtual Brain experiment itself as well as scripts for organizing data from test subjects and automatically grading tests during the experiment.

*Blender*
- Many of the 3D models used in the Virtual Brain project originated from MRI scan data. After converting this data into a 3D model format, further cleanup was performed in Blender. This included smoothing out various artifacts in the model by hand, texturing some models that needed color variation across their surface, and reducing geometry on models to optimize rendering speed in virtual reality.

*Photoshop*
- Photoshop was used for the creation of any 2D assets needed for the project, such as the UI.