Part A - Outdoor 3D scene
I started with the base code that was presented in class for height maps and skyboxes and combined the two.
Afterwards, I added the gui functions just to help debug the program with sliding values and it proved to be quite useful for debugging.
The water is a flat plane that utilizes skybox reflections from the base code from class. However, the water seemed quite boring since it was a still plane.
I added a small set of sin/cos functions that added a wave effect to the plane that was inspired by a shader I saw on shaderfrog.
Another issue that arose though is that the reflection map was not updated, so even with ripples in the water, the reflection was still.
This was fixed by adjusting the normal's X and Z so that the reflection map is updated and look a lot nicer. Maybe I will implement the Fresnel effect later.

Part B - Abstract scene with particles and noise
I decided to do a snow storm effect with the base GPUParticleSystem.js and I am not very happy with it.
A lot of the time I was figuring out how the implemented class worked rather than doing cool things with it.
In the end, I moved the emitter's Y position up so that it was on top of the scene, had it emit down, then I applied a standard gravity of -9.8 to the Y velocity.
I tried using the noise from the webgl-noise to adjust the turbulence but it ended up not working because I could not figure out how it worked, so I kept the default perlin noise png.
Right now, I implemented the wind power and a direction to push the particles in a certain direction. Turbulence affects the pattern of the snowflakes as they fall.