# mybatis学习笔记(三)
## TypeHandler简介及配置

Mybatis中的TypeHandler是什么？

　　无论是 MyBatis 在预处理语句（PreparedStatement）中设置一个参数时，还是从结果集中取出一个值时，都会用类型处理器将获取的值以合适的方式转换成 Java 类型。Mybatis默认为我们实现了许多TypeHandler, 当我们没有配置指定TypeHandler时，Mybatis会根据参数或者返回结果的不同，默认为我们选择合适的TypeHandler处理。
  
    <configuration>
        <typeHandlers>
      <!-- 
          当配置package的时候，mybatis会去配置的package扫描TypeHandler
          <package name="com.dy.demo"/>
       -->
      
      <!-- handler属性直接配置我们要指定的TypeHandler -->
          <typeHandler handler=""/>
      
      <!-- javaType 配置java类型，例如String, 如果配上javaType, 那么指定的typeHandler就只作用于指定的类型 -->
          <typeHandler javaType="" handler=""/>
      
      <!-- jdbcType 配置数据库基本数据类型，例如varchar, 如果配上jdbcType, 那么指定的typeHandler就只作用于指定的类型  -->
          <typeHandler jdbcType="" handler=""/>
      
      <!-- 也可两者都配置 -->
            <typeHandler javaType="" jdbcType="" handler=""/>
      
          </typeHandlers>
  
      ......
  
    </configuration>
