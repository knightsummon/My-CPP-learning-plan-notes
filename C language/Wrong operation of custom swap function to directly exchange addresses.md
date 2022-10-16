## 自定义swap函数直接交换地址的错误操作  
## Wrong operation of custom swap function to directly exchange addresses  
  
自定义一个swap函数如下，最初的理解是只要将地址传进去了，两个形参之间交换地址后再读取数值就可以完成数值的交换。  
Costum a swap function by myself, at first I think only if I put addresses in parameters, and then after compile, these parameters will exchange addresses with each others.   
Finally, the exchange of Values will be done, because I already change the address for each parameter.  
````
void swapaddress(int *a, int *b) {
    int *temp;
    temp = a;
    a = b;
    b = temp;
}
***ERROR***
````
<br/>  
但是如下就可以将数值正常交换      
If we write as follow, the values can exchange each other.   
  
````
void swapvalue(int *a,int *b){
	int temp;
	temp = *a;
	*a=*b;
	*b=temp;
}
````
    
 <br/> 
同时值得注意的一点是，如下使用二级指针传递参数也可以交换函数的实参数值。  
But what also need we pay attention is that If we use secondary pointer to exchange Arguments in Function, the values can be changed.    
  
````
void swapSpoint(int **pa, int **pb) {
    int *temp;
    temp = *pa;
    *pa = *pb;
    *pb = temp;
}
````
  
## 结论如下   
## So it is conclusion:    
  
Swap函数中传递进去的地址任然是一个形参，它只是原有的实际地址的备份，以同样的名字地址存放在Swap函数占据的内存中。  
  
The address what we can see in the parameteres of Swap function is also a parameter, it is just a coppy from actual addresses(Argument), Using the same name in the memory which occupied by the Swap Function.    
  
这就是为什么Swap函数的实体里面任然要用\*的原因了。    
This is why we should use \* in Swap Function body to help ue complete the exchange of values.  

