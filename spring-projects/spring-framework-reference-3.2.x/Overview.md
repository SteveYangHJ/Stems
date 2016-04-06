# Spring3.2.16 Agenda

标签（空格分隔）： Spring3.2.16

---

# Spring-Framework Reference Documentation
[Reference]:http://docs.spring.io/spring/docs/3.2.16.RELEASE/spring-framework-reference/htmlsingle/

### **Authors**
Rod Johnson, Juergen Hoeller, Keith Donald, Colin Sampaleanu, Rob Harrop, Thomas Risberg, Alef Arendsen, Darren Davison, Dmitriy Kopylenko, Mark Pollack, Thierry Templier, Erwin Vervaet, Portia Tung, Ben Hale, Adrian Colyer, John Lewis, Costin Leau, Mark Fisher, Sam Brannen, Ramnivas Laddad, Arjen Poutsma, Chris Beams, Tareq Abedrabbo, Andy Clement, Dave Syer, Oliver Gierke, Rossen Stoyanchev, Phillip Webb

**3.2.16.RELEASE**
Copyright © 2004-2013
Copies of this document may be made for your own use and for distribution to others, provided that you do not charge any fee for such copies and further provided that each copy contains this Copyright Notice, whether distributed in print or electronically.
[本文档的副本可以供你自己使用或分发给他人，只要你对这些副本不收取任何费用，并且每一份副本都包含这个版权声明，无论这些副本是通过打印方式或者电子版本进行分发。]


**Table of Contents**

# I. Overview of Spring Framework

## 1. Introduction to Spring Framework
### 1.1. Dependency Injection and Inversion of Control
### 1.2. Modules
#### 1.2.1. Core Container
#### 1.2.2. Data Access/Integration
#### 1.2.3. Web
#### 1.2.4. AOP and Instrumentation
#### 1.2.5. Test

### 1.3. Usage scenarios
#### 1.3.1. Dependency Management and Naming Conventions
Spring Dependencies and Depending on Spring
Maven Dependency Management
Ivy Dependency Management

#### 1.3.2. Logging
Not Using Commons Logging
Using SLF4J
Using Log4J


# II. What's New in Spring 3

## 2. New Features and Enhancements in Spring Framework 3.0

### 2.1. Java 5
### 2.2. Improved documentation
### 2.3. New articles and tutorials
### 2.4. New module organization and build system
### 2.5. Overview of new features
#### 2.5.1. Core APIs updated for Java 5
#### 2.5.2. Spring Expression Language
#### 2.5.3. The Inversion of Control (IoC) container
Java based bean metadata
Defining bean metadata within components
#### 2.5.4. General purpose type conversion system and field formatting system
#### 2.5.5. The Data Tier
#### 2.5.6. The Web Tier
Comprehensive REST support
@MVC additions
#### 2.5.7. Declarative model validation
#### 2.5.8. Early support for Java EE 6
#### 2.5.9. Support for embedded databases

## 3. New Features and Enhancements in Spring Framework 3.1
### 3.1. Cache Abstraction
### 3.2. Bean Definition Profiles
### 3.3. Environment Abstraction
### 3.4. PropertySource Abstraction
### 3.5. Code equivalents for Spring's XML namespaces
### 3.6. Support for Hibernate 4.x
### 3.7. TestContext framework support for @Configuration classes and bean definition profiles
### 3.8. c: namespace for more concise constructor injection
### 3.9. Support for injection against non-standard JavaBeans setters
### 3.10. Support for Servlet 3 code-based configuration of Servlet Container
### 3.11. Support for Servlet 3 MultipartResolver
### 3.12. JPA EntityManagerFactory bootstrapping without persistence.xml
### 3.13. New HandlerMethod-based Support Classes For Annotated Controller Processing
### 3.14. "consumes" and "produces" conditions in @RequestMapping
### 3.15. Flash Attributes and RedirectAttributes
### 3.16. URI Template Variable Enhancements
### 3.17. @Valid On @RequestBody Controller Method Arguments
### 3.18. @RequestPart Annotation On Controller Method Arguments
### 3.19. UriComponentsBuilder and UriComponents

## 4. New Features and Enhancements in Spring Framework 3.2
### 4.1. Support for Servlet 3 based asynchronous request processing
### 4.2. Spring MVC Test framework
### 4.3. Content negotiation improvements
### 4.4. @ControllerAdvice annotation
### 4.5. Matrix variables
### 4.6. Abstract base class for code-based Servlet 3+ container initialization
### 4.7. ResponseEntityExceptionHandler class
### 4.8. Support for generic types in the RestTemplate and in @RequestBody arguments
### 4.9. Jackson JSON 2 and related improvements
### 4.10. Tiles 3
### 4.11. @RequestBody improvements
### 4.12. HTTP PATCH method
### 4.13. Excluded patterns in mapped interceptors
### 4.14. Using meta-annotations for injection points and for bean definition methods
### 4.15. Initial support for JCache 0.5
### 4.16. Support for @DateTimeFormat without Joda Time
### 4.17. Global date & time formatting
### 4.18. New Testing Features
### 4.19. Concurrency refinements across the framework
### 4.20. New Gradle-based build and move to GitHub
### 4.21. Refined Java SE 7 / OpenJDK 7 support

