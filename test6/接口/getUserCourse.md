<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 接口：getUserCourse  [返回](../README.md)
用例： [查看用户课程](../用例/查看课程.md)

- 功能：
    查看用户的所有信息。
    
- 权限：
    学生/老师：查看自己的相关课程，必须先登录。    
    
- API请求地址： 
    接口基本地址/v1/api/getUserCourse<user_id>

- 请求方式 ：
    GET
      
- 请求参数说明:        

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |user_id|用户的ID号。对应表USERS.USER_ID的值|
  
- 返回实例：

        {         
            "status": true,
            "info": null,
            "ID":"2101201281",    
            "name":"张三",
            "course":[
              {
                "name":"oracle",
                "info":"*******",
                "exp_date":"2020-12-20"  
              },
              {
                 "name":"系统与分析",
                "info":"*******",
                "exp_date":"2020-12-20" 
              },
              ......
            ],
            "type":"学生"            
        }
 
- 返回参数说明：    
 
  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |status|bool类型，true表示正确的返回，false表示有错误|
  |info|返回结果说明信息|
  |ID|学号或者工号|
  |name|用户的真实姓名|  
  |course_name|课程名称|
  |course_info|课程信息|
  |exp_date|课程截止时间|
  |type|用户类型：老师或者学生|

