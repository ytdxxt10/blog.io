---
layout: post
title: Object-C Math function&constants
date: 2016-02-15
categories: blog
tags: [iOS积累]
description: Object-C Math function&constants。

---


#Object-C Math function&constants


```
extern float ceilf(float);
extern double ceil(double);
extern long double ceill(long double);
 
extern float floorf(float);
extern double floor(double);
extern long double floorl(longdouble);
 
extern float roundf(float);
extern double round(double);
extern long double roundl(longdouble);

extern float powf(float, float);
extern double pow(double, double);
extern long double powl(long double, long double);

extern float sqrtf(float);
extern double sqrt(double);
extern long double sqrtl(long double);

extern float fmaxf(float, float);
extern double fmax(double, double);
extern long double fmaxl(long double, long double);

extern float fminf(float, float);
extern double fmin(double, double);
extern long double fminl(long double, long double);

extern float fabsf(float);
extern double fabs(double);
extern long double fabsl(long double);

```

+ ceil(x)返回不小于x的最小整数值
+ floor(x)返回不大于x的最大整数值
+ round(x)返回x的四舍五入整数值

- pow(x,n)返回x的n次幂
- sqrt(x) 返回x的平方根
- fmax(x,y)返回x,y中最大的数
- fmin(x,y)返回x,y中最小的数
- fabs(x)返回x的绝对值



#Constants

```
/*  Even though these might be more useful as long doubles, POSIX requires
    that they be double-precision literals.                                   */
#define M_E         2.71828182845904523536028747135266250   /* e              */
#define M_LOG2E     1.44269504088896340735992468100189214   /* log2(e)        */
#define M_LOG10E    0.434294481903251827651128918916605082  /* log10(e)       */
#define M_LN2       0.693147180559945309417232121458176568  /* loge(2)        */
#define M_LN10      2.30258509299404568401799145468436421   /* loge(10)       */
#define M_PI        3.14159265358979323846264338327950288   /* pi             */
#define M_PI_2      1.57079632679489661923132169163975144   /* pi/2           */
#define M_PI_4      0.785398163397448309615660845819875721  /* pi/4           */
#define M_1_PI      0.318309886183790671537767526745028724  /* 1/pi           */
#define M_2_PI      0.636619772367581343075535053490057448  /* 2/pi           */
#define M_2_SQRTPI  1.12837916709551257389615890312154517   /* 2/sqrt(pi)     */
#define M_SQRT2     1.41421356237309504880168872420969808   /* sqrt(2)        */
#define M_SQRT1_2   0.707106781186547524400844362104849039  /* 1/sqrt(2)      */

#define MAXFLOAT    0x1.fffffep+127f
```

