# Part 3: Developing XR with WebXR #

Third part of the Extended Reality Specialization course by Michael Nebeling from University of Michigan.

Official link on
Coursera: [Developing AR/VR/MR/XR Apps with WebXR, Unity & Unreal](https://www.coursera.org/learn/develop-augmented-virtual-mixed-extended-reality-applications-webxr-unity-unreal)

The Hanoi Tower app is an augmented reality app to play the Hanoi Tower game and implemented with AFrame, a great tool
for AR built on top of the WebXR JavaScript library.

Checkout the code [here](hanoi-towers/README.md) or try the Hanoi Tower Game online
on [CodePen.io](https://codepen.io/davidsantucci/pen/OJzxGrp).

## Abstract of the course ##

This third course in the XR for Everybody specialization is geared toward the technical development of XR experiences.
The course provides learners with a more technical mental model of XR technologies and the tools to approach XR
development with confidence. It walks through the stages of development for both VR and AR projects, introducing the
main XR development platforms as well as the key methods and tools. This third course also helps learners infer advanced
XR requirements from physical/digital prototypes and teaches them how to differentiate major technical concerns,
estimate development costs, and plan research necessary to advance XR.

This course also has an honors track that guides learners in the implementation of 3D, VR, and AR scenes in WebXR using
A-Frame and in Unity, and helps them generate a development plan with clear milestones and deliverables.

## Notes from the course ##

**Interaction Design**
At the highest level, there are three types of XR interactions:
1. Implicit Interactions 
   1. Camera-based: gaze, eye
   2. System-based: location, time, counter, event, physics
2. Explicit Interactions
   1. User-based: controller, hand, finger pose/gesture; voice command 
   2. Environment-based: marker, object
3. Combination of the above
   1. System-based+user-based (mixed-initiative): dwell on target 
   2. User-based+user-based (multi-modal): gesture+speech command


## Assignments ##

### Assignment 1 - 3D Scene ###

My idea is to represent the well-known game "the Hanoi Towers". The game is very simple, here the 3 basic rules from
Wikipedia:

1. "Only one disk may be moved at a time."
2. "Each move consists of taking the upper disk from one of the stacks and placing it on top of another stack or on an
   empty rod."
3. "No disk may be placed on top of a disk that is smaller than it."

As a first step I created a sketch on paper to understand the 3D scene compositions. In attachment the sketch. Then I
prototyped the 3D scene with 3D primitives using A-Frame and codepen.io. It was my first time with this technology, and
I started from the "A-Frame 360 Template" provided by Prof. Nebeling on codepen. I tried different angles for the camera
to reach a good starting perspective for the scene. At the end of the tests I decided to go with a frontal view.

In attachment a screenshot of my experiments and the first good results with A-Frame. I used torus and cylinder as
primitives.

### Assignment 2 - VR Scene ###

Continuing the work started with the 360 scene, I decided to create a basic interaction to make the experience more
effective: when the camera rig is pointing to a specific disk, the disk is moved to the left rod. If the user wants to
move the disk to the rod on the right, it is enough to do the same operation again (left+left = right, as we only have 3
rods).

To create this experience I took inspiration from Prof. Nebeling's templates on codepen. In attachment a picture with
the final result and a comparison with the previous state.

The final experience can be definitively improved creating a better interaction with the objects (the disks), but I
suppose that the result is sufficient for this stage of prototyping.

### Assignment 3 - AR Scene ###

For the Hanoi Tower project I decided to use a marker-based approach for the AR and I adapted the scene for this
purpose. The expected interaction is the same of the VR approach (when the camera rig is pointing to a specific disk,
the disk is moved to the rod on the left) but the final result with AR is very effective. The support for marker-based
AR interaction is done with A-Frame primitives and I extended the examples provided by Prof. Nebeling on codepen.

I attached the screenshots and the link to codepen with the code.

https://codepen.io/davidsantucci/pen/OJzxGrp

### Honors Peer-graded Assignment - Final Prototype ###

Project Title:
> Hanoi Towers AR

Design Idea & Sketch
_(In a few sentences, describe the main idea and inspiration for your 3D/VR/AR scene. If possible, share the sketch
based on which you modelled your work. Even if you just submit a 3D scene without particular adaptations for AR/VR, make
it clear whether you have been designing for AR or VR.)_
> The main idea is to represent the "Hanoi Towers" game in a AR interactive version. 
> The game is very simple, here the 3 basic rules from Wikipedia:
> 1. "Only one disk may be moved at a time."
> 2. "Each move consists of taking the upper disk from one of the stacks and placing it on top of another stack or on an empty rod."
> 3. "No disk may be placed on top of a disk that is smaller than it."

As a first step, I created a sketch on paper (in attachment) to understand the 3D scene compositions. Then I prototyped
the 3D scene with 3D primitives using A-Frame and codepen.io (the link is also attached).

Development Approach and Tools
_(State which XR platforms and tools you were using and briefly describe your development process and experience with
the tools. What are the key interactions you wanted to implement? What were some of the design and technical challenges
you had? How close did you get towards your envisioned final AR/VR user experience with your 3D/VR/AR scene?)_

> I used WebXR for the experiment, and I used codepen and A-Frame. It was my first time with this technology, and
> I started from the "A-Frame 360 Template" provided by Prof. Nebeling on codepen.
> I tried different angles for the camera to reach a good starting perspective for the scene.
> At the end of the tests I decided to go with a frontal view. In attachment a screenshot of my experiments and the
> results with the AR approach. I used torus and cylinder as primitives to build the scene in a realistic way.

Final 3D/VR/AR Scene
_Submit screenshots, photos, or a video of your final 3D/VR/AR scene walking us through your design._

TITLE:
> Hanoi Towers - From a sketch to a VR model with WebXR

CAPTION:
> Built a simple interactive game based on Hanoi Towers using WebXR and A-Frame.
> Starting from a sketch, design the 360 models and then arrive to a final AR model with a basic interaction.

Envisioned AR/VR User Experience
_(Provide a description of your envisioned final AR/VR user experience. Summarize the key interactions you wanted to
implement in your prototype.)_
> The idea is to implement the game of the Hanoi Towers in an interactive mode taking advantage of AR.
> I decided to create a marker-based interaction to make the experience more effective and stable: after placing the
> marker (I used the regular "[Hiro](./hiro-marker.png)" marker for this purpose) when the camera rig is pointing to a specific disk,
> the disk is moved to the left rod. If the user wants to move the disk to the rod on the right, it is enough to do
> the same operation again (left+left = right, as we only have 3 rods).
> To create this experience I took inspiration from Prof. Nebeling's templates on codepen. In attachment a picture
> with the final result and a comparison with the previous state.

Provide a list of open issues and ask specific questions that you would like to have feedback on regarding your 3D/VR/AR
scenes.
> Even if I think the result is sufficient for this stage of prototyping, the final experience can be definitively improved:
> - Creating a better interaction with the objects
> - Use 3 markers to customize the placement of the 3 rods in the space
> - Validate moves (at the moment there is no validation)
