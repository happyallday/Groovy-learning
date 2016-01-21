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

####doc注释和java 注释一致
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
####但是以下格式是不合法的：
