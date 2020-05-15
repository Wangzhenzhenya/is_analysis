<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 接口：setUserInfo  [返回](../README.md)
用例： [修改用户信息](../用例/修改用户信息.md)

- 功能：
    修改用户的GitHub用户名。
    
- 权限：
    学生/老师：修改自己的信息，必须先登录。    
    
- API请求地址： 
    接口基本地址/v1/api/setUserInfo

- 请求方式 ：
    POST

- 请求实例：

         {
      "id":"21048329823",
      "github_username":"ABCDE",
       "phone":"18200244217",
       "name": "张三",
       "class": "软件工程1班",
       "type": "学生"            
  }
        
- 请求参数说明:        

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |user_id|用户的ID号。对应表USERS.USER_ID的值|
  |github_username|用户GitHub用户名。| 
  |phone|用户电话|
  |name|用户名称|
  |class|用户班级|
  |type|用户类型| 
  
- 返回实例：

        {         
            "status": true,
            "info": null，
        }
 
- 返回参数说明：    
 
  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |status|bool类型，true表示正确的返回，false表示有错误|
  |info|返回结果说明信息|


