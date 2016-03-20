# Part I. Overview of Spring Framework
Spring框架是一个轻量级的，一个潜在的一站式构建企业级应用的解决方案。但是，Spring也是模块化的，允许你只使用那些你需要的模块，而不必引入其余的模块。你可以使用IoC容器，在其之上使用Struts，你也可以只使用Hibernate集成代码或者JDBC抽象层。Spring框架支持声明式事务管理，通过RMI或Web Service远程访问你的逻辑，和多种选项来持久化你的数据。它提供了一个功能齐全的MVC框架，并允许你将AOP透明地集成到你的软件。

Spring被设计为非侵入式的，这意味着通常你的领域逻辑代码不会依赖于框架本身。在集成层（比如数据访问层），会存在一些对数据访问技术和Spring Libraries的依赖。但是，从你的代码库中其他部分隔离这些依赖是比较容易的。

本文档是Spring框架功能的参考指南。如果你对本文档有其他任何请求，评论或问题，请将他们贴到用户邮件列表或[Spring官网](http://forum.springsource.org/)的支持论坛

## 1.Introduction to Spring Framework
Spring框架是一个为开发Java应用提供了全面的基础设施支持的Java平台。Spring处理基础设施，这样你就可以只关注你的应用。
Springg允许你从“Plain old Java object”（POJOs）构建应用，并将企业级服务非侵入式地应用到POJOs。这一功能适用于所有的Java SE和部分的Java EE编程模型。
以下示例展示了一个应用开发者如何使用Spring平台的优势：
* 使一个Java方法在数据库事务中执行，而不用处理事务APIs
* 将一个本地Java方法发布为远程过程调用，而不用处理Remote API
* 将一个本地Java方法发布为管理操作，而不用处理JMX API
* 将一个本地Java方法作为消息处理器，而不用处理JMS API

### 1.1 Dependency Injection and Inversion of Control - 依赖注入和控制反转
Java应用--一个松散的术语，从受约束的applets到N层服务端企业应用--通常由很多对象合作组成合适的应用程序。这样，对象就会在应用互相依赖。

尽管Java平台提供了丰富的应用开发功能，但它缺少将基本构建块组织为一个连贯整体的手段，而将这一任务留给了架构师和开发人员。是的，你可以使用设计模式，比如工厂模式、抽象工厂模式、构造器模式、装饰器模式，和服务定位器来将各种类和对象实例组成一个应用。然而，这些们模式是如此简单：给出最佳实践一个名字，并描述该模式做什么，在哪里应用它，它解决什么问题等等。模式是最佳实践的形式化，你必须在应用中自己实现。

Spring框架的IoC组件提供了一个将不同的组件组合为一个已经可用的完全工作的应用的正式的方法，解决了这一问题。Spring框架把形式化的设计模式编纂为一等对象(first-class objects)，你可以集成到你自己的应用。众多组织和机构以这种方式使用Spring框架，来设计健壮的、可维护的应用。

### 1.2 Modules - 模块
Spring框架的各种功能组织为大约20个模块。这些模块被分类为下图所示的几组：Core Container，Data Access/Integration，Web，AOP，Instrumentation和Test。
![Overview of the Spring Framework](http://docs.spring.io/spring/docs/3.2.16.RELEASE/spring-framework-reference/htmlsingle/images/spring-overview.png)

#### 1.2.1 Core Container - 核心容器
Core Container包含Core, Beans, Context和Expression Language模块。

Core和Beans模块提供了框架的基础部分，包括IoC和依赖注入功能。BeanFactory是工厂模式的一个精致的实现。它消除了程序化单例的必须性，允许你将配置和依赖规范从你的实际程序逻辑中解耦。

Context模块建立在由Core和Beans模块提供的坚实基础之上：它是一种以framework-style方式访问对象的手段，与JNDI注册表类似。Context模块从Beans模块继承了它的功能，并增加了对国际化（如使用Resource bundles）、事件传播、资源加载，以及透明化的创建上下文（例如被servlet容器）。Context模块还支持Java EE功能，比如：EJB、JMX、基本的远程处理。ApplicationContext接口是Context模块的焦点。

Expression Language表达式语言模块提供了一个强大的在运行时查询和操纵对象图的表达式语言。它是JSP2.1规范中定义的统一表达式语言（Unified EL）的一个扩展。这种语言支持：设置和获取属性值，属性分配（Property Assignement？？需求确认下），方法调用（method invocation），访问数组上下文（accessing the context of arrays），集合和索引器，逻辑和算术运算符，命名变量，根据对象名从Spring IoC容器检索对象。它也支持列表投影和选择（list projection and selection）以及常见的列表聚合（list aggregation）。

#### 1.2.2 Data Access/Integration




















