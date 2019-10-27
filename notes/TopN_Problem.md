Manacher's algorithm
======================
This algorithm is a linear time complexity algorithm used to find the longest palindromic substring of a string.
This algorithm has two key points:
  1. Insert some specific character like '#' to seperate each character of the string, to transfer "two-char-core" to "one-char-core".
  2. Use the symmetricity of palindromic string to reduce the cost of calculating the length of the substring.
  
Explaination about point 2
-----------------------
  In this algorithm, we scan the string from left to right.
  
  For each character, we record the radius of the longest palindromic substring expanded from it in a vector R.
  
  In this scan process, we always record the right-most index reached by some substring, and the index of the core of this substring, as rm and c_rm. 
  
  Then, for the current index i, it is always at the right of the c_rm, we can try to find the symmetric location, i_sym, with respect to c_rm, and the radius of i_sym can help determine the radius of i.
  

Details
------------------------
  c_rm: the index of the char which reaches the right most location;
  rm: the right most location;
  l: the left boundary of the c_rm, l = 2\*c_rm - rm;
  R: the vector of the radius of each location;
  i: current location.


  First of all insert the '#';
  Scan the string sequentially;
  Record c_rm and rm;
  For each index, 


