参考文档的这部分覆盖了所有那些对Spring框架来说是绝对必须的技术。

其中居于首要地位的是Spring框架的IoC控制反转容器。其次就是Spring的面向切面的编程（AOP）技术。Spring框架有自己的AOP框架，概念上来讲，也很容易理解，其成功解决了Java企业级编程中的AOP需求中80%的热点。

Spring也提供了对AspectJ（当前功能上来讲最全面，当然在Java企业级领域也最成熟的AOP实现）的支持。

最后，Spring团队提倡采用测试驱动开发（TDD）的软件开发方法，所以Spring也包含了对集成测试的支持（同时包含了单元测试的最佳实践）。Spring团队发现，正确使用IoC容器的确简化了单元测试和集成测试（在其中类中的setter方法和恰当的构造器的存在使得在一个测试中联合单元和集成测试更容易，而不需要设置服务定位注册器和诸如此类的业务）。专门独立的测试章节希望能够说服你。

 - [Chapter 5, The IoC Container](5. The IoC Container.md)
 - [Chapter 6, Resources](6. Resources.md)
 - [Chapter 7, Validation,Data Binding, and Type Conversion](7. Validation, Data Binding, and Type Conversion.md)
 - [Chapter 8, Srping Expression Language(SpEL)](8. Spring Expression Language (SpEL).md)
 - [Chapter 9, Aspect Oriented Programming with Spring](9. Aspect Oriented Programming with Spring.md)
 - [Chapter 10, Spring AOP APIs](10. Spring AOP APIs.md)
 - [Chapter 11, Testing](11. Testing.md)
