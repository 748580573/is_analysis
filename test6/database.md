## <center>用户表<center>
| 字段  | 类型 | 主键、外键 | 可以为空 |默认值| 约束 | 说明 |
|---    | ---  |    ---     |   ------------   |---   | --- |--- |
|user_number     | NUMBER(8,0)   |  主键 | 否 | 无 | 无 |  用户编号|
|class_number    |NUMBER(8,0)    | 外键  |否  |无  |无  |  班级号(班级表外键)  |
|user_name       |varchar(20byte)|无     |  否|  无 |无  |   用户名  |
|github_username |varchar(20byte)|无     |  否|  无 |无  |  github账号 |
|update_date     |DATE           |否     |  否|  无 |无  |  用户密码修改时间|
|password     |VARCHAR2(512 BYTE)|否     |  否|  无 |无  |  用户密码 |
|disable      |VARCHAR2(20 BYTE) |否     |否  | 无  |无  |用户是否禁用


## <center>教师表</center>
| 字段  | 类型 | 主键、外键 | 可以为空 |默认值| 约束 | 说明 |
|---    | ---  |    ---     |   ------------   |---   | --- |--- |
|teacher_number|NUMBER(8,0)|主键|否|无|无|教师编号|
|user_number|NUMBER(8,0)|外键|否|无|无|用户编号，用户表外键|
|teacher_name|varchar(20byte)|无|否|无|无|教师姓名|
|department  |varchar(30byte)|无|否|无|无|教师所在部门|

## <center>学生表</center>
| 字段  | 类型 | 主键、外键 | 可以为空 |默认值| 约束 | 说明 |
|---    | ---  |    ---     |   ------------   |---   | --- |--- |
|student_number|NUMBER(8,0) |

