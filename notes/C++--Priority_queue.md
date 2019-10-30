Priority_queue
======================
Priority_queue is a kind of container adapter in C++ STL. The other two container adapters are queue and stack.

Container adapter
----------------------
Container adapter is based on some sequential container in C++ STL to have special functions.
In default, queue and stack is based on deque, and priority_queue is based on vector.

Template
----------------------
template <typename T, typename Container=std::vector<T>, typename Compare=std::less<T>> class priority_queue

Initializing priority_queue
----------------------
Creating an empty queue:
priority_queue<T> queue_name;

Creating a queue and initializing it with an existing array:
vector<T> vector_T = {a,b,c};
priority_queue<T> queue_T = {vector_T.begin(), vector_T.end()}; 
priority_queue<T> queue_T_1 = {less<T>(), vector_T};//Less<T>() is default, if another comp function is required, all template type parameters need to be specified.
priority_queue<T, vector<T>, greater<T>> queue_T_2 = {greater<T>(), vector_T};
  
Copy from an existing priority_queue:
priority_queue<T> queue_T = {queue_existing}; //The bracket is not necessary
  
Operators
----------------------
queue_T.pop(): Remove the first element;
queue_T.push(): Add an element and sort automatically;
queue_T.empty(): Return true if empty;
queue_T.top(): Return the reference of the first element in the container;
queue_T.size(): Return the number of elements;

There are other operators.



  

