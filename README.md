# -Actions-Workflow-V2ray-Ubuntu-
这是借用 actions 产生的虚拟机网络环境从而让我访问国际互联网，FreeVPS-ubuntu-latest 项目被人举报了，github管理员禁用了我的项目，唉，重做吧，可能不会像之前做的那样好了吧，毕竟源码也没有了，重头开始吧。

## 描述
1. 这个项目主要是为了弥补另一个 FreeVPS-ubuntu-latest 项目，因为被管理员禁用，我也是重新制作测试，为了能够正常看 youtube 和 google。  
2. 运行 actions workflow 用于运行脚本，需要添加 `GITHUB_TOKEN` 环境变量，这个是访问 GitHub API 的令牌，可以在 GitHub 主页，点击个人头像，Settings -> Developer settings -> Personal access tokens ，设置名字为 GITHUB_TOKEN 接着要勾选权限，勾选repo、admin:repo_hook和workflow即可，最后点击Generate token，如图所示  
![image](https://user-images.githubusercontent.com/94947393/198914419-0f567e83-03b2-4a33-845f-0039236fb640.png)  
3. 添加 linux 用户名 `USER_NAME` 在 GitHub 仓库页 -> Settings -> Secrets -> actions -> New repository secret  
4. 添加 linux 密码 `USER_PW` 在 GitHub 仓库页 -> Settings -> Secrets -> actions -> New repository secret  
5. 添加 linux hostname `HOST_NAME` 在 GitHub 仓库页 -> Settings -> Secrets -> actions -> New repository secret  
6. 注册 Ngrok 账户登录，并复制 Ngrok AUTH TOKEN key 位置在此 https://dashboard.ngrok.com/auth/your-authtoken
7. 添加 ngrok `NGROK_AUTH_TOKEN` 在 GitHub 仓库页 -> Settings -> Secrets -> actions -> New repository secret  
8. 添加 email smtp 服务器域名 `MAILADDR` 在 GitHub 仓库页 -> Settings -> Secrets -> actions -> New repository secret    
9. 添加 email smtp 服务器端口 `MAILPORT` 在 GitHub 仓库页 -> Settings -> Secrets -> actions -> New repository secret    
10. 添加 email smtp 服务器登录账号 `MAILUSERNAME` 在 GitHub 仓库页 -> Settings -> Secrets -> actions -> New repository secret  
11. 添加 email smtp 服务器第三方登陆授权码 `MAILPASSWORD` 在 GitHub 仓库页 -> Settings -> Secrets -> actions -> New repository secret  
12. 添加  email smtp 服务器应该发送邮件位置 `MAILSENDTO` 在 GitHub 仓库页 -> Settings -> Secrets -> actions -> New repository secret  
13. 转到 Actions -> -Actions-Workflow-V2ray-Ubuntu- 并且启动 workflow，实现自动化  
14. 新修改目录结构  

        .
        ├── getorupdatefile.sh                          # 搭建脚本  
        └── README.md                                   # 这个是说明文件   
    
9. 出于安全考虑还是使用邮箱把发送内容发给自己的邮箱  
10. ~这次能维持6h挺好~维持的时间还是不稳定  
11. 紧急修复了v2ray配置文件，发现配置文件写入方式有问题导致不能上google，现在我终于可以舒舒服服的使用google和duckduckgo了。

# 声明
本项目仅作学习交流使用，用于查找资料，学习知识，不做任何违法行为。所有资源均来自互联网，仅供大家交流学习使用，出现违法问题概不负责。  
