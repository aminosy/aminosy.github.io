+++
date = '2026-09-20T16:50:50+08:00'
draft = false
title = 'Python_function_tutorial'
+++

#前面的知识不算难，而且我是在学到函数是才接触的博客，就不补前面的东西了

一、基础题（参数与返回值）
1. 两数之和
定义一个函数 add(a, b)，接收两个数，返回它们的和。加上类型注解。

2. 判断奇偶
定义 is_even(n: int) -> bool，判断一个整数是否为偶数。

3. 最大值
定义 max_of_three(a, b, c)，返回三个数中的最大值（不许用内置 max）。

4. 摄氏度转华氏度
定义 celsius_to_fahrenheit(c: float) -> float，公式：F = C * 9/5 + 32。

5. 字符串反转
定义 reverse_string(s: str) -> str，返回反转后的字符串（不许用切片 [::-1]，用循环实现）。

Ans:
1.
def add(a,b):
    result = a + b
    return result
a = int(input())
b = int(input())
print(add(a,b))

2.
def is_even(n:int) -> bool:
    if n % 2 == 0:
        return True
n = int(input())
if is_even(n):
    print('偶数')
else:
    print('奇数')

3.
def max_of_three(a,b,c):
    if a >= b and a >= c:
        return a
    elif b >= a and b >= c:
        return b
    elif c >= a and c >= b:
        return c
a = float(input())
b = float(input())
c = float(input())

print(max_of_three(a,b,c))

4.
def celsius_to_fahrenheit(c:float) ->float:
    f = c * 9 / 5 + 32
    return f

c = float(input('input c'))
print(celsius_to_fahrenheit(c))

5.
def reverse_string(s: str) -> str:
    return ''.join(reversed(s))

text = input('请输入字符串: ')
print(reverse_string(text))