# III. Core Technologies
## 5. The IoC container
### 5.1. Introduction to the Spring IoC container and beans
### 5.2. Container overview
#### 5.2.1. Configuration metadata
#### 5.2.2. Instantiating a container
Composing XML-based configuration metadata
#### 5.2.3. Using the container
### 5.3. Bean overview
#### 5.3.1. Naming beans
Aliasing a bean outside the bean definition
#### 5.3.2. Instantiating beans
Instantiation with a constructor
Instantiation with a static factory method
Instantiation using an instance factory method
### 5.4. Dependencies
#### 5.4.1. Dependency injection
Constructor-based dependency injection
Setter-based dependency injection
Dependency resolution process
Examples of dependency injection
#### 5.4.2. Dependencies and configuration in detail
Straight values (primitives, Strings, and so on)
References to other beans (collaborators)
Inner beans
Collections
Null and empty string values
XML shortcut with the p-namespace
XML shortcut with the c-namespace
Compound property names
#### 5.4.3. Using depends-on
#### 5.4.4. Lazy-initialized beans
#### 5.4.5. Autowiring collaborators
Limitations and disadvantages of autowiring
Excluding a bean from autowiring
#### 5.4.6. Method injection
Lookup method injection
Arbitrary method replacement
### 5.5. Bean scopes
#### 5.5.1. The singleton scope
#### 5.5.2. The prototype scope
#### 5.5.3. Singleton beans with prototype-bean dependencies
#### 5.5.4. Request, session, and global session scopes
Initial web configuration
Request scope
Session scope
Global session scope
Scoped beans as dependencies
#### 5.5.5. Custom scopes
Creating a custom scope
Using a custom scope
### 5.6. Customizing the nature of a bean
#### 5.6.1. Lifecycle callbacks
Initialization callbacks
Destruction callbacks
Default initialization and destroy methods
Combining lifecycle mechanisms
Startup and shutdown callbacks
Shutting down the Spring IoC container gracefully in non-web applications
#### 5.6.2. ApplicationContextAware and BeanNameAware
#### 5.6.3. Other Aware interfaces
### 5.7. Bean definition inheritance
### 5.8. Container Extension Points
#### 5.8.1. Customizing beans using a BeanPostProcessor
Example: Hello World, BeanPostProcessor-style
Example: The RequiredAnnotationBeanPostProcessor
#### 5.8.2. Customizing configuration metadata with a BeanFactoryPostProcessor
Example: the PropertyPlaceholderConfigurer
Example: the PropertyOverrideConfigurer
#### 5.8.3. Customizing instantiation logic with a FactoryBean
### 5.9. Annotation-based container configuration
#### 5.9.1. @Required
#### 5.9.2. @Autowired
#### 5.9.3. Fine-tuning annotation-based autowiring with qualifiers
#### 5.9.4. CustomAutowireConfigurer
#### 5.9.5. @Resource
#### 5.9.6. @PostConstruct and @PreDestroy
### 5.10. Classpath scanning and managed components
#### 5.10.1. @Component and further stereotype annotations
#### 5.10.2. Automatically detecting classes and registering bean definitions
#### 5.10.3. Using filters to customize scanning
#### 5.10.4. Defining bean metadata within components
#### 5.10.5. Naming autodetected components
#### 5.10.6. Providing a scope for autodetected components
#### 5.10.7. Providing qualifier metadata with annotations
### 5.11. Using JSR 330 Standard Annotations
#### 5.11.1. Dependency Injection with @Inject and @Named
#### 5.11.2. @Named: a standard equivalent to the @Component annotation
#### 5.11.3. Limitations of the standard approach
### 5.12. Java-based container configuration
#### 5.12.1. Basic concepts: @Bean and @Configuration
#### 5.12.2. Instantiating the Spring container using AnnotationConfigApplicationContext
Simple construction
Building the container programmatically using register(Class<?>...)
Enabling component scanning with scan(String...)
Support for web applications with AnnotationConfigWebApplicationContext
#### 5.12.3. Using the @Bean annotation
Declaring a bean
Receiving lifecycle callbacks
Specifying bean scope
Customizing bean naming
Bean aliasing
#### 5.12.4. Using the @Configuration annotation
Injecting inter-bean dependencies
Lookup method injection
Further information about how Java-based configuration works internally
#### 5.12.5. Composing Java-based configurations
Using the @Import annotation
Combining Java and XML configuration
### 5.13. Registering a LoadTimeWeaver
### 5.14. Additional Capabilities of the ApplicationContext
#### 5.14.1. Internationalization using MessageSource
#### 5.14.2. Standard and Custom Events
#### 5.14.3. Convenient access to low-level resources
#### 5.14.4. Convenient ApplicationContext instantiation for web applications
#### 5.14.5. Deploying a Spring ApplicationContext as a J2EE RAR file
### 5.15. The BeanFactory
#### 5.15.1. BeanFactory or ApplicationContext?
#### 5.15.2. Glue code and the evil singleton

## 6. Resources
### 6.1. Introduction
### 6.2. The Resource interface
### 6.3. Built-in Resource implementations
#### 6.3.1. UrlResource
#### 6.3.2. ClassPathResource
#### 6.3.3. FileSystemResource
#### 6.3.4. ServletContextResource
#### 6.3.5. InputStreamResource
#### 6.3.6. ByteArrayResource
### 6.4. The ResourceLoader
### 6.5. The ResourceLoaderAware interface
### 6.6. Resources as dependencies
### 6.7. Application contexts and Resource paths
#### 6.7.1. Constructing application contexts
Constructing ClassPathXmlApplicationContext instances - shortcuts
#### 6.7.2. Wildcards in application context constructor resource paths
Ant-style Patterns
The classpath*: prefix
Other notes relating to wildcards
#### 6.7.3. FileSystemResource caveats

## 7. Validation, Data Binding, and Type Conversion
### 7.1. Introduction
### 7.2. Validation using Spring's Validator interface
### 7.3. Resolving codes to error messages
### 7.4. Bean manipulation and the BeanWrapper
#### 7.4.1. Setting and getting basic and nested properties
#### 7.4.2. Built-in PropertyEditor implementations
Registering additional custom PropertyEditors
### 7.5. Spring 3 Type Conversion
#### 7.5.1. Converter SPI
#### 7.5.2. ConverterFactory
#### 7.5.3. GenericConverter
ConditionalGenericConverter
#### 7.5.4. ConversionService API
#### 7.5.5. Configuring a ConversionService
#### 7.5.6. Using a ConversionService programmatically
### 7.6. Spring 3 Field Formatting
#### 7.6.1. Formatter SPI
#### 7.6.2. Annotation-driven Formatting
Format Annotation API
#### 7.6.3. FormatterRegistry SPI
#### 7.6.4. FormatterRegistrar SPI
#### 7.6.5. Configuring Formatting in Spring MVC
### 7.7. Configuring a global date & time format
### 7.8. Spring 3 Validation
#### 7.8.1. Overview of the JSR-303 Bean Validation API
#### 7.8.2. Configuring a Bean Validation Implementation
Injecting a Validator
Configuring Custom Constraints
Additional Configuration Options
#### 7.8.3. Configuring a DataBinder
#### 7.8.4. Spring MVC 3 Validation
Triggering @Controller Input Validation
Configuring a Validator for use by Spring MVC
Configuring a JSR-303 Validator for use by Spring MVC

