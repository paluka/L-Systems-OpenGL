Erik Paluka. Winter 2012.

L-Systems

Implemented in C++ using OpenGL.

I first expand the L-system ‘n’ times (maximum depth of the tree) and save each expansion in a vector. I expand by iterating through the string starting at the beginning and replacing the letters with their production rules. I added randomness to the model by creating a pseudo random number between 0 and 1. The value of the random number dictates which production rule a letter gets replaced with.
When I draw the screen (display function), I first draw the ground (the plane that the tree is sitting in) using triangles. Depending on the current depth of the tree, I draw a specific L-system string that I expanded at the beginning. I draw the branch width (line width) based on the current branch depth. Each time a push matrix operation happens, I decrease the depth. Each time a pop matrix operation happens, I increase the depth. I draw the branches using lines. I draw the leaves using triangles.
Every 2 seconds, the current depth of the tree increases, which in turn grows the tree. Also, the length of the lines increase.

My tree is 3D. I did this by rotating in all three axis when a clockwise or counter-clockwise rotation occurs.
My tree blows in the wind by changing the angle of rotation for the branches by using a pseudo random number. The change in angle is dictated by the value of the random number.