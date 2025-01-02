# MyBatis 3 | 配置 – mybatis
- URL: https://mybatis.org/mybatis-3/zh_CN/configuration.html
- Added At: 2025-01-02 09:53:28
- [Link To Text](2025-01-02-mybatis-3-配置-–-mybatis_raw.md)

## TL;DR
MyBatis配置文件包含多个顶层元素，如`properties`、`settings`、`typeAliases`等，用于动态替换属性、调整运行时行为、设置类型别名等。它还支持自定义类型处理器、对象工厂和插件，允许在SQL执行过程中进行拦截。环境配置支持多数据库环境，`databaseIdProvider`用于区分不同数据库厂商。`mappers`元素用于定义SQL映射语句的位置，支持多种配置方式。

## Summary
1. **MyBatis配置文件结构**：
   - MyBatis的配置文件包含多个顶层元素，用于影响MyBatis的行为：
     - `properties`：用于配置外部属性，支持动态替换。
     - `settings`：调整MyBatis的运行时行为。
     - `typeAliases`：为Java类型设置缩写名，减少冗余。
     - `typeHandlers`：处理Java类型与JDBC类型之间的转换。
     - `objectFactory`：用于创建结果对象的实例。
     - `plugins`：允许在映射语句执行过程中进行拦截。
     - `environments`：配置数据库环境，包括事务管理器和数据源。
     - `databaseIdProvider`：支持不同数据库厂商的语句执行。
     - `mappers`：定义SQL映射语句的位置。

2. **属性配置（properties）**：
   - 属性可以在外部配置文件中定义，并通过`<properties>`元素进行动态替换。
   - 支持在`SqlSessionFactoryBuilder.build()`方法中传入属性值，优先级最高。
   - 从MyBatis 3.4.2开始，支持为占位符指定默认值，需通过特定属性开启。

3. **设置配置（settings）**：
   - `settings`元素用于调整MyBatis的运行时行为，包含多个设置项，如：
     - `cacheEnabled`：全局缓存开关。
     - `lazyLoadingEnabled`：延迟加载的全局开关。
     - `autoMappingBehavior`：自动映射列到字段或属性的行为。
     - `defaultExecutorType`：默认的执行器类型。
     - `mapUnderscoreToCamelCase`：是否开启驼峰命名自动映射。
     - `logImpl`：指定MyBatis的日志实现。

4. **类型别名（typeAliases）**：
   - 类型别名用于为Java类型设置缩写名，减少XML配置中的冗余。
   - 可以通过`<typeAlias>`元素为单个类设置别名，或通过`<package>`元素为整个包下的类自动生成别名。
   - MyBatis内置了常见Java类型的别名，如`string`对应`String`，`int`对应`Integer`等。

5. **类型处理器（typeHandlers）**：
   - 类型处理器用于在预处理语句中设置参数或从结果集中取出值时，进行Java类型与JDBC类型之间的转换。
   - MyBatis内置了多种默认的类型处理器，如`BooleanTypeHandler`、`StringTypeHandler`等。
   - 支持自定义类型处理器，需实现`TypeHandler`接口或继承`BaseTypeHandler`类。

6. **对象工厂（objectFactory）**：
   - 对象工厂用于创建结果对象的新实例，默认行为是通过无参构造方法或带参数的构造方法实例化目标类。
   - 可以通过自定义对象工厂来覆盖默认行为，需实现`ObjectFactory`接口。

7. **插件（plugins）**：
   - 插件允许在映射语句执行过程中的某一点进行拦截调用，支持拦截的方法包括`Executor`、`ParameterHandler`、`ResultSetHandler`和`StatementHandler`。
   - 插件需实现`Interceptor`接口，并通过`<plugins>`元素进行配置。

8. **环境配置（environments）**：
   - MyBatis支持配置多个环境，每个环境包含事务管理器和数据源的配置。
   - 每个`SqlSessionFactory`实例只能选择一种环境，多个数据库需要多个`SqlSessionFactory`实例。
   - 事务管理器支持`JDBC`和`MANAGED`两种类型，数据源支持`UNPOOLED`、`POOLED`和`JNDI`三种类型。

9. **数据库厂商标识（databaseIdProvider）**：
   - `databaseIdProvider`用于支持不同数据库厂商的语句执行，基于映射语句中的`databaseId`属性。
   - 可以通过`<databaseIdProvider>`元素配置数据库厂商的别名，简化`databaseId`的设置。

10. **映射器（mappers）**：
    - `mappers`元素用于定义SQL映射语句的位置，支持多种配置方式：
      - 使用相对于类路径的资源引用。
      - 使用完全限定资源定位符（URL）。
      - 使用映射器接口实现类的完全限定类名。
      - 将包内的映射器接口全部注册为映射器。
