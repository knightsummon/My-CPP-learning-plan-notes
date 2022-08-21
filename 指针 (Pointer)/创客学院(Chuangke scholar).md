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
Rules:  
1.返回地址必须是全局变量的地址 2.返回地址必须是指针函数内局部static变量的地址 3.返回地址必须是字符串常量。
1.return addresses must be the address of arguments. 2. return address must be the local static parameter inside the Pointer function 3. return addresses could be the string constant.  

_______________________________________________________________________________________________________________________________________________________________________
  
**8.递归函数**  
**8.Recursive function**  
  
![8.1](https://github.com/knightsummon/My-CPP-learning-plan-notes/blob/main/photoes/86363077547690258.jpg)  
递归函数的调用分为两个阶段： 
  
Recursive Function when it got used, it can divided into two parts belows:  
1.递推阶段：从原问题出发，按照递归公式发展，最终达到递归终止条件。  
1.Recurrence:starting from question and following the recursive formula, finally, entering the destination of terminative condition.  
2.回归阶段：按照递归终止条件求出结果，逆向代入递归公式，最后回到原问题求解。  
2.Regression: Following the answer of destination, we put it to recursive formula that reversed, finally we wil track back to original question and get the final answer.  

_______________________________________________________________________________________________________________________________________________________________________    
**9.函数指针**  
**9.Function Pointer**  
<br/>  
![9.1](https://github.com/knightsummon/My-CPP-learning-plan-notes/blob/main/photoes/110918105011885124.jpg)  
函数指针是用来存放函数的地址，这个地址是一个函数的入口地址。  
Function Pointer is used to store addresses of Functions, which is a Function's entrance.  
函数的名代表了函数的入口地址。  
The name of Function represents the Entrance addresses of Function.  
```
函数的指针变量形式如下：  
The formula of Function Pointer as following:  
<数据结构> (\*<函数指针名称>) (<参数说明列表>);  
<Data type> (\*<the name of Function Pointer>) (<Parameters>);   
```
**实验  函数指针**  
Practice  
一、场景描述  
No1.Scenario  
用函数指针数组存放各种排序算法，通过指针去调用算法进行排序。  
We can use pointer to call algorithms, which are stored by Function Pointer array.  
在本程序中，一共定义了4种排序算法——选择排序、插入排序、希尔排序、归并排序。  
In this practice programmer, I define four sort algorithms---Select sort,insert sort, Shell sort, Merge_sort.  
定义了一个通用排序接口void sort(void (sortAlgorithm)(int,int),int \*array, int n) ，在主程序中由用户选择使用何种排序算法，调用sort方法，传入函数指针数组中对应的项，进行排序并且输出排序后的结果。  
I define a interface which can be used in programmer commenly, which names void sort(void (sortAlgorithm)(int,int),int \*array, int n), where in main function administer can use sort function to choose which algorithms to use. Give actual paramters to Function Pointer Array, and return back the results to main function.  
<br/>  
二、代码  
No.2 Code
```  
/*
 * 函数指针数组的应用————多种排序算法
 * 用函数指针数组存放各种排序算法，通过指针去调用算法进行排序
 */
#include <stdio.h>

//比较大小  
//Comparission  
int less(int v, int w) {
    if (v < w) {
        return 1;
    }
    else return 0;
}

//交换位置  
//Exchange  
void exch(int *array,int v, int w) {
    int tmp = array[v];
    array[v] = array[w];
    array[w] = tmp;
}

//打印数组  
//Traversal  
void show(int *array, int n) {
    for (int i = 0; i < n; ++i) {
        printf("%d ", array[i]);
    }
    printf("\n");
}

//选择排序  
SelectSort  
void selectSort(int *array, int n) {
    for (int i = 0; i < n; ++i) {
        int min = i;
        for (int j = i+1; j < n; ++j) {
            if (less(array[j], array[min])) {
                min = j;
            }
        }
        exch(array, min, i);
    }
}

//插入排序  
//InsertSort  
void insertSort(int *array, int n) {
    for (int i = 0; i < n; ++i) {
        for (int j = i; j > 0 && less(array[j], array[j - 1]); --j) {
            exch(array, j, j - 1);
        }
    }
}

//希尔排序
//Shell sort
void shellSort(int *array, int n) {
    int h = 1;
    while (h < n / 3) {
        h = 3 * h + 1;
    }
    while (h >= 1) {
        for (int i = h; i < n; ++i) {
            for (int j = i; j >= h && less(array[j], array[j - h]); j -= h) {
                exch(array, j, j - h);
            }
        }
        h = h/3;
    }
}

//归并排序  
//Merge_Sort  
void merge(int *array,int lo,int mid,int hi, int *aux) {
    int i = lo, j = mid + 1;
    for (int k = lo; k <= hi; ++k) {
        aux[k] = array[k];
    }
    for (int l = lo; l <= hi; ++l) {
        if (i > mid) array[l] = aux[j++];
        else if (j > hi) array[l] = aux[i++];
        else if (less(aux[i],aux[j])) array[l] = aux[i++];
        else array[l] = aux[j++];
    }
}

void mergeSortRecursive(int *array,int lo,int hi, int *aux) {
    if (hi <= lo) return;
    int mid = lo + (hi - lo) / 2;
    mergeSortRecursive(array, lo, mid, aux);
    mergeSortRecursive(array, mid + 1, hi, aux);
    merge(array, lo, mid, hi, aux);
}

void mergeSort(int *array, int n) {
    int aux[n];
    mergeSortRecursive(array, 0, n - 1, aux);
}

//通用排序接口，传入的是函数指针，具体视传入的是哪个排序算法而定
void sort(void (*sortAlgorithm)(int*,int),int *array, int n) {
    sortAlgorithm(array, n);
    show(array,n);
}



int main(int argc, char *args[]) {
    int count = 0;
    //函数指针数组，存放各种排序算法
    void (*sortAlgorithm[])(int*,int) = {selectSort,insertSort,shellSort,mergeSort};

    printf("这是一个简单的应用函数指针数组的例子————多种排序算法\n");
    printf("Choosing multiple Sort Algorithms\n");
    printf("请输入整数的个数：");
    printf("Please input the numbers of integers\n");
    scanf("%d", &count);
    int array[count];
    printf("请输入你想排序的整数列：");
    printf("Please input the original array：");
    for (int i = 0; i < count; ++i) {
        scanf("%d", array + i);
    }
    printf("请选择排序方式：\n");
    printf("Choosing the Sort Algorithm：\n");
    printf("1----选择排序\n");
    printf("2----插入排序\n");
    printf("3----希尔排序\n");
    printf("4----归并排序\n");
    int choice;
    scanf("%d", &choice);
    printf("排序后的结果如下：");
    sort(sortAlgorithm[choice-1], array, count);

    return 0;
}  
```
<br/>  
三、程序优势  
No.3 The advantages of programmer  

在主程序中只要调用sort方法，就可以不需要编写switch语句就能实现调用不同排序算法的功能。  
通过将函数名赋值给函数指针，也就是使函数指针指向该入口地址。  
Give algorithm's name to Function Pointer, Making function poiner point at the address of chosed Algorithm Function.  

四、理解与收获   
No.4 Comprehend  
函数指针有两个用途：调用函数和做函数的参数。本程序主要是使用了它做函数参数的功能。通过传入不同的函数，就可以调用不同的排序算法。提供了调用的灵活性，简化结构，某种程序上也是实现了面向对象编程的多态性。   
Function Pointer has two use: call function and be the parameter of function. This programmer use Function Pointer as global parameter, giving it variable functions to call numerous Sort Algorithms, reflecting the flexible of programming. And somehow it also reflects the polymorphism of object oriented programming.  
而函数指针数组，就是一个包含多个函数指针的数组，这样可以将多个函数进行统一标识。这体现在菜单驱动系统中。例如本程序就是提示用户输入一个整数值来选择排序算法菜单中的一个选项。用户的选择可以做函数指针数组的下标，而数组中的指针可以用来调用函数。  
In my programmer, Function Pointer is an array which includes various Fuction Poiner, putting all functions's addresses in it. In my view, I see it as a menu, user can choose the subscript to select one of these Function Pointers to call needed Sort Algorithm.  
__________________________________________________________________________________________________________________________________
<br/>  
