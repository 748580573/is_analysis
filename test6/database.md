## <center>用户表<center>
| 字段  | 类型 | 主键、外键 | 可以为空 |默认值| 约束 | 说明 |
|:---:  | :---:|   :---:    |  :-----------:  |:---: | :---: | :---: |
|user_number     | NUMBER(8,0)   |  主键 | 否 | 无 | 无 |  用户编号|
|class_number    |NUMBER(8,0)    | 外键  |否  |无  |无  |  班级号(班级表外键)  |
|user_name       |varchar(20byte)|无     |  否|  无 |无  |   用户名  |
|github_username |varchar(20byte)|无     |  否|  无 |无  |  github账号 |
|update_date     |DATE           |否     |  否|  无 |无  |  用户密码修改时间|
|password     |VARCHAR2(512 BYTE)|否     |  否|  无 |无  |  用户密码 |
|disable      |VARCHAR2(20 BYTE) |否     |否  | 无  |无  |用户是否禁用


## <center>教师表</center>
| 字段  | 类型 | 主键、外键 | 可以为空 |默认值| 约束 | 说明 |
| :---:  | :---:  |  :---:     |   :---------:   | :---: | :---: |:---: |
|teacher_number|NUMBER(8,0)|主键|否|无|无|教师编号|
|user_number|NUMBER(8,0)|外键|否|无|无|用户编号，用户表外键|
|teacher_name|varchar(24byte)|无|否|无|无|教师姓名|
|department  |varchar(32byte)|无|否|无|无|教师所在部门|

## <center>学生表</center>
| 字段  | 类型 | 主键、外键 | 可以为空 |默认值| 约束 | 说明 |
|  :---:  | :---:  |  :---:   |  :-----------:   | :---:  | :---: | :---: |
|student_number|NUMBER(8,0) |主键|否|无|无|学生学号|
|user_number|NUMBER(8,0)|外键键|否|无|无|用户表外键|
|student_name|varchar(20byte)|无|否|无|无|学生姓名|
|class_number|NUMBER(8,0)|无|否|无|无|班级号|
|student_major|varchar(32byte)|无|否|无|无|课程|
|web_sum|VARCHAR(400 BYTE)|无|否|无|无|GitHub网址是否正确，用逗号分开，Y代表正确，N代表不正确。第1位代表总的GitHUB地址是否正确，第2位表示第1次实验的地址，第3位表示第2位实验地址，依此类推。比如：“Y,Y,Y,Y,Y,N”表示第5次实验地址不正确，其他地址正确|

## <center>成绩表</center>
| 字段  | 类型 | 主键、外键 | 可以为空 |默认值| 约束 | 说明 |
|:---:    | :---:  |    :---:     |   :---------:   | :---:   | :---: | :---: |
|class_number|NUMBER(8,0)|主键|否|无|无|课程编号|
|student_number|NUMBER(8,0)|外键|否|无|无|学生编号（学生表外键）|
|class_name|varchar(32byte)|无|否|无|无|课程名|
|result | float|无|否|无|无|成绩分数|
|memo   |varchar(400byte)|无|否|无|无|评价|
|update_date|Date|无|否|无|无|成绩修改时间|

## <center>课程表</center>
| 字段  | 类型 | 主键、外键 | 可以为空 |默认值| 约束 | 说明 |
|:---:    | :---:  |    :---:     |   :---------:   | :---:   | :---: | :---: |
|class_number|NUMBER(8,0)|主键|否|无|无|课程编号|
|teacher_number/NUMBER(8,0)|外键|否|无|无|教师编号|
|courses_coll|NUMBER(8,0)|外键|否|无|无|开课学院号|
|courses_name|varchar(32byte)|否|否|无|无|课程名|



## <center>学生-课程中间表</center>
| 字段  | 类型 | 主键、外键 | 可以为空 |默认值| 约束 | 说明 |
|:---:    | :---:  |    :---:     |   :---------:   | :---:   | :---: | :---: |
|id|int |主键|否|无|无|主键id无意义|
|student_number|NUMBER(8,0)|外键|无|无|无|学生表外键|
|class_nubmer|NUMBER(8,0)|外键|无|无|无|课程表外键|

## <center>学生-教师中间表</center>
| 字段  | 类型 | 主键、外键 | 可以为空 |默认值| 约束 | 说明 |
|:---:    | :---:  |    :---:     |   :---------:   | :---:   | :---: | :---: |
|id|int |主键|否|无|无|主键id无意义|
|student_number|NUMBER(8,0)|外键|无|无|无|学生表外键|
|teacher_number|NUMBER(8,0)|外键|无|无|无|教师表外键|

## <center>教师-课程中间表</center>
| 字段  | 类型 | 主键、外键 | 可以为空 |默认值| 约束 | 说明 |
|:---:    | :---:  |    :---:     |   :---------:   | :---:   | :---: | :---: |
|id|int |主键|否|无|无|主键id无意义|
|class_number|NUMBER(8,0)|外键|无|无|无|课程表外键|
|teacher_number|NUMBER(8,0)|外键|无|无|无|教师表外键|

## <center>学生-成绩</center>
|id|int |主键|否|无|无|主键id无意义|
|student_number|NUMBER(8,0)|外键|无|无|无|学生表外键|
|score_number|NUMBER(8,0)|外键|无|无|无|成绩表外键|


