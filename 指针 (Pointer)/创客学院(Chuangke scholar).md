**1.关于指针数组的使用**  
**1.The using of pointer in array**  
<br/>
<br/>
![1.1](https://github.com/knightsummon/My-CPP-learning-plan-notes/blob/main/2466453.jpg)  
```
Claim a pointer array  
double *pa[2],a[2][3];  
Putting the first address of a[0] and [1] to Pointer array pa[0] and pa[1]  

pa[0]=a[0];  //Equalling pa[0]=&a[0][0];
pa[1]=a[1];  //Equalling pa[1]=&a[1][0];
```  
<br/>
练习    
practice   
  
  
int a=1;
int *b=&a;

printf("%d/n",a);  \\1  
printf("%d/n",&a);  \\23145  
printf("%d/n",b);  \\23145  
printf("%d/n",*b);  \\1  

```
总结（Conclution)  
变量a 本质上代表一个存储单元。a本来代表两个值：存储单元的地址和储单元中的数据。  
Variable a is a storage unit, So a present two values: Address of storage unit and Data of storage unit.  
为了消除这种二义性，C语言规定a表示存储单元中的数据，&a表示存储单元的地址  
In order to eliminate anbiguity, C language specifies that a present the data of storage unit and Using &a to present the address of a  
a存储单元中的数据可以是一个普通数值，也可以是另一个存储单元的地址，比如：a = &b  
In a storage unit where can not only storage a data value, but also an address of another storage unit.  
指针本身也具有二义性  
Pointer also has ambiguity  
使用b表示指针的地址（指针指向哪里哪里就是它的地址),使用\*b来读取指针地址指向的值。
Using b present the address of pointer( Where pointer point, give pointer the same address),Using \*b to present what the data value of Pointer b(addresss)  
```
**1.2指针的使用**  

**1.2 Practice of Pointer**  

int \*p;  
  
|Pointer|描述 Describe| 
|:-:|:-:|  
|&p|取出指针自己在内存中的地址 output address of pointer itself in the memory |  
|p|指针指向的地址 address of Pointer that pointed to|  
|\*p|读取指针指向的地址所指向的数值 read the address of Pointer which pointed and give out the value through reading the address|  

<br/>
<br/>
  
 **2.指针和二维数组**  
 **2.Pointer and 2-D array**
 

<br/>  

![2.1](https://github.com/knightsummon/My-CPP-learning-plan-notes/blob/main/684255965171918649.jpg)  
  
 二维数组名代表数组的起始地址，数组名加1，是移动了一行元素，因此，二维数组名被称为行地址  
 2 2-Dimensional array's name present the beginning of the address.When the name of array plus one, the pointer jump through a whole rank and point to nextrank. So, the name of 2-D array alled address of rank.  
 
 <br/>  
   
 **3.字符指针和字符串**  
 **3.Character Pointer and String**  
 <br/>
 <br/>
 ![3.1](https://github.com/knightsummon/My-CPP-learning-plan-notes/blob/main/photoes/29306216951985340.jpg)  
   
 In C programming, when a character pointer point to a constant string, we can not use giving character pointer a new value to change the old character which pointed by character pointer.  
<br/>  
<br/>  
  
**4.二级指针**  
**4.Secondary Pointer**  
  
![4.1](https://github.com/knightsummon/My-CPP-learning-plan-notes/blob/main/photoes/399069905579327721.jpg)  
<br/>  
前面红色部分代表指针q指向的单元的数据类型和结构  
The red part which in front means the data type (int) and data structure (\*) which pointed by q  
后面蓝色部分代表q的数据结构(\*)   
The blue part which in near means the data structure of pointer q itself.  
<br/>  
<br/>  
  
**5.Void指针和Const修饰符**  
**5.Void Pointer and Const Modifiers**  
<br/>  
Void指针是一种不确定数据类型的指针变量，它可以通过强制类型转换让该变量指向任何数据类型的变量  
Void Pointer is a pointer variable which has no certified data type, it can be forced to become all data type which you want.  
数据结构：Void \*<指针变量名称>  
Data structure: Void \*<The name of Pointer>  
<br/>  
Const修饰符指针  
Const Modifiers Pointer  
const <数据类型> *<指针变量名>  
const <data type> *<the name of Pointer Variable>  
常量化指针的目标是限制通过指针改变其目标的值  
The aim of const pointer is to limit a way which using change address of pointer to change value of object.   
  
  
实践  
Practice

const int \*p;  
int \* const p;  
将const作为定冠词修饰后面的名词属性  
Using const as definite article to define later noun   
在int \*p前有一个const作为修饰的时候，作用于它整体，是的指针p只能指向一个地方。   
When use a const as a definite article in front of int \*p, make pointer p can only point to a one place.  
而在int \*const p 中，指针的地址被常量化无法改变，p因为前面有const修饰后面无法接受新的地址赋值。  

_______________________________________________________________________________________________________________________________________________________________________

**6.函数**  
**6.Function**  
<br/>  
![6.1](https://github.com/knightsummon/My-CPP-learning-plan-notes/blob/main/photoes/217551750491529628.jpg)  
函数名称 (<实际参数>)  
Function name (<argument>)  
实参就是在使用函数时候，调用函数传递给被调用函数的数据。需要实际确切的数字。  
Argument is when using function, outter function gives practicle data to this function.  
<br/>    
函数参数的传递 (实参和形参的使用）   
The passing of function parameters  
  
![6.2](https://github.com/knightsummon/My-CPP-learning-plan-notes/blob/main/photoes/716102449211848029.jpg)  
Using address to pass parameter  
1.按照地址传递，实参为变量的地址，而形参为同类型的指针。  
1.Using address to pass address, using address of Variable as arguments in function, meanwhile, Using Pointer as parameter in the same function.  
<br/>  
2.被调用函数中对形参的操作，将直接改变实参的值。  
2.The operating on parameter in funcuion will directly change the value of argument which uses the function.  
<br/>  
实例  
Practice
交换数值  
swap the values  
```
 #include <cstdio>
#include <cstdlib>
using namespace std;

void swap(int* x,int* y);

int main()
{
	int a = 10;
	int b = 20;
	swap(&a, &b);
	printf("%d  %d\n", a, b);
	return 0;
}

void swap(int* x, int* y)
{
	printf("%d  %d\n", x, y);
	int t;
	t = *x;
	*x = *y;
	*y = t;
	printf("%d  %d\n", *x, *y);
}
```
<br/>      
_______________________________________________________________________________________________________________________________________________________________________
  
**7.指针函数**  
**7.Pointer Function**  
<br/>  
指针函数是指一个函数的返回值是地址量的函数  
Pointer function which returns value is the address.  
![7.1](https://github.com/knightsummon/My-CPP-learning-plan-notes/blob/main/photoes/348262166088450666.jpg)  
指针函数的结构  
The common struct of Pointer Function  
``` 
<data type> * <name of function>(<parameters>)
	{
	sentences;
	return address;
	}
```
注意：如在main函数外调用指针函数，指针函数的返回值必须按照以下规定返回，不然cpu会销毁掉指针函数的返回地址。  
PS: If we use pointer function out of main, the return addresses of Pointer Functin must follow under rulers. Or CPU wil destory the return addresses of Pointer Function.  


  


 
 
 
