// refer to thebookofshaders.com
// and further shader school
1. Shader language has a single main function that returns a color
at the end.

2. gl_FragColor is a reserved global variable which should be given 
the final color3. 
Well known types are int, float, bool, vec2, vec3, vec4.

gl_FragColor is a vec4 standing for (r,g,b,a) all of which 
are normalized from 0 to 1

float types are vital in shaders, so level of precision is crucial
Lower presicion means faster rendering but bad quality
e.g. precision mediump float makes all floats to medium precision

A good idea is to always put decimal point (.) in your floats

 You can make C like functions like following :
 vec4 red(){
 	return vec4(1.0, 0.0, 0.0, 1.0);
 }


* Some inputs will need to be equal (uniform) to all the threads/processors in the GPU and hence are called uniforms.
Supported types for uniforms are :
float, vec2, vec3, vec4, mat2, mat3, mat4, sampler2D and samplerCube.

An example is following
```
uniform vec2 u_resolution; // canvas size(w/h)
uniform vec2 u_mouse; // mouse position in screen pixels
```

some of the math functions available to shader are :
sin cos tan pow exp log min max mod floor clamp sqrt abs floor ceil
etc.

* gl_FragCoord

gl_FragCoord holds screen coordinates of the pixel being worked on 
in the curren tthread.

Also since it is not same for all threads it is "varying"