## 8. Spring Expression Language (SpEL)
### 8.1. Introduction
### 8.2. Feature Overview
### 8.3. Expression Evaluation using Spring's Expression Interface
#### 8.3.1. The EvaluationContext interface
Type Conversion
### 8.4. Expression support for defining bean definitions
#### 8.4.1. XML based configuration
#### 8.4.2. Annotation-based configuration
### 8.5. Language Reference
#### 8.5.1. Literal expressions
#### 8.5.2. Properties, Arrays, Lists, Maps, Indexers
#### 8.5.3. Inline lists
#### 8.5.4. Array construction
#### 8.5.5. Methods
#### 8.5.6. Operators
Relational operators
Logical operators
Mathematical operators
#### 8.5.7. Assignment
#### 8.5.8. Types
#### 8.5.9. Constructors
#### 8.5.10. Variables
The #this and #root variables
#### 8.5.11. Functions
#### 8.5.12. Bean references
#### 8.5.13. Ternary Operator (If-Then-Else)
#### 8.5.14. The Elvis Operator
#### 8.5.15. Safe Navigation operator
#### 8.5.16. Collection Selection
#### 8.5.17. Collection Projection
#### 8.5.18. Expression templating
### 8.6. Classes used in the examples

## 9. Aspect Oriented Programming with Spring
### 9.1. Introduction
#### 9.1.1. AOP concepts
#### 9.1.2. Spring AOP capabilities and goals
#### 9.1.3. AOP Proxies
### 9.2. @AspectJ support
#### 9.2.1. Enabling @AspectJ Support
Enabling @AspectJ Support with Java configuration
Enabling @AspectJ Support with XML configuration
#### 9.2.2. Declaring an aspect
#### 9.2.3. Declaring a pointcut
Supported Pointcut Designators
Combining pointcut expressions
Sharing common pointcut definitions
Examples
Writing good pointcuts
#### 9.2.4. Declaring advice
Before advice
After returning advice
After throwing advice
After (finally) advice
Around advice
Advice parameters
Advice ordering
#### 9.2.5. Introductions
#### 9.2.6. Aspect instantiation models
#### 9.2.7. Example
### 9.3. Schema-based AOP support
#### 9.3.1. Declaring an aspect
#### 9.3.2. Declaring a pointcut
#### 9.3.3. Declaring advice
Before advice
After returning advice
After throwing advice
After (finally) advice
Around advice
Advice parameters
Advice ordering
#### 9.3.4. Introductions
#### 9.3.5. Aspect instantiation models
#### 9.3.6. Advisors
#### 9.3.7. Example
### 9.4. Choosing which AOP declaration style to use
#### 9.4.1. Spring AOP or full AspectJ?
#### 9.4.2. @AspectJ or XML for Spring AOP?
### 9.5. Mixing aspect types
### 9.6. Proxying mechanisms
#### 9.6.1. Understanding AOP proxies
### 9.7. Programmatic creation of @AspectJ Proxies
### 9.8. Using AspectJ with Spring applications
#### 9.8.1. Using AspectJ to dependency inject domain objects with Spring
Unit testing @Configurable objects
Working with multiple application contexts
#### 9.8.2. Other Spring aspects for AspectJ
#### 9.8.3. Configuring AspectJ aspects using Spring IoC
#### 9.8.4. Load-time weaving with AspectJ in the Spring Framework
A first example
Aspects
'META-INF/aop.xml'
Required libraries (JARS)
Spring configuration
Environment-specific configuration
### 9.9. Further Resources

## 10. Spring AOP APIs
### 10.1. Introduction
### 10.2. Pointcut API in Spring
#### 10.2.1. Concepts
#### 10.2.2. Operations on pointcuts
#### 10.2.3. AspectJ expression pointcuts
#### 10.2.4. Convenience pointcut implementations
Static pointcuts
Dynamic pointcuts
#### 10.2.5. Pointcut superclasses
#### 10.2.6. Custom pointcuts
### 10.3. Advice API in Spring
#### 10.3.1. Advice lifecycles
#### 10.3.2. Advice types in Spring
Interception around advice
Before advice
Throws advice
After Returning advice
Introduction advice
### 10.4. Advisor API in Spring
### 10.5. Using the ProxyFactoryBean to create AOP proxies
#### 10.5.1. Basics
#### 10.5.2. JavaBean properties
#### 10.5.3. JDK- and CGLIB-based proxies
#### 10.5.4. Proxying interfaces
#### 10.5.5. Proxying classes
#### 10.5.6. Using 'global' advisors
### 10.6. Concise proxy definitions
### 10.7. Creating AOP proxies programmatically with the ProxyFactory
### 10.8. Manipulating advised objects
### 10.9. Using the "auto-proxy" facility
#### 10.9.1. Autoproxy bean definitions
BeanNameAutoProxyCreator
DefaultAdvisorAutoProxyCreator
AbstractAdvisorAutoProxyCreator
#### 10.9.2. Using metadata-driven auto-proxying
### 10.10. Using TargetSources
#### 10.10.1. Hot swappable target sources
#### 10.10.2. Pooling target sources
#### 10.10.3. Prototype target sources
#### 10.10.4. ThreadLocal target sources
### 10.11. Defining new Advice types
### 10.12. Further resources

