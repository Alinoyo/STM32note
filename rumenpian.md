# 入门篇

## **自己写库——构建库函数模型**

### **构建库函数雏形（1）**

前面学的寄存器编程，是底层的东西。现在我们学固件库编程这节课<u>分析寄存器和固件库编程的优缺点问题</u>。

```c
//使用结构体来实现寄存器映射
typedef unsigned int unint32_t
typedef unsigned int unint16_t
typedef struct
{
    unint32_t CRL;
    unint32_t CRH;
    unint32_t IDR;
    unint32_t ODR;
    unint32_t BSRR;
    unint32_t BRR;
    unint32_t LCKR;
    
}GPIO_TypeDef;
#define GPIOB ((GPIO_TypeDef*)GPIO_BASE)
```

