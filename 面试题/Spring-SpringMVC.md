# JAVA

标签：Spring/Spring MVC

----------

**Contents**

-  [Spring/Spring MVC](#Spring/SpringMVC)
    - [为什么要使用 spring？](#为什么要使用spring)
    - [解释一下什么是aop？](#解释一下什么是aop)
    - [解释一下什么是 ioc？](#解释一下什么是ioc)
    - [spring有哪些主要模块？](#spring有哪些主要模块)
    - [spring常用的注入方式有哪些？](#spring常用的注入方式有哪些)
    - [spring支持几种bean的作用域？](#spring支持几种bean的作用域)
    - [spring自动装配bean有哪些方式？](#spring自动装配bean有哪些方式)
    - [@RequestMapping的作用是什么？](#@RequestMapping的作用是什么)
    - [@Autowired的作用是什么？](@Autowired的作用是什么)
    - [关于跨域，以及跨域的几种方式](#关于跨域，以及跨域的几种方式)

----------
## 为什么要使用 spring？

## 解释一下什么是aop？

## 解释一下什么是 ioc？

## spring有哪些主要模块？

## spring常用的注入方式有哪些？

## spring支持几种bean的作用域？

当通过spring容器创建一个Bean实例时，不仅可以完成Bean实例的实例化，还可以为Bean指定特定的作用域。Spring支持如下5种作用域：

- singleton：单例模式，在整个Spring IoC容器中，使用singleton定义的Bean将只有一个实例

- prototype：原型模式，每次通过容器的getBean方法获取prototype定义的Bean时，都将产生一个新的Bean实例

- request：对于每次HTTP请求，使用request定义的Bean都将产生一个新实例，即每次HTTP请求将会产生不同的Bean实例。只有在Web应用中使用Spring时，该作用域才有效

- session：对于每次HTTP Session，使用session定义的Bean豆浆产生一个新实例。同样只有在Web应用中使用Spring时，该作用域才有效

- globalsession：每个全局的HTTP Session，使用session定义的Bean都将产生一个新实例。典型情况下，仅在使用portlet context的时候有效。同样只有在Web应用中使用Spring时，该作用域才有效


##@Autowired的作用是什么？

@Autowired是Spring提供的一种注入Bean的方法。

在Service类中定义的注入属性前加@Autowired。例如：@Autowired private PersonDAO personDAO,

## 关于跨域，以及跨域的几种方式

**跨域:**浏览器对于javascript的同源策略的限制,例如a.cn下面的js不能调用b.cn中的js,对象或数据(因为a.cn和b.cn是不同域),所以跨域就出现了.

**同域的概念：**简单的解释就是相同域名,端口相同,协议相同

**同源策略:**请求的url地址,必须与浏览器上的url地址处于同域上,也就是域名,端口,协议相同.































