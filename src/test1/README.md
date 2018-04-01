# test
第一次实验
=============================
# test1为pg107实验
@startuml
start
:安排考试;
:出卷;
fork
:A、B试卷;
fork again
:打印审批表;
:审批签字;
:打印审批表;
endfork;
:打印试卷;
:试卷;
:参加考试;
:答卷;
:阅卷出成绩;
    fork
    :成绩单;
    fork
    : 有不及格?;
     ->有;
    : 安排考试;
    : 补考安排表;
    fork again
    :答卷;
    :装订存档;
    endfork;
    :期末流程结束;
    endfork;
end
@enduml


![Image text](https://github.com/748580573/is_analysis/blob/master/src/test1/flow1.png)


@startuml
start
:申请服务;
if(是新用户?)then(是)
:登记用户信息;
else(不是)
endif
:上门勘察;
:指定方案;
if(满意吗?)then(否)
end
else(是)
:签订服务合同;
fork
:安排人工;
fork again
:安排材料;
endfork;
:填写派工单;
:领取材料;
:上门服务;
:验收并填写反馈意见;
:交回派工单;
:结算收款;
end
@enduml
