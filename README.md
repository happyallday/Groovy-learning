# Groovy-learning
Groovy学习笔记

##官方教程
[文档](http://www.groovy-lang.org/documentation.html#)


###语法

=====
###注释
````groovy
//单行注释
println "a"

/*多行注释
     多行注释*/
println "a"

println 1 /*注释1*/ + 2 /*注释2*/

````

doc注释和java 注释一致
````groovy
/**
 * A Class description
 */
class Person {
    /** the name of the person */
    String name

    /**
     * Creates a greeting method for a certain person.
     *
     * @param otherPerson the person to greet
     * @return a greeting message
     */
    String greet(String otherPerson) {
       "Hello ${otherPerson}"
    }
}
````
====

###标识符
####普通标识符
普通标识符和java基本一致，必须以字母，$或者_开头才合法.

####例如:
````groovy
def a
def d3
def $a
````
以下格式是不合法的：
````groovy
def a+b
def a#b
````
关键字跟在点后面是合法的，如下所示:
````groovy
def foo.catch
def foo.as
````

####引号标识符
引号一般跟随在点后面，例如person.name可以表示成person."name"或者person.'name'
````groovy
def map = [:]
map."key" = "value"
assert map."key" == 'value'
````

GString(可插入的字符串）和普通的字符串有所差别，可用${}标识符插入变量的值到另一个字符串，并且是永久的赋值。需要注意的是GString必须是双引号，否则失效
````groovy
def value = 'inserted_value'
def result = "aaa${value}"
assert result == 'aaainserted_value'
````



