# c-code
An advance c++ code
Sign in

for Education
Home
Products
Google for Education
C++
C++ In Depth


C++ Language Tutorial
The early sections of this tutorial cover the basic material already presented in the last two modules, and provide more information on advanced concepts. Our focus in this module is on dynamic memory, and more details on objects and classes. Some advanced topics are also introduced, like inheritance, polymorphism, templates, exceptions and namespaces. We will study these later in the Advanced C++ course.

Object-Oriented Design
This is an excellent tutorial on object-oriented design. We will apply the methodology presented here in this module's project.

Learn by Example #3
Our focus in this module is on obtaining more practice with pointers, object-oriented design, multi-dimensional arrays, and classes/objects. Work through the following examples. We can't emphasize enough that the key to becoming a good programmer is practice, practice, practice!
Exercise #1: More Practice with Pointers
If you need additional practice with pointers, read through this resource which covers all aspects of pointers and provides many program examples.

What's the output of the following program? Please do not run the program, but draw the memory picture to determine the output.

void Unknown(int *p, int num);
void HardToFollow(int *p, int q, int *num);

void Unknown(int *p, int num) {
  int *q;

  q = &num;
  *p = *q + 2;
  num = 7;
}

void HardToFollow(int *p, int q, int *num) {
  *p = q + *num;
  *num = q;
  num = p;
  p = &q;
  Unknown(num, *p);
}

main() {
  int *q;
  int trouble[3];

  trouble[0] = 1;
  q = &trouble[1];
  *q = 2;
  trouble[2] = 3;

  HardToFollow(q, trouble[0], &trouble[2]);
  Unknown(&trouble[0], *q);

  cout << *q << " " << trouble[0] << " " << trouble[2];
}
