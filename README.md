1. just run make command to execute the makefile at the shell prompt.

2. Make sure you have installed OpenGl(glad) library. if not follow the instructions below. This is required to compile and link 
include/glad/src/glad.c

OpenGL Setup: Installing dependencies

Before installing the required libraries, we’ll first have to install a few dependencies. So open your terminal and run the following commands:

sudo apt-get update

sudo apt-get install cmake pkg-config 

sudo apt-get install mesa-utils libglu1-mesa-dev freeglut3-dev mesa-common-dev 

sudo apt-get install libglew-dev libglfw3-dev libglm-dev 

sudo apt-get install libao-dev libmpg123-dev 

sudo apt install libxcursor-dev 

sudo apt install libxinerama-dev 

sudo apt install libxkbcommon-dev 

sudo apt install libxi-dev 


Running the below commands would install GLFW in your system:

sudo cd /usr/local/lib/

sudo git clone https://github.com/glfw/glfw.git

sudo cd glfw

sudo cmake .

sudo make

sudo make install

##################################################################

Head on to the GLAD web service. Set the language to C++ and choose the specification as OpenGL. In the API section, select gl version of at least 3.3, make sure the profile is set to Core, and that the Generate a loader option is ticked.
Ignore the extensions and click Generate to produce the resulting library files. GLAD, by now, should have provided you a zip file: glad.zip containing two folders(include and src). Copy the folders inside include (glad and KHR) into your include(s) directory: cp -R include/* /usr/include/
    
Now copy the file glad.c inside the src folder to your current working directory.