## 11. Testing
### 11.1. Introduction to Spring Testing
### 11.2. Unit Testing
#### 11.2.1. Mock Objects
Environment
JNDI
Servlet API
Portlet API
#### 11.2.2. Unit Testing support Classes
General utilities
Spring MVC
### 11.3. Integration Testing
#### 11.3.1. Overview
#### 11.3.2. Goals of Integration Testing
Context management and caching
Dependency Injection of test fixtures
Transaction management
Support classes for integration testing
#### 11.3.3. JDBC Testing Support
#### 11.3.4. Annotations
Spring Testing Annotations
Standard Annotation Support
Spring JUnit Testing Annotations
#### 11.3.5. Spring TestContext Framework
Key abstractions
Context management
Dependency injection of test fixtures
Testing request and session scoped beans
Transaction management
TestContext Framework support classes
#### 11.3.6. Spring MVC Test Framework
Server-Side Tests
Client-Side REST Tests
#### 11.3.7. PetClinic Example
### 11.4. Further Resources

# IV. Data Access
## 12. Transaction Management
### 12.1. Introduction to Spring Framework transaction management
### 12.2. Advantages of the Spring Framework's transaction support model
#### 12.2.1. Global transactions
#### 12.2.2. Local transactions
#### 12.2.3. Spring Framework's consistent programming model
### 12.3. Understanding the Spring Framework transaction abstraction
### 12.4. Synchronizing resources with transactions
#### 12.4.1. High-level synchronization approach
#### 12.4.2. Low-level synchronization approach
#### 12.4.3. TransactionAwareDataSourceProxy
### 12.5. Declarative transaction management
#### 12.5.1. Understanding the Spring Framework's declarative transaction implementation
#### 12.5.2. Example of declarative transaction implementation
#### 12.5.3. Rolling back a declarative transaction
#### 12.5.4. Configuring different transactional semantics for different beans
#### 12.5.5. <tx:advice/> settings
#### 12.5.6. Using @Transactional
@Transactional settings
Multiple Transaction Managers with @Transactional
Custom shortcut annotations
#### 12.5.7. Transaction propagation
Required
RequiresNew
Nested
#### 12.5.8. Advising transactional operations
#### 12.5.9. Using @Transactional with AspectJ
### 12.6. Programmatic transaction management
#### 12.6.1. Using the TransactionTemplate
Specifying transaction settings
#### 12.6.2. Using the PlatformTransactionManager
### 12.7. Choosing between programmatic and declarative transaction management
### 12.8. Application server-specific integration
#### 12.8.1. IBM WebSphere
#### 12.8.2. BEA WebLogic Server
#### 12.8.3. Oracle OC4J
### 12.9. Solutions to common problems
#### 12.9.1. Use of the wrong transaction manager for a specific DataSource
### 12.10. Further Resources

## 13. DAO support
### 13.1. Introduction
#### 13.2. Consistent exception hierarchy
#### 13.3. Annotations used for configuring DAO or Repository classes
## 14. Data access with JDBC
### 14.1. Introduction to Spring Framework JDBC
#### 14.1.1. Choosing an approach for JDBC database access
#### 14.1.2. Package hierarchy
### 14.2. Using the JDBC core classes to control basic JDBC processing and error handling
#### 14.2.1. JdbcTemplate
Examples of JdbcTemplate class usage
JdbcTemplate best practices
#### 14.2.2. NamedParameterJdbcTemplate
#### 14.2.3. SQLExceptionTranslator
#### 14.2.4. Executing statements
#### 14.2.5. Running queries
#### 14.2.6. Updating the database
#### 14.2.7. Retrieving auto-generated keys
### 14.3. Controlling database connections
#### 14.3.1. DataSource
#### 14.3.2. DataSourceUtils
#### 14.3.3. SmartDataSource
#### 14.3.4. AbstractDataSource
#### 14.3.5. SingleConnectionDataSource
#### 14.3.6. DriverManagerDataSource
#### 14.3.7. TransactionAwareDataSourceProxy
#### 14.3.8. DataSourceTransactionManager
#### 14.3.9. NativeJdbcExtractor
### 14.4. JDBC batch operations
#### 14.4.1. Basic batch operations with the JdbcTemplate
#### 14.4.2. Batch operations with a List of objects
#### 14.4.3. Batch operations with multiple batches
### 14.5. Simplifying JDBC operations with the SimpleJdbc classes
#### 14.5.1. Inserting data using SimpleJdbcInsert
#### 14.5.2. Retrieving auto-generated keys using SimpleJdbcInsert
#### 14.5.3. Specifying columns for a SimpleJdbcInsert
#### 14.5.4. Using SqlParameterSource to provide parameter values
#### 14.5.5. Calling a stored procedure with SimpleJdbcCall
#### 14.5.6. Explicitly declaring parameters to use for a SimpleJdbcCall
#### 14.5.7. How to define SqlParameters
#### 14.5.8. Calling a stored function using SimpleJdbcCall
#### 14.5.9. Returning ResultSet/REF Cursor from a SimpleJdbcCall
### 14.6. Modeling JDBC operations as Java objects
#### 14.6.1. SqlQuery
#### 14.6.2. MappingSqlQuery
#### 14.6.3. SqlUpdate
#### 14.6.4. StoredProcedure
### 14.7. Common problems with parameter and data value handling
#### 14.7.1. Providing SQL type information for parameters
#### 14.7.2. Handling BLOB and CLOB objects
#### 14.7.3. Passing in lists of values for IN clause
#### 14.7.4. Handling complex types for stored procedure calls
### 14.8. Embedded database support
#### 14.8.1. Why use an embedded database?
#### 14.8.2. Creating an embedded database instance using Spring XML
#### 14.8.3. Creating an embedded database instance programmatically
#### 14.8.4. Extending the embedded database support
#### 14.8.5. Using HSQL
#### 14.8.6. Using H2
#### 14.8.7. Using Derby
#### 14.8.8. Testing data access logic with an embedded database
### 14.9. Initializing a DataSource
#### 14.9.1. Initializing a database instance using Spring XML
Initialization of Other Components that Depend on the Database

