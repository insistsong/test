# PHP中的魔术方法的触发时机#

1. __get($name)

   - 当调用一个不可访问的成员属性的时候，会自动触发。可以利用这个方法来完成对不可调用的属性进行调用，但是不能设置值

     ```php
     public class __get($name)
       {
         
       }
     ```

     ​

3. __set($name,$lue)

   - 当给一个不可访问的成员属性赋值的时候，会自动触发。可以利用这个方法完成对不可以访问的属性进行赋值

     ```php
     public class __set($name,$lue)
       {
         
       }
     ```

     ​

4. __isset($name)

   - 当使用isset函数来判断一个对象的属性的时候，如果这个属性不存在或者不可访问的时候，会触发这个方法

     ```php
     public class __isset($name)
       {
         
       }
     ```

     ​

5. __call($method,$args)

   - 当对象调用一个不可访问的成员方法或者不存在的成员方法时会被触发

     ```php
     public class __call($method,$args)
       {
         
       }
     ```

     ​

6. __callStatic($method,$args)

   - 当调用一个不可访问的静态成员方法或者不存在的静态成员方法时会被触发

     ```php
     static public class __call($method,$args)
       {
         
       }
     ```

     ​

7. __unset

   - 当要销毁不存在的成员属性或者不可以访问的成员属性的时候，会被触发

     ```php
     public function __unset()
     {
       
     }
     ```


     ```

     ​

7. __sleep()

   - 当用*serialize* 把对象进行序列化的时候，会被触发。

     ```php
     public function __sleep()
       {
         
       }
     ```

     ​

8. __weakup()

   - 当用*unserialize* 把对象进行反序列化的时候，会被触发。

     ```php
     public function __wakeup()
     {
       
     }
     ```

     ​

9. __toString

   - 当 *echo* 一个对象的时候，会触发

     ```php
     public function __toString()
     {
     	return '小可爱';
     }
     ```


10. __autoload

   - 当创建的对象的类不存在的时候，会调用该函数

     ```php
     function __autoload($name)
     {
     	var_dump($name);
     	include $name.'.php';
     }

     ```

     ​
