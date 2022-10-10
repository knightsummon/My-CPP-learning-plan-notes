##函数指针和指针函数  
##Function Pointer and Pointer Function  
  
###1.函数指针  
###1.Function Pointer   
  
一个函数在编译后，会占据内存的一部分，它的函数的名字，就是这段函数的首地址。  
A function after compile, will take a part of memory where function's name is the head address of the memory.  
这就解释了为什么将函数的参数设置为标准为指针的形参，函数就能直接调用实参来改变数值。因为函数的名字本身就是一个指针，指向的是一个地址。  
It explained why we can set the parameters of function as pointer, then function can directly change the Arguments. Because the name of Function is a pointer  
which points to a address where the function hold place in memory.  

  