## 15. Object Relational Mapping (ORM) Data Access
### 15.1. Introduction to ORM with Spring
### 15.2. General ORM integration considerations
#### 15.2.1. Resource and transaction management
#### 15.2.2. Exception translation
### 15.3. Hibernate
#### 15.3.1. SessionFactory setup in a Spring container
#### 15.3.2. Implementing DAOs based on plain Hibernate 3 API
#### 15.3.3. Declarative transaction demarcation
#### 15.3.4. Programmatic transaction demarcation
#### 15.3.5. Transaction management strategies
#### 15.3.6. Comparing container-managed and locally defined resources
#### 15.3.7. Spurious application server warnings with Hibernate
### 15.4. JDO
#### 15.4.1. PersistenceManagerFactory setup
#### 15.4.2. Implementing DAOs based on the plain JDO API
#### 15.4.3. Transaction management
#### 15.4.4. JdoDialect
### 15.5. JPA
#### 15.5.1. Three options for JPA setup in a Spring environment
LocalEntityManagerFactoryBean
Obtaining an EntityManagerFactory from JNDI
LocalContainerEntityManagerFactoryBean
Dealing with multiple persistence units
#### 15.5.2. Implementing DAOs based on plain JPA
#### 15.5.3. Transaction Management
#### 15.5.4. JpaDialect
### 15.6. iBATIS SQL Maps
#### 15.6.1. Setting up the SqlMapClient
#### 15.6.2. Using SqlMapClientTemplate and SqlMapClientDaoSupport
#### 15.6.3. Implementing DAOs based on plain iBATIS API

## 16. Marshalling XML using O/X Mappers
### 16.1. Introduction
### 16.2. Marshaller and Unmarshaller
#### 16.2.1. Marshaller
#### 16.2.2. Unmarshaller
#### 16.2.3. XmlMappingException
### 16.3. Using Marshaller and Unmarshaller
### 16.4. XML Schema-based Configuration
### 16.5. JAXB
#### 16.5.1. Jaxb2Marshaller
XML Schema-based Configuration
### 16.6. Castor
#### 16.6.1. CastorMarshaller
#### 16.6.2. Mapping
XML Schema-based Configuration
### 16.7. XMLBeans
#### 16.7.1. XmlBeansMarshaller
XML Schema-based Configuration
### 16.8. JiBX
#### 16.8.1. JibxMarshaller
XML Schema-based Configuration
### 16.9. XStream
#### 16.9.1. XStreamMarshaller

