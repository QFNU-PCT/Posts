---
title: P1001 A+B Problem
date: 2025-10-27 16:00:59
tags: 讲义
---

> Link：[P1001 A+B Problem - 洛谷](https://www.luogu.com.cn/problem/P1001)

## 题目背景

**不熟悉算法竞赛的选手请看这里：**

算法竞赛中要求的输出格式中，**不能有多余的内容**，**这也包括了“请输入整数 $a$ 和 $b$” 这一类的提示用户输入信息的内容**。

例如以下 C 语言程序则输出了**多余信息**，**不能通过测试**：

```c
#include<stdio.h>
int main()
{
int a,b;
printf("输入两个正整数:\n");
scanf("%d %d",&a,&b);
printf("a + b = %d\n",a + b);
return 0;
}
```

正确的写法为：

```c
#include<stdio.h>
int main()
{
int a,b;
scanf("%d %d",&a,&b);
printf("%d\n",a + b);
return 0;
}
```

若包含了这些内容，将会被认为是 `Wrong Answer`，即洛谷上的 `WA`。在对比代码输出和标准输出时，系统将忽略每一行结尾的空格，以及最后一行之后多余的换行符。

若因此类问题出现本机似乎输出了正确的结果，但是实际提交结果为错误的现象，请勿认为是洛谷评测机出了问题，而是你的代码中可能存在多余的输出信息。用户可以参考在题目末尾提供的代码。

## 题目描述

输入两个整数 $a, b$，输出它们的和（$|a|,|b| \le {10}^9$）。

注意：

1. 要使用标准输入和标准输出来输出。那么，什么是标准输入和输出呢？

    - C 语言中的标准输入输出方法为 `scanf()` 和 `printf()`；
    - C++ 中的标准输入输出方法为 `cin` 和 `cout`，或者使用 `scanf()` 和 `printf()`；
    - Java 中的标准输入输出流为 `System.in` 和 `System.out`；
    - Python 中的标准输入输出方法为 `input()`和 `print()`；

2. Pascal 使用 `integer` 会爆掉哦！

3. 有负数哦！

4. C/C++ 的 main 函数必须是 `int` 类型。程序正常结束时的返回值必须是 0。这不仅对洛谷其他题目有效，而且也是 NOIP/CSP/NOI 比赛的要求！

5. Java 语言中无需 `package` ，类名必须为 `Main` ，不可修改。`main()` 函数中 `xxx.close();` 语句不可缺少。

6. 后台测试会忽略行末空格及换行。

7. 在算法竞赛或在线评测系统中，提交程序后系统会根据程序的编译、运行及输出情况返回不同的状态代码。以下是常见的评测结果含义：

    - **AC（Accepted）——通过**
        程序输出结果与标准答案**完全一致**。表示程序正确通过所有测试数据。AC 并不保证算法是最优的。
    - **CE（Compile Error）——编译错误**
        程序无法成功编译。通常是语法错误、缺少头文件、函数声明错误等。
    - **PC（Partially Correct）——部分正确**
        程序通过了部分测试数据，但仍有部分未通过。可能是边界情况、特殊输入或溢出问题导致。
    - **WA（Wrong Answer）——答案错误**
        程序输出结果与标准答案**不一致**。即使能通过样例输入，也可能因为隐藏测试数据未通过而判为 WA。
    - **RE（Runtime Error）——运行时错误**
        程序在运行过程中发生错误。常见原因：除以 0、数组越界、非法内存访问、栈溢出等。
    - **TLE（Time Limit Exceeded）——超时**
        程序运行时间超过题目规定的时间限制。可能是算法复杂度过高，或陷入死循环。
    - **MLE（Memory Limit Exceeded）——内存超限**
        程序运行时使用的内存超出限制。例如使用过大的数组或递归层数过深。
    - **OLE（Output Limit Exceeded）——输出超限**
        程序输出内容超出系统允许的最大长度。可能是死循环输出或调试信息未删除。
    - **UKE（Unknown Error）——未知错误**

好吧，同志们，我们就从这一题开始，向着大牛的路进发。

> 任何一个伟大的思想，都有一个微不足道的开始。

## 输入格式

两个以空格分开的整数。

## 输出格式

一个整数。

## 输入输出样例 #1

### 输入 #1

```
20 30
```

### 输出 #1

```
50
```

## **本题各种语言的程序范例：**

### C

```c
#include <stdio.h>

int main()
{
    int a,b;
    scanf("%d%d",&a,&b);
    printf("%d\n", a+b);
    return 0;
}
```
----------------

### C++

```cpp
#include <iostream>
#include <cstdio>

using namespace std;

int main()
{
    int a,b;
    cin >> a >> b;
    cout << a+b << endl;
    return 0;
}
```
----------------

### Pascal

```pascal
var a, b: longint;
begin
    readln(a,b);
    writeln(a+b);
end.
```
-----------------

### Python 3

```python
s = input().split()
print(int(s[0]) + int(s[1]))
```
-----------------

### Java

```java
import java.io.*;
import java.util.*;
public class Main {
    public static void main(String args[]) throws Exception {
        Scanner cin=new Scanner(System.in);
        int a = cin.nextInt(), b = cin.nextInt();
        System.out.println(a+b);
    }
}
```
-----------------

### JavaScript （Node.js）

```javascript
const fs = require('fs')
const data = fs.readFileSync('/dev/stdin')
const result = data.toString('ascii').trim().split(' ').map(x => parseInt(x)).reduce((a, b) => a + b, 0)
console.log(result)
process.exit() // 请注意必须在出口点处加入此行
```

-----------------

### Ruby

```ruby
a, b = gets.split.map(&:to_i)
print a+b
```

-----------------

### PHP

```php
<?php
$input = trim(file_get_contents("php://stdin"));
list($a, $b) = explode(' ', $input);
echo $a + $b;
```

-----------------

### Rust

```rust
use std::io;

fn main(){
    let mut input=String::new();
    io::stdin().read_line(&mut input).unwrap();
    let mut s=input.trim().split(' ');

    let a:i32=s.next().unwrap()
               .parse().unwrap();
    let b:i32=s.next().unwrap()
               .parse().unwrap();
    println!("{}",a+b);
}
```

-----------------

### Go

```go
package main

import "fmt"

func main() {
    var a, b int
    fmt.Scanf("%d%d", &a, &b)
    fmt.Println(a+b)
}
```

-----------------

### C# Mono

```cs
using System;

public class APlusB{
    private static void Main(){
        string[] input = Console.ReadLine().Split(' ');
        Console.WriteLine(int.Parse(input[0]) + int.Parse(input[1]));
    }
}
```

------------------

### Kotlin

```kotlin
fun main(args: Array<String>) {
    val (a, b) = readLine()!!.split(' ').map(String::toInt)
    println(a + b)
}
```

------------------

### Haskell

```haskell
main = do
    [a, b] <- (map read . words) `fmap` getLine
    print (a+b)
```

------------------

### Lua

```lua
a = io.read('*n')
b = io.read('*n')
print(a + b)
```

------------------

### OCaml

```ocaml
Scanf.scanf "%i %i\n" (fun a b -> print_int (a + b))
```

------------------

### Julia

```julia
nums = map(x -> parse(Int, x), split(readline(), " "))
println(nums[1] + nums[2])
```

------------------

### Scala

```scala
object Main {
  def main(args: Array[String]): Unit = {
    import java.util.Scanner
    
    val cin = new Scanner(System.in)
    val a = cin.nextInt()
    val b = cin.nextInt()
    System.out.println(a + b)
  }
}
```

------------------

### Perl

```perl
my $in = <STDIN>;
chomp $in;
$in = [split /[\s,]+/, $in];
my $c = $in->[0] + $in->[1];
print "$c\n";
```
