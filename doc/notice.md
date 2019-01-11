# Notice

## 语言性能

### 内存管理

- 手动
- gc

### 基础类型

## 开发效率

### 标准库

## 语法讨论

### 字符类型关键字命名规范

- Java 系的 String
- javascript、typescript 的 string

### 数据类型的表示方法

- go 中： 空格+关键字
- ts 中：`:`+ 关键子

### 静态方法与实例方法的语义化

- `.`操作符
- `::`操作符

### 函数定义规则及返回值类型

- function、func、fun、fn、()->

### 值类型、引用类型和指针

- 指针
- 值类型、引用类型

### 零值与空值

### 集合类型

- 数组
- 元组
- 切片

### 结构体与类

- 结构体更多出现在面向过程语言中，类更多出现在面向对象语言中，作用是否有重合的部分，如何分配职责。

rust 中的结构体与面向对象语言中的类十分相似

```rust
struct Rectangle {
    width: u32,
    height: u32,
}

impl Rectangle {
    // 结构体方法
    fn area(&self) -> u32 {
        self.width * self.height
    }
    fn can_hold(&self, other: &Rectangle) -> bool {
        self.width > other.width && self.height > other.height
    }

    // 关联函数
    fn square(size: u32) -> Rectangle {
        Rectangle { width: size, height: size }
    }
}
```

```typescript
class Rectangle {
  width: number;
  height: number;
  constructor(option: { width: number; height: number }) {
    this.width = option.width;
    this.height = option.height;
  }
  area(): number {
    return this.width * this.height;
  }
  can_hold(other: Rectangle): boolean {
    return this.width > other.width && this.height > other.height;
  }
  static square(size: number): Rectangle {
    return new Rectangle({
      width: size,
      height: size
    });
  }
}
```

### 简化写法

- 参数名与字段名都完全相同，使用字段初始化简写语法

```
{
    email,
    username,
    active: true,
}
```

### 模块化方案

- python
- java
- go
- rust
- typescript

### 内存管理

- rust 所有权
- GC 垃圾回收
- c 手动释放内存
