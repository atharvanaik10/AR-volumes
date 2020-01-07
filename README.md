## Modeling Solids of Revolution in Augmented Reality

### Introduction

Augmented Reality(AR) is a way to visualise, navigate, and interact with virtual objects in the real world. It is a result of superimposing information such as images, sound and text on the world we see. It is a relatively new technology which has a lot of untapped potentials - especially in education and entertainment. Apps such as Pokemon Go and SkyMap harness augmented reality to create overlays on a camera image. In this project, I explore how I can use AR to model solids of revolution.

### How does AR work?
ARKit combines device motion tracking, camera scene capture, advanced scene processing, and display conveniences to simplify the task of building an AR experience.

1.  Orientation tracking: 
ARKit uses the device’s internal sensors to track rotation in three degrees of freedom, but it’s like turning your head without walking anywhere—changes in physical position aren’t tracked here, just orientation in a spherical virtual environment with the device at the origin.
    
2.  World Tracking: 
It tracks the device’s camera viewing orientation and any changes in the device’s physical location. So unlike orientation tracking, it understands if the device has moved two feet to the right.  
    Further, ARKit uses a process called visual inertial odometry, which involves identifying key physical features in the environment around the device. - depth
    
3.  Plane Detection: 
Plane detection uses the world map to detect surfaces on which augmented reality objects can be placed.


### My project
I want to use augmented reality to model a solid of revolution. The first step was to find a way to create a 3D model. After some research, I found that the easiest way was Wolfram Mathematica, which lets you code 3D objects in Wolfram Language and then export them as 3D files. 

SceneKit is Apple’s built-in software for AR App development. It is housed inside Xcode, which is Apple’s Integrated Development Environment (IDE, read: editor) for Apple app dev. SceneKit was useful for me because of the ease of connecting objects to their respective views in the app and scripting their behaviour. SceneKit makes it seamless to create and reference code in objects, and to work with Xcode and Swift to create an easier app experience. Because of this, I decided to use SceneKit for my project.

![XCode](https://user-images.githubusercontent.com/35256233/71882886-398f1d00-3170-11ea-8fef-7380a098661e.png)

Once I had decided on SceneKit, I created a new app in Xcode, and created its related Views. Each ‘screen’ that the user sees is a new view, hence, I had to create a new view for each button.  The next step was to create the code for each of my AR Views. The code for each ‘AR’ View would be almost exactly the same, with the only difference being the Object that is imported.

![App screenshot](https://user-images.githubusercontent.com/35256233/71882971-64797100-3170-11ea-864e-e0ac5754ee87.png)


### Challenges
I faced tons of challenges along the way. In the two weeks that we had to finish this project, I had to overcome hurdle after hurdle. The first problem was that I did not know how to build an App, let alone an AR app. This meant that I had to watch tutorials and read the documentation on how I could get started. After this, I had to figure out how I would make 3D objects. My initial idea was to take in user input which would then model a surface of revolution. This was the hardest part of my project, and in the end, I couldn’t find any way to do it. To the best of my knowledge, it had never been done before. Generating 3D shapes in real time based on user input is possible in ARKit, Apple’s AR Software Development Kit (SDK), but it is only possible to do so using Bézier curves, which was a complicated topic with a steep learning curve.


### Conclusion
A possible extension in the future could be to implement this custom user generated models using Bézier curves, but this would be relatively difficult as it involves having a series to approximate a Bézier curve to a rectangular curve.  
Overall, this project has sufficiently challenged me, and it has had a significant learning curve. However, I hope to continue to improve it in the future, while making it more accessible and beautiful.
