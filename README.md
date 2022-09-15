## Stream 综合测试项目 
***
#### 请不要修改处trigger之外的所有分支，一切测试都可以在 trigger与trigger.txt 完成
***

##### 测试结果
+ 综合测试
  1. 所有MR应该是**全绿**（除了V1）
  2. 当前commitId对应的push和tagpush应该是**全绿**
+ 特殊测试
  1. 测试结束后页面不应出现流水线 **删除流水线测试**

> ##### 触发测试
>
> - .ci/trigger.yml 触发测试逻辑的Yaml文件
> - trigger 分支，用来在此分支修改触发构建
> - trigger.txt 总触发文件,修改后开启测试

> ##### 触发测试-特殊测试
>
> - .ci/trigger-tmp.yml 特殊触发测试逻辑的Yaml文件
> - trigger-tmp 用来执行触发分支
> - ymls/delete.yml 用来测试流水线删除的功能

> ##### 全部语法测试(除模板)
> 
> - .ci/all.yml 全部语法Yaml文件
> - trigger 触发分支
> - master MR目标分支
> - triggers/trigger-all.txt 触发文件 -自动修改(手动)

> ##### 全部语法测试(模板)
> 
> - .ci/all-templates.yml 全部语法(模板)Yaml文件
> - .ci/templates/all-test/* 测试需要的模板文件
> - all-test-templates 测试需要的远程模板库
> - private_token 测试需要的凭证
> - trigger 触发分支
> - master MR目标分支
> - triggers/trigger-all-templates.txt 触发文件 -自动修改(手动)

> ##### Stage-Check 功能综合测试
> 
> - .ci/check.yml Stage-Check 功能综合测试Yaml文件
> - .ci/templates/check/* 测试需要的模板文件
> - all-test-templates 测试需要的远程模板库
> - trigger 触发分支
> - master MR目标分支
> - triggers/trigger-check.txt 触发文件 -自动修改(手动)

> ##### 跨项目引用构建机测试 测试
> 
> - .ci/merge-action.yml otherAgent 测试Yaml文件
> - trigger-tmp 用来执行触发分支

> ##### merge action 测试
> 
> - .ci/merge-action.yml merge action 测试Yaml文件
> - 手动reopenMr触发
