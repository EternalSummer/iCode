<i.summer@aliyun.com> 邮箱
#Handlebars基本使用

##一、如何引入handlebars
1.  引入jquery.js
2.  引入handlebars.js


##二、基础语法

{{}} 不解析html特殊字符

{{{}}} 解析html特殊字符 &lt；&nbsp；

块表达式以{{#表达式}}开头{{/表达式}}结尾
### 1. each循环

    <!--id可以用来唯一确定一个模版,type是模版固定的写法-->
    <script id="table-template" type="text/x-handlebars-template">
      {{#each student}}
        <tr>
          <td align="center">{{name}}</td>
          <td align="center">{{sex}}</td>
          <td align="center">{{age}}</td>
        </tr> 
      {{/each}}
    </script>


----
	
      <script type="text/javascript">
      $(document).ready(function() {
        //模拟的json对象
        var data = {
                    "student": [
                        {
                            "name": "张三",
                            "sex": "0",
                            "age": 18
                        },
                        {
                            "name": "李四",
                            "sex": "0",
                            "age": 22
                        },
                        {
                            "name": "妞妞",
                            "sex": "1",
                            "age": 18
                        }
                    ]
                };
        
        //注册一个Handlebars模版，通过id找到某一个模版，获取模版的html框架
        //$("#table-template").html()是jquery的语法，不懂的童鞋请恶补。。。
        var source = $("#table-template").html();
        var myTemplate = Handlebars.compile(source);
        
        //将json对象用刚刚注册的Handlebars模版封装，得到最终的html，插入到基础table中。
        $('#tableList').html(myTemplate(data));
      });
    </script>
    
----
很多时候，我们拿到的json对象，本身就是一个list，并不是map，直接就可以遍历，不需要#each student这样指定遍历某个属性。此时可以用#each this，表示遍历当前对象。**this**表示当前上下文，非常灵活，以后还会提及，读者可以举一反三。



     <script id="table-template" type="text/x-handlebars-template">
      {{#each this}}
        <tr>
          <td>{{name}}</td>
          <td>{{sex}}</td>
          <td>{{age}}</td>
        </tr> 
      {{/each}}
    </script>