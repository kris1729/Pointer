# Pointer_Codder_army
```cpp
int a = 10;

```
in a memory at a place store 10 that place name is a and , a is nothing only a unique address like 500 . so that address memory store 10 number

# how to know the address of a is like 500
by the help of **symble table** , when we declear a variable ..


# 2GB , 4GB , 8GB RAM ...
In Memory 1,1,1 BYTE Blocks
if 4GB Ram than
4GB --> 2^32 BYTE --> for this we need total 2^32 unique address .. for this we need only 32 bit os system because , by the help of 32 bit we can create the 2 ^ 32 unique 


# How to print and store appress

```cpp
int a = 10;
//stroe address
int *ptr = &a;
// read value
cout<< ptr ;
// or 
cout<< &a ;

//
float  b = 12.3;
float *ptr1 = &b;
cout<< ptr1;

```
# Size of A pointer 
if ram is 4GB than size of a pointer will be 32 bit or 4Byte
if Ram is 8GB , 16GB ....... then address will be 64 bit or 8Byte

> it does not depend on (int , float , char , double) type

# Why write int , float , char before the ptr
bcz. when we read than .. if char then read only one block , if int than read 4 block alternate memory blocks

# how to read value of with the help of address pointer 

```cpp
int a = 10;
int *ptr = &a;
// access the value with the hepl of pointer
cout<<(*ptr);
```
> in a pointer we can store multiple address but at one time one address

```cpp
int a =10;
int *ptr = &a;

int b = 12;
// imp
ptr = &b;
cout<<(*ptr) ; // 12
b = 1000;
cout<<(*ptr) ; // 1000
```

# Pointer in arr
![](./01/first.png)

if int arr[5] ;
int *ptr = &arr[0];
or 
int * ptr = arr
than the address of each one is 
arr = arr[0]  --> x
arr+1 = arr[1] --> x+4
arr+2 = arr[2] --> x+2*4
arr+3 = arr[3]
arr+4 = arr[4]

# cout<< arr[i] ;
  at this case first go for the address of arr[3] which will
  **address --> arr + i * dataType size** 
  and than give the value which is store at this lucation


> arr[3] == *(arr+3) == *(3+arr)  == 3[arr]

or 
int *ptr = arr;

> > ptr[3] == *(ptr+3) == *(3+ptr) == 3[ptr]


arr = &arr[0]
    = & (*(arr+0))
    = arr  

# print all the address of arr
```cpp
int arr[5] = {1,2,3,4,5};
for(int i =0;i<5;i++)
cout<< (arr+i) << " same " << &arr[i]<<endl;
```

# print all tha value 

```cpp
int arr[5] = {1,2,3,4,5};
for(int i =0;i<5;i++)
cout<< arr[i] <<" or " << *(arr+i) << " or " << *(i+arr) << " or " << i[arr]<<endl;
```

# airthmetic operation of pointer

> print array 

```cpp
int arr[5] = {1,2,3,4,5};

int *ptr = arr;

for(int i =0;i<5;i++){
    cout<<*ptr<<" ";

    ptr++; // ptr = ptr + 1
}
// or 

int *ptr1 = &arr[4];
for(int i =0;i<5;i++){
    cout<<*ptr1<<" ";
    ptr1--; // ptr1 = ptr1 - 1;
}

```
ptr = ptr + 3 ✅
ptr1 = ptr1 - 2 ✅

# BUT BUT  it's worng
arr++ ❎
arr -- ❎
arr = arr + 3 ❎

> ❎❎❎❎❎❎❎❎worng❎❎❎❎
```cpp
int arr[5] = {1,2,3,4,5};
for(int i =0;i<5;i++)
{
    cout<<*arr;
    arr++;
}
```
bcz these pointer arr , arr+1 , arr+3 are constent
if it variable then data can be lost 





