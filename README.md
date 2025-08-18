## Phigros rks Image Maker Template

本仓库为[Phigros-rks-Image-Maker](https://github.com/Tb114/Phigros-rks-Image-Maker)的启用github-actions版的模板

info.tsv等文件来自于[Phigros Resource](https://github.com/7aGiven/Phigros_Resource)

## 使用步骤

### 1. 获取SessionToken(**必要**)
网上有教程，不过多赘述

### 2. 以此为模板创建你的仓库
  - 单击右上角绿色按钮`Use this template`
  - 在弹出菜单中选择`Create a new repository`
  - **勾选** `Include all branches` **项(必要)**, 使右侧开关显示`On`
  - 在`General`的`Repository name *`栏中填写你的仓库名称(这很重要), (建议使用较短的命名)
  - `Configuration`的`Choose visibility *`项建议保持public(否则你无法在不登录时看到)，保证你的SessionToken不会泄露(前提是你需要跟着我做)
  - 点击绿色按钮`Create Repository`并稍等片刻

### 3. 配置Repository secrets
  - 打开刚才Github自动为你跳转到的网页，若不小心关闭，可在点击页面右上角用户头像给出的菜单中选择`Your Repositories`并找到你刚才命名的仓库
  - 转到`Settings`页面
  - 在左侧菜单中找到`Secrets and variables`项
  - 点击该项再点击Actions
  - 点击绿色按钮`New repository secret`
  - 在`Name*`栏中填写`SESSIONTOKEN`(严格相同)
  - 在`Secret*`栏中填写你的SessionToken(详见步骤1)
  - 点击绿色按钮`Add secret`
  
### 4.更新文件(建议在创建仓库后进行一次，该项也会定时执行)
  - 转到`Actions`页面
  - 点击右侧`Actions`栏中的`Run updatefile.py daily`
  - 点击`Run workflow`然后点击绿色按钮`Run workflow`
  - 刷新页面等待工作流完成，若出现了绿色的勾，你就做对了以上所有操作，如果时红色的叉，检查一下前面有没有哪里错了(经检查发现没有出错可以在仓库[Phigros-rks-Image-Maker](https:/github.com/Tb114/Phigros-rks-Image-Maker)或[Phigros-rks-Image-Maker-Template](https://github.com/Tb114/Phigros-rks-Image-Maker-Template)提交一下Issue，也可以bilibili上面私信[![](https://img.shields.io/badge/bilibili---Tb__-FF6699)](https://space.bilibili.com/2081603574))

### 5.生成你的成绩图(该项会定时执行)
  - 同步骤4，但是要点击`Actions`栏中的`Run main.py hourly`

### 6.找到你的成绩图
  - 转到`Code`页面
  - 找到并点击`result.png`文件(国内网络可能需要一定加载时间) \
    或者打开网址`https://github.com/{你的用户名}/{刚才你创建仓库的名称}/blob/main/result.png`(国内访问速度慢可以在网址前面加`https://github.akams.cn/`即`https://github.akams.cn/https://github.com/{你的用户名}/{刚才你创建仓库的名称}/blob/main/result.png`)
