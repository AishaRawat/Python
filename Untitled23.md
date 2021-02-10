## Type hinting 


```python
def add(a,b=1):
    return a+b
```


```python
add(1)
```




    2




```python
add('a')
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-3-d8e687724821> in <module>
    ----> 1 add('a')
    

    <ipython-input-1-f53f0db65610> in add(a, b)
          1 def add(a,b=1):
    ----> 2     return a+b
    

    TypeError: can only concatenate str (not "int") to str



```python
def add(a: int ,b:int=1):
    return a+b
```


```python
help(add)
```

    Help on function add in module __main__:
    
    add(a: int, b: int = 1)
    
    

So , Basically the function is int was our hint 

If we want to specify also the return type of the function, we can use the following defintion


```python
def add(a: int ,b:int=1) ->int:
    return a+b
```


```python
help(add)
```

    Help on function add in module __main__:
    
    add(a: int, b: int = 1) -> int
    
    


```python

```

# Generic type functions 


```python
def list_sum(l:list):
    return sum(l)
```


```python
help(list_sum)
```

    Help on function list_sum in module __main__:
    
    list_sum(l: list)
    
    


```python
from typing import List 
```


```python
def list_sum(l:List[int]):
    return sum(l)
```


```python
help(list_sum)
```

    Help on function list_sum in module __main__:
    
    list_sum(l: List[int])
    
    


```python
from typing import Union 
```


```python
def divide(a:Union[int,float],b:Union[int , float ]):
    return a/b
```


```python
help(divide)
```

    Help on function divide in module __main__:
    
    divide(a: Union[int, float], b: Union[int, float])
    
    


```python
from typing import Any
```


```python
def anything(a):
    print(a)
```


```python
help(anything)
```

    Help on function anything in module __main__:
    
    anything(a)
    
    


```python
def add(a,b):
    return a+b
```


```python
add(1,2)
```




    3




```python
add("abc","def")
```




    'abcdef'




```python
add(1.0,3.0)
```




    4.0




```python

```
