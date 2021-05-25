
## How to use freeglut, glew with OpenGL in your macOS with Visual Studio code.   

### 1. Install https://www.xquartz.org for window system.   

### 2. Construct .vscode like this repo.

### 3. Include glew and freeglut in your code.
~~~c++
// Include glew and freeglut like this
#include <GL/glew.h>
#ifdef __APPLE__
#   include <OpenGL/gl3.h>
#   include <GLUT/glut.h>
#endif

// ...

// When you init yout glut, import GLUT_3_2_CORE_PROFILE for using OpenGL 3.2 or later.
// glewExperimental = GL_TRUE is also needed for macOS. I don't know why.
// Just do below two lines when your application prepares OpenGL context.
    glutInitDisplayMode (/*...*/ | GLUT_3_2_CORE_PROFILE);
    glewExperimental = GL_TRUE;
~~~

### 3. Click Terminal in vscode --> Run Build Task to build your project.
