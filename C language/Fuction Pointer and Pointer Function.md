## 函数指针和指针函数  
## Function Pointer and Pointer Function
  
### 1.函数指针  
### 1.Function Pointer  
  
一个函数在编译后，会占据内存的一部分，它的函数的名字，就是这段函数的首地址。  
A function after compile, will take a part of memory where function's name is the head address of the memory.  
这就解释了为什么将函数的参数设置为标准为指针的形参，函数就能直接调用实参来改变数值。因为函数的名字本身就是一个指针，指向的是一个地址。  
It explained why we can set the parameters of function as pointer, then function can directly change the Arguments. Because the name of Function is a pointer  which points to a address where the function hold place in memory.  
  
格式：函数的返回类型 （\*指针变量名）（函数参数列表)  
Format: return type of function （\*The variable name of Pointer）（Fuction Parameter list)  

````
#include <stdio.h>
// A normal function with an int parameter
// and void return type
void fun(int a)
{
    printf("Value of a is %d\n", a);
}
  
int main()
{ 
    void (*fun_ptr)(int) = fun;  // & removed
  
    fun_ptr(10);  // * removed
  
    return 0;
}
````  
<br/>  
  
### 2.指针函数   
### 2.Pointer Function  

函数类型是函数的返回值是一个指针类型，故称为指针函数。  
The function after compile will return a value which is the type of Pointer, so we call it as Pointer Function  
  
类型：指针返回类型\* 指针变量名 (函数参数列表)  
Format: The type of the Pointer\* name of Pointer (parameters)  
eg: Int\* MAX(int x, int y);  
  
eg: char* strcat (char \*dest, const char\* src);  

That's enough, look out the difference between these two types I have mentioned.  
````
char *my_strcat(char *dest, const char *src)
{
	assert(dest != NULL);
	assert(src != NULL);
	char *ret = dest;
	while (*dest!='\0')                 //寻找到目标字符串的'\0'位置
	{
		dest++;
	}
	while (*dest++ = *src++);       //拷贝过程与strcpy相同
	return ret;
}  
````  