#V. The Web
## 17. Web MVC framework
17.1. Introduction to Spring Web MVC framework
17.1.1. Features of Spring Web MVC
17.1.2. Pluggability of other MVC implementations
17.2. The DispatcherServlet
17.2.1. Special Bean Types In the WebApplicationContext
17.2.2. Default DispatcherServlet Configuration
17.2.3. DispatcherServlet Processing Sequence
17.3. Implementing Controllers
17.3.1. Defining a controller with @Controller
17.3.2. Mapping Requests With @RequestMapping
New Support Classes for @RequestMapping methods in Spring MVC 3.1
URI Template Patterns
URI Template Patterns with Regular Expressions
Path Patterns
Patterns with Placeholders
Matrix Variables
Consumable Media Types
Producible Media Types
Request Parameters and Header Values
17.3.3. Defining @RequestMapping handler methods
Supported method argument types
Supported method return types
Binding request parameters to method parameters with @RequestParam
Mapping the request body with the @RequestBody annotation
Mapping the response body with the @ResponseBody annotation
Using HttpEntity<?>
Using @ModelAttribute on a method
Using @ModelAttribute on a method argument
Using @SessionAttributes to store model attributes in the HTTP session between requests
Specifying redirect and flash attributes
Working with "application/x-www-form-urlencoded" data
Mapping cookie values with the @CookieValue annotation
Mapping request header attributes with the @RequestHeader annotation
Method Parameters And Type Conversion
Customizing WebDataBinder initialization
Support for the 'Last-Modified' Response Header To Facilitate Content Caching
17.3.4. Asynchronous Request Processing
Exception Handling for Async Requests
Intercepting Async Requests
Configuration for Async Request Processing
17.3.5. Testing Controllers
17.4. Handler mappings
17.4.1. Intercepting requests with a HandlerInterceptor
17.5. Resolving views
17.5.1. Resolving views with the ViewResolver interface
17.5.2. Chaining ViewResolvers
17.5.3. Redirecting to views
RedirectView
The redirect: prefix
The forward: prefix
17.5.4. ContentNegotiatingViewResolver
17.6. Using flash attributes
17.7. Building URIs
17.8. Using locales
17.8.1. AcceptHeaderLocaleResolver
17.8.2. CookieLocaleResolver
17.8.3. SessionLocaleResolver
17.8.4. LocaleChangeInterceptor
17.9. Using themes
17.9.1. Overview of themes
17.9.2. Defining themes
17.9.3. Theme resolvers
17.10. Spring's multipart (file upload) support
17.10.1. Introduction
17.10.2. Using a MultipartResolver with Commons FileUpload
17.10.3. Using a MultipartResolver with Servlet 3.0
17.10.4. Handling a file upload in a form
17.10.5. Handling a file upload request from programmatic clients
17.11. Handling exceptions
17.11.1. HandlerExceptionResolver
17.11.2. @ExceptionHandler
17.11.3. Handling Standard Spring MVC Exceptions
17.11.4. Annotating Business Exceptions With @ResponseStatus
17.11.5. Customizing the Default Servlet Container Error Page
17.12. Convention over configuration support
17.12.1. The Controller ControllerClassNameHandlerMapping
17.12.2. The Model ModelMap (ModelAndView)
17.12.3. The View - RequestToViewNameTranslator
17.13. ETag support
17.14. Code-based Servlet container initialization
17.15. Configuring Spring MVC
17.15.1. Enabling the MVC Java Config or the MVC XML Namespace
17.15.2. Customizing the Provided Configuration
17.15.3. Configuring Interceptors
17.15.4. Configuring Content Negotiation
17.15.5. Configuring View Controllers
17.15.6. Configuring Serving of Resources
17.15.7. mvc:default-servlet-handler
17.15.8. More Spring Web MVC Resources
17.15.9. Advanced Customizations with MVC Java Config
17.15.10. Advanced Customizations with the MVC Namespace
18. View technologies
18.1. Introduction
18.2. JSP & JSTL
18.2.1. View resolvers
18.2.2. 'Plain-old' JSPs versus JSTL
18.2.3. Additional tags facilitating development
18.2.4. Using Spring's form tag library
Configuration
The form tag
The input tag
The checkbox tag
The checkboxes tag
The radiobutton tag
The radiobuttons tag
The password tag
The select tag
The option tag
The options tag
The textarea tag
The hidden tag
The errors tag
HTTP Method Conversion
HTML5 Tags
18.3. Tiles
18.3.1. Dependencies
18.3.2. How to integrate Tiles
UrlBasedViewResolver
ResourceBundleViewResolver
SimpleSpringPreparerFactory and SpringBeanPreparerFactory
18.4. Velocity & FreeMarker
18.4.1. Dependencies
18.4.2. Context configuration
18.4.3. Creating templates
18.4.4. Advanced configuration
velocity.properties
FreeMarker
18.4.5. Bind support and form handling
The bind macros
Simple binding
Form input generation macros
HTML escaping and XHTML compliance
18.5. XSLT
18.5.1. My First Words
Bean definitions
Standard MVC controller code
Convert the model data to XML
Defining the view properties
Document transformation
18.5.2. Summary
18.6. Document views (PDF/Excel)
18.6.1. Introduction
18.6.2. Configuration and setup
Document view definitions
Controller code
Subclassing for Excel views
Subclassing for PDF views
18.7. JasperReports
18.7.1. Dependencies
18.7.2. Configuration
Configuring the ViewResolver
Configuring the Views
About Report Files
Using JasperReportsMultiFormatView
18.7.3. Populating the ModelAndView
18.7.4. Working with Sub-Reports
Configuring Sub-Report Files
Configuring Sub-Report Data Sources
18.7.5. Configuring Exporter Parameters
18.8. Feed Views
18.9. XML Marshalling View
18.10. JSON Mapping View
19. Integrating with other web frameworks
19.1. Introduction
19.2. Common configuration
19.3. JavaServer Faces 1.1 and 1.2
19.3.1. DelegatingVariableResolver (JSF 1.1/1.2)
19.3.2. SpringBeanVariableResolver (JSF 1.1/1.2)
19.3.3. SpringBeanFacesELResolver (JSF 1.2+)
19.3.4. FacesContextUtils
19.4. Apache Struts 1.x and 2.x
19.4.1. ContextLoaderPlugin
DelegatingRequestProcessor
DelegatingActionProxy
19.4.2. ActionSupport Classes
19.5. WebWork 2.x
19.6. Tapestry 3.x and 4.x
19.6.1. Injecting Spring-managed beans
Dependency Injecting Spring Beans into Tapestry pages
Component definition files
Adding abstract accessors
Dependency Injecting Spring Beans into Tapestry pages - Tapestry 4.x style
19.7. Further Resources
20. Portlet MVC Framework
20.1. Introduction
20.1.1. Controllers - The C in MVC
20.1.2. Views - The V in MVC
20.1.3. Web-scoped beans
20.2. The DispatcherPortlet
20.3. The ViewRendererServlet
20.4. Controllers
20.4.1. AbstractController and PortletContentGenerator
20.4.2. Other simple controllers
20.4.3. Command Controllers
20.4.4. PortletWrappingController
20.5. Handler mappings
20.5.1. PortletModeHandlerMapping
20.5.2. ParameterHandlerMapping
20.5.3. PortletModeParameterHandlerMapping
20.5.4. Adding HandlerInterceptors
20.5.5. HandlerInterceptorAdapter
20.5.6. ParameterMappingInterceptor
20.6. Views and resolving them
20.7. Multipart (file upload) support
20.7.1. Using the PortletMultipartResolver
20.7.2. Handling a file upload in a form
20.8. Handling exceptions
20.9. Annotation-based controller configuration
20.9.1. Setting up the dispatcher for annotation support
20.9.2. Defining a controller with @Controller
20.9.3. Mapping requests with @RequestMapping
20.9.4. Supported handler method arguments
20.9.5. Binding request parameters to method parameters with @RequestParam
20.9.6. Providing a link to data from the model with @ModelAttribute
20.9.7. Specifying attributes to store in a Session with @SessionAttributes
20.9.8. Customizing WebDataBinder initialization
Customizing data binding with @InitBinder
Configuring a custom WebBindingInitializer
20.10. Portlet application deployment
VI. Integration
21. Remoting and web services using Spring
21.1. Introduction
21.2. Exposing services using RMI
21.2.1. Exporting the service using the RmiServiceExporter
21.2.2. Linking in the service at the client
21.3. Using Hessian or Burlap to remotely call services via HTTP
21.3.1. Wiring up the DispatcherServlet for Hessian and co.
21.3.2. Exposing your beans by using the HessianServiceExporter
21.3.3. Linking in the service on the client
21.3.4. Using Burlap
21.3.5. Applying HTTP basic authentication to a service exposed through Hessian or Burlap
21.4. Exposing services using HTTP invokers
21.4.1. Exposing the service object
21.4.2. Linking in the service at the client
21.5. Web services
21.5.1. Exposing servlet-based web services using JAX-RPC
21.5.2. Accessing web services using JAX-RPC
21.5.3. Registering JAX-RPC Bean Mappings
21.5.4. Registering your own JAX-RPC Handler
21.5.5. Exposing servlet-based web services using JAX-WS
21.5.6. Exporting standalone web services using JAX-WS
21.5.7. Exporting web services using the JAX-WS RI's Spring support
21.5.8. Accessing web services using JAX-WS
21.6. JMS
21.6.1. Server-side configuration
21.6.2. Client-side configuration
21.7. Auto-detection is not implemented for remote interfaces
21.8. Considerations when choosing a technology
21.9. Accessing RESTful services on the Client
21.9.1. RestTemplate
Working with the URI
Dealing with request and response headers
21.9.2. HTTP Message Conversion
StringHttpMessageConverter
FormHttpMessageConverter
ByteArrayHttpMessageConverter
MarshallingHttpMessageConverter
MappingJackson2HttpMessageConverter (or MappingJacksonHttpMessageConverter with Jackson 1.x)
SourceHttpMessageConverter
BufferedImageHttpMessageConverter
22. Enterprise JavaBeans (EJB) integration
22.1. Introduction
22.2. Accessing EJBs
22.2.1. Concepts
22.2.2. Accessing local SLSBs
22.2.3. Accessing remote SLSBs
22.2.4. Accessing EJB 2.x SLSBs versus EJB 3 SLSBs
22.3. Using Spring's EJB implementation support classes
22.3.1. EJB 2.x base classes
22.3.2. EJB 3 injection interceptor
23. JMS (Java Message Service)
23.1. Introduction
23.2. Using Spring JMS
23.2.1. JmsTemplate
23.2.2. Connections
Caching Messaging Resources
SingleConnectionFactory
CachingConnectionFactory
23.2.3. Destination Management
23.2.4. Message Listener Containers
SimpleMessageListenerContainer
DefaultMessageListenerContainer
23.2.5. Transaction management
23.3. Sending a Message
23.3.1. Using Message Converters
23.3.2. SessionCallback and ProducerCallback
23.4. Receiving a message
23.4.1. Synchronous Reception
23.4.2. Asynchronous Reception - Message-Driven POJOs
23.4.3. The SessionAwareMessageListener interface
23.4.4. The MessageListenerAdapter
23.4.5. Processing messages within transactions
23.5. Support for JCA Message Endpoints
23.6. JMS Namespace Support
24. JMX
24.1. Introduction
24.2. Exporting your beans to JMX
24.2.1. Creating an MBeanServer
24.2.2. Reusing an existing MBeanServer
24.2.3. Lazy-initialized MBeans
24.2.4. Automatic registration of MBeans
24.2.5. Controlling the registration behavior
24.3. Controlling the management interface of your beans
24.3.1. The MBeanInfoAssembler Interface
24.3.2. Using Source-Level Metadata (JDK 5.0 annotations)
24.3.3. Source-Level Metadata Types
24.3.4. The AutodetectCapableMBeanInfoAssembler interface
24.3.5. Defining management interfaces using Java interfaces
24.3.6. Using MethodNameBasedMBeanInfoAssembler
24.4. Controlling the ObjectNames for your beans
24.4.1. Reading ObjectNames from Properties
24.4.2. Using the MetadataNamingStrategy
24.4.3. Configuring annotation based MBean export
24.5. JSR-160 Connectors
24.5.1. Server-side Connectors
24.5.2. Client-side Connectors
24.5.3. JMX over Burlap/Hessian/SOAP
24.6. Accessing MBeans via Proxies
24.7. Notifications
24.7.1. Registering Listeners for Notifications
24.7.2. Publishing Notifications
24.8. Further Resources
25. JCA CCI
25.1. Introduction
25.2. Configuring CCI
25.2.1. Connector configuration
25.2.2. ConnectionFactory configuration in Spring
25.2.3. Configuring CCI connections
25.2.4. Using a single CCI connection
25.3. Using Spring's CCI access support
25.3.1. Record conversion
25.3.2. The CciTemplate
25.3.3. DAO support
25.3.4. Automatic output record generation
25.3.5. Summary
25.3.6. Using a CCI Connection and Interaction directly
25.3.7. Example for CciTemplate usage
25.4. Modeling CCI access as operation objects
25.4.1. MappingRecordOperation
25.4.2. MappingCommAreaOperation
25.4.3. Automatic output record generation
25.4.4. Summary
25.4.5. Example for MappingRecordOperation usage
25.4.6. Example for MappingCommAreaOperation usage
25.5. Transactions
26. Email
26.1. Introduction
26.2. Usage
26.2.1. Basic MailSender and SimpleMailMessage usage
26.2.2. Using the JavaMailSender and the MimeMessagePreparator
26.3. Using the JavaMail MimeMessageHelper
26.3.1. Sending attachments and inline resources
Attachments
Inline resources
26.3.2. Creating email content using a templating library
A Velocity-based example
27. Task Execution and Scheduling
27.1. Introduction
27.2. The Spring TaskExecutor abstraction
27.2.1. TaskExecutor types
27.2.2. Using a TaskExecutor
27.3. The Spring TaskScheduler abstraction
27.3.1. The Trigger interface
27.3.2. Trigger implementations
27.3.3. TaskScheduler implementations
27.4. Annotation Support for Scheduling and Asynchronous Execution
27.4.1. Enable scheduling annotations
27.4.2. The @Scheduled Annotation
27.4.3. The @Async Annotation
27.4.4. Executor qualification with @Async
27.5. The Task Namespace
27.5.1. The 'scheduler' element
27.5.2. The 'executor' element
27.5.3. The 'scheduled-tasks' element
27.6. Using the Quartz Scheduler
27.6.1. Using the JobDetailBean
27.6.2. Using the MethodInvokingJobDetailFactoryBean
27.6.3. Wiring up jobs using triggers and the SchedulerFactoryBean
28. Dynamic language support
28.1. Introduction
28.2. A first example
28.3. Defining beans that are backed by dynamic languages
28.3.1. Common concepts
The <lang:language/> element
Refreshable beans
Inline dynamic language source files
Understanding Constructor Injection in the context of dynamic-language-backed beans
28.3.2. JRuby beans
28.3.3. Groovy beans
Customising Groovy objects via a callback
28.3.4. BeanShell beans
28.4. Scenarios
28.4.1. Scripted Spring MVC Controllers
28.4.2. Scripted Validators
28.5. Bits and bobs
28.5.1. AOP - advising scripted beans
28.5.2. Scoping
28.6. Further Resources
29. Cache Abstraction
29.1. Introduction
29.2. Understanding the cache abstraction
29.3. Declarative annotation-based caching
29.3.1. @Cacheable annotation
Default Key Generation
Custom Key Generation Declaration
Conditional caching
Available caching SpEL evaluation context
29.3.2. @CachePut annotation
29.3.3. @CacheEvict annotation
29.3.4. @Caching annotation
29.3.5. Enable caching annotations
29.3.6. Using custom annotations
29.4. Declarative XML-based caching
29.5. Configuring the cache storage
29.5.1. JDK ConcurrentMap-based Cache
29.5.2. EhCache-based Cache
29.5.3. GemFire-based Cache
29.5.4. Dealing with caches without a backing store
29.6. Plugging-in different back-end caches
29.7. How can I set the TTL/TTI/Eviction policy/XXX feature?
VII. Appendices
A. Classic Spring Usage
A.1. Classic ORM usage
A.1.1. Hibernate
The HibernateTemplate
Implementing Spring-based DAOs without callbacks
A.1.2. JDO
JdoTemplate and JdoDaoSupport
A.1.3. JPA
JpaTemplate and JpaDaoSupport
A.2. Classic Spring MVC
A.3. JMS Usage
A.3.1. JmsTemplate
A.3.2. Asynchronous Message Reception
A.3.3. Connections
A.3.4. Transaction Management
B. Classic Spring AOP Usage
B.1. Pointcut API in Spring
B.1.1. Concepts
B.1.2. Operations on pointcuts
B.1.3. AspectJ expression pointcuts
B.1.4. Convenience pointcut implementations
Static pointcuts
Dynamic pointcuts
B.1.5. Pointcut superclasses
B.1.6. Custom pointcuts
B.2. Advice API in Spring
B.2.1. Advice lifecycles
B.2.2. Advice types in Spring
Interception around advice
Before advice
Throws advice
After Returning advice
Introduction advice
B.3. Advisor API in Spring
B.4. Using the ProxyFactoryBean to create AOP proxies
B.4.1. Basics
B.4.2. JavaBean properties
B.4.3. JDK- and CGLIB-based proxies
B.4.4. Proxying interfaces
B.4.5. Proxying classes
B.4.6. Using 'global' advisors
B.5. Concise proxy definitions
B.6. Creating AOP proxies programmatically with the ProxyFactory
B.7. Manipulating advised objects
B.8. Using the "autoproxy" facility
B.8.1. Autoproxy bean definitions
BeanNameAutoProxyCreator
DefaultAdvisorAutoProxyCreator
AbstractAdvisorAutoProxyCreator
B.8.2. Using metadata-driven auto-proxying
B.9. Using TargetSources
B.9.1. Hot swappable target sources
B.9.2. Pooling target sources
B.9.3. Prototype target sources
B.9.4. ThreadLocal target sources
B.10. Defining new Advice types
B.11. Further resources
C. Migrating to Spring Framework 3.1
C.1. Component scanning against the "org" base package
D. Migrating to Spring Framework 3.2
D.1. Newly optional dependencies
D.2. EHCache support moved to spring-context-support
D.3. Inlining of spring-asm jar
D.4. Explicit CGLIB dependency no longer required
D.5. For OSGi users
D.6. MVC Java Config and MVC Namespace
D.7. Decoding of URI Variable Values
D.8. HTTP PATCH method
D.9. Tiles 3
D.10. Spring MVC Test standalone project
D.11. Spring Test Dependencies
D.12. Public API changes
D.12.1. JDiff reports
D.12.2. Deprecations
E. XML Schema-based configuration
E.1. Introduction
E.2. XML Schema-based configuration
E.2.1. Referencing the schemas
E.2.2. The util schema
<util:constant/>
<util:property-path/>
<util:properties/>
<util:list/>
<util:map/>
<util:set/>
E.2.3. The jee schema
<jee:jndi-lookup/> (simple)
<jee:jndi-lookup/> (with single JNDI environment setting)
<jee:jndi-lookup/> (with multiple JNDI environment settings)
<jee:jndi-lookup/> (complex)
<jee:local-slsb/> (simple)
<jee:local-slsb/> (complex)
<jee:remote-slsb/>
E.2.4. The lang schema
E.2.5. The jms schema
E.2.6. The tx (transaction) schema
E.2.7. The aop schema
E.2.8. The context schema
<property-placeholder/>
<annotation-config/>
<component-scan/>
<load-time-weaver/>
<spring-configured/>
<mbean-export/>
E.2.9. The tool schema
E.2.10. The jdbc schema
E.2.11. The cache schema
E.2.12. The beans schema
F. Extensible XML authoring
F.1. Introduction
F.2. Authoring the schema
F.3. Coding a NamespaceHandler
F.4. Coding a BeanDefinitionParser
F.5. Registering the handler and the schema
F.5.1. 'META-INF/spring.handlers'
F.5.2. 'META-INF/spring.schemas'
F.6. Using a custom extension in your Spring XML configuration
F.7. Meatier examples
F.7.1. Nesting custom tags within custom tags
F.7.2. Custom attributes on 'normal' elements
F.8. Further Resources
G. spring.tld
G.1. Introduction
G.2. The bind tag
G.3. The escapeBody tag
G.4. The hasBindErrors tag
G.5. The htmlEscape tag
G.6. The message tag
G.7. The nestedPath tag
G.8. The theme tag
G.9. The transform tag
G.10. The url tag
G.11. The eval tag
H. spring-form.tld
H.1. Introduction
H.2. The checkbox tag
H.3. The checkboxes tag
H.4. The errors tag
H.5. The form tag
H.6. The hidden tag
H.7. The input tag
H.8. The label tag
H.9. The option tag
H.10. The options tag
H.11. The password tag
H.12. The radiobutton tag
H.13. The radiobuttons tag
H.14. The select tag
H.15. The textarea tag





