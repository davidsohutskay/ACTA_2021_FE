# AB_2021_FE
Wound healing finite element code.

Publication: 

**Mechanobiological Wound Model for Improved Design and Evaluation of Collagen Dermal Replacement Scaffolds 
David Sohutskay, Sherry Voytik-Harbin, Adrian Buganza Tepole**

The code has been designed to run on Purdue Research Computing Clusters. It may not work as-is in your system. Here are a few tips to troubleshoot compiling: 

* The code requires EIGEN linear algebra libraries, as well as BOOST libraries. It currently runs witn BOOST 1.75 and EIGEN 3.2.10
* The code has a parallel version with OPEN MP. The parallel parts of the code are primarily in solver.cpp and can be easily commented out if desired 
* Compilation is done with CMAKE

To compile the code: 
* Make sure EIGEN and BOOST files are downloaded in the folder in which the folder ACTA_2021_FE is located 
* Open terminal. Make sure you have Cmake installed (https://cmake.org/), as well as C++ compilers. We use intel compilers with support for openMP. 
* Create and go to the 'build' folder, i.e. a folder where the code will actually be compiled.
mkdir build 
cd build
* Run Cmake in the terminal to create the makefile: 
cmake ../ 
* This should create a makefile in the build directory. To actually compile the code type this in the terminal 
make 
* This should have created the executable 'woundcpp3D'. You can directly run in terminal by doing: 
./woundcpp3D  
* This would reproduce the simulation shown in Figure 5B of the paper. The file with the problem setup is in the 'src' folder and it is the 'results_circle_wound.cpp' file. We are currently working to provide a better interface to edit the problem setup in 'results_circle_wound.cpp' file. However, the code has been commented to guide edits to the code. Namely, the sections for model parameters, solver parameters, mesh reading, boundary conditions, have been commented more to guide users on how to edit the problem setup. 

Please get in touch in you have additional questions about using this code:
abuganza@purdue.edu
Adrian Buganza Tepole
Associate Professor, Purdue University 


