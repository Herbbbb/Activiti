# activitispringboot
* 此工程为activiti7与springboot整合
* activiti7默认采用了spring security来做权限控制
* bpmn文件放在resources/processes目录下可以自动部署
* activiti7自动生成的表里没有历史表，需要开启配置
* 7.1.0.M6开始加入了全新的版本控制逻辑，需要在default-project.json文件里指定版本，不然启动实例会报错
# 流程图说明
* springboot01.bpmn candidateGroup为官方示例中的activitiTeam
* springboot02.bpmn candidateGroup为自定义的firstGroup和secondGroup
* qingjia.bpmn 分享演示用
* Bohui.bpmn 单个执行人的驳回，用连线方式可以解决
* Bohui2.bpmn candidate user的驳回，用连线方式有问题
* Bohui3.bpmn candidate user的驳回，用底层操作取得节点信息，重新指定节点流向解决
* Huiqian.bpmn 节点多实例实现会签 并行 条件：所有人通过才进入下一个节点
* Huiqian2.bpmn 节点多实例实现会签 并行 条件：一半以上通过则进入下一个节点
* Huiqian3.bpmn 节点多实例实现会签 串行 条件：所有人通过才进入下一个节点
* Huiqian4.bpmn 节点多实例实现会签 并行 在会签节点动态增加节点实例
* Jiaqian.bpmn 动态加签（即动态增加一个节点）：暂时无法实现，只能通过修改流程图或者代码动态增加节点后保存到流程图来实现加签，但这样一来会影响所有实例。建议尽量用节点多实例会签来替代。
* HuiqianDaiqian.bpmn 节点多实例实现代签 用户组 模拟单实例
* HuiqianDaiqian2.bpmn 节点多实例实现代签 用户组 模拟多实例
* HuiqianDaiqian3.bpmn 节点多实例实现代签 同一个流程定义，模拟单实例和多实例两种情况
