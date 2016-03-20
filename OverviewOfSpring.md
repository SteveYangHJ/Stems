# Part I. Overview of Spring Framework

The Spring Framework is a lightweight solution and a potential one-stop-shop for building your enterprise-ready applications. However, Spring is modular, allowing you to use only those parts that you need, without having to bring in the rest. You can use the IoC container, with Struts on top, but you can also use only the Hibernate integration code or the JDBC abstraction layer. The Spring Framework supports declarative transaction management, remote access to your logic through RMI or web services, and various options for persisting your data. It offers a full-featured MVC framework, and enables you to integrate AOP transparently into your software.
[Spring框架是一个轻量级的，一个潜在的一站式构建企业级应用的解决方案。但是，Spring也是模块化的，允许你只使用那些你需要的模块，而不必引入其余的模块。你可以使用IoC容器，在其之上使用Struts，你也可以只使用Hibernate集成代码或者JDBC抽象层。Spring框架支持声明式事务管理，通过RMI或Web Service远程访问你的逻辑，和多种选项来持久化你的数据。它提供了一个功能齐全的MVC框架，并允许你将AOP透明地集成到你的软件。]

Spring is designed to be non-intrusive, meaning that your domain logic code generally has no dependencies on the framework itself. In your integration layer (such as the data access layer), some dependencies on the data access technology and the Spring libraries will exist. However, it should be easy to isolate these dependencies from the rest of your code base.
[Spring被设计为非侵入式的，这意味着通常你的领域逻辑代码不会依赖于框架本身。在集成层（比如数据访问层），会存在一些对数据访问技术和Spring Libraries的依赖。但是，从你的代码库中其他部分隔离这些依赖是比较容易的。]

This document is a reference guide to Spring Framework features. If you have any requests, comments, or questions on this document, please post them on the user mailing list or on the support forums at http://forum.springsource.org/.
【本文档是Spring框架功能的参考指南。如果你对本文档有其他任何请求，评论或问题，请将他们贴到用户邮件列表或Spring官网（http://forum.springsource.org/）的支持论坛。】

## Introduction to Spring Framework
