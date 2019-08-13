<div style="width:100%;height:30px;"><div style='float:right;'>- 2019.06.Django -</div></div>
<div style="float:left;width:12.5%;height:4px;background:deeppink;"></div>
<div style="float:left;width:12.5%;height:4px;background:fuchsia;"></div>
<div style="float:left;width:12.5%;height:4px;background:maroon;"></div>
<div style="float:left;width:12.5%;height:4px;background:navy;"></div>
<div style="float:left;width:12.5%;height:4px;background:crimson;"></div>
<div style="float:left;width:12.5%;height:4px;background:darkcyan;"></div>
<div style="float:left;width:12.5%;height:4px;background:purple;"></div>
<div style="float:left;width:12.5%;height:4px;background:brown;"></div>
# Django_2.1.8_Models_Manager

> <span style='color:darkcyan'>模型管理类介绍</span>

* Django中的每一个模型类都是一个模型管理类对象

  ![01](./01.png)

  django.db.models.manager.Manager类，是Django中提供的一个模型管理类，可以自定义模型管理类

> <span style='color:darkcyan'>自定义模型管理类</span>

* 创建模型管理类

  ```python
  class AddressManager(models.Manager):
    pass
  ```

* 在模型类中定义一个模型管理类对象

  ![03](./03.png)

> <span style='color:darkcyan'>自定义模型管理类应用</span>

* 改变查询的结果集

  ![02](./02.png)

![04](./04.png)

* 封装函数，操作模型类对应的数据表(增删改查)

  在Django中模型类和表一一对应，有时需要给模型类添加一些自定义方法，为了保持代码的可读性，可以把自定义方法封装放在模型管理类中

![](./05.png)

![06](./06.png)

* 通过模型管理类获取模型类

  ```python
  model_cls = self.model
  ```

  例如上述方法可以改为

![07](./07.png)

> <span style='color:darkcyan'>使用元选项指定模型类对应的表名</span>

* Django默认生成的表名：应用名小写_模型类名小写

  可以在模型类中定义一个元类Meta,通过其db_table指定其表名

![](./08.png)

​		注意：上述格式是固定的

​		指定表名之后，需要重新数据迁移

![09](./09.png)







> <span style='color:fuchsia'>fuchsia</span>
>
> <span style='color:maroon'>maroon</span>
>
> <span style='color:navy'>navy</span>
>
> <span style='color:crimson'>crimson</span>
>
> <span style='color:deeppink'>deeppink</span>
>
> <span style='color:darkcyan'>darkcyan</span>

<div style="float:left;width:12.5%;height:4px;background:deeppink;"></div>
<div style="float:left;width:12.5%;height:4px;background:fuchsia;"></div>
<div style="float:left;width:12.5%;height:4px;background:maroon;"></div>
<div style="float:left;width:12.5%;height:4px;background:navy;"></div>
<div style="float:left;width:12.5%;height:4px;background:crimson;"></div>
<div style="float:left;width:12.5%;height:4px;background:darkcyan;"></div>
<div style="float:left;width:12.5%;height:4px;background:purple;"></div>
<div style="float:left;width:12.5%;height:4px;background:brown;"></div>
<div style='width:100%;height:30px;text-align:center;'>Copyright ©2019 iticle</div>