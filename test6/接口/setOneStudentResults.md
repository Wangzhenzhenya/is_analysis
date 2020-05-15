<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 接口：setOneStudentResults  [返回](../README.md)
用例： [评定成绩](../用例/评定成绩.md)

- 功能：
    设置一个学生的部分实验成绩和评语。
    
    输入参数result不为空，自动设置update_date为当前日期，表示同时设置批改日期。
    
    输入参数result为空，自动设置update_date为空，表示未批改。
    
- 权限：
    老师：可以查看/更改所有学生的成绩。
    
- API请求地址： 
    接口基本地址/v1/api/setOneStudentResults

- 请求方式 ：
    POST
 
- 请求实例：  
        { 
            "student_id": "201510315203", 
            "total": 6,
            "data": [
                {
                "student_id": "201510315203", 
                "test_id": 1,
                "course_id"
                "part1": 10,
                "rate1": 20,
                "part2": 10,
                "rate2": 20,
                "part3": 10,
                "rate3": 20,
                "part4": 10,
                "rate4": 20,
                "part5": 10,
                "rate5": 20,
                "comment": "评价",
                "result": 91,
                "update_date": "2018-04-02 13:48:01"
                }, 
                {
                ...其他实验
                }
            ] 
        }

- 请求参数说明:       
 
  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |student_id|学号|
  |test_id|实验编号|
  |part1|实验第1部分的成绩|
  |rate1|占比1|
  |part2|实验第2部分的成绩|
  |rate2|占比2|
  |part3|实验第3部分的成绩|
  |rate3|占比3|
  |part4|实验第4部分的成绩|
  |rate4|占比4|
  |part5|实验第5部分的成绩|
  |rate5|占比5|
  |result|本实验总成绩，可以为空，为空表示没有批改。|
  |comment|本实验老师的评价，可以为空|   
  |update_date|批改时间|  
 
- 返回实例：

        {         
            "status": true,
            "info": null
        }

- 返回参数说明：    
 
  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |status|bool类型，true表示正确的返回，false表示有错误|
  |info|返回结果说明信息|


