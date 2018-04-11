Typecho 评论邮件提醒插件
=============
访客评论后，将会发送评论内容到您指定的邮箱。
原作者是 byends（https://github.com/byends/CommentToMail/） 基于 DEFE (http://defe.me) 维护的版本。
基于作者 byends 的2.0.0版本进行维护。


### 使用说明
1. 下载插件
2. 将插件上传到 `/usr/plugins/` 这个目录下
3. 登陆后台，在“控制台”下拉菜单中进入“插件管理”
4. 启用相关插件
5. 设置smtp服务器地址、邮箱地址、密码等信息

### 升级日志

##### 2.0.1 Upgrade at 2018-04-11
- 修改socket 和 curl 方式提交请求为POST方式
- 优化curl方式对于SSL证书的验证
- 更新PHPMailer邮件类至最新版

##### 2.0.0 Upgrade at 2014-04-25

版本要求：需要 Typecho `0.9 (13.12.12)`

注意：由于此版本改动较大，请先在 插件管理 中心禁用该插件的低级版本，然后再上传插件并重新激活插件，配置设置
- 添加支持后台评论管理回复评论发邮件
- 添加设置发件人选项，可自由设置发件人名称
- 添加测试发邮件功能
- 添加邮件模板编辑功能
- 支持socket 和 curl 两种方式异步触发请求

##### 1.3.2 Upgrade at 2014-04-17
- 更新PHPMailer邮件类至最新版
- 修复0.9版不能发送邮件的BUG
- 提高安全性，缓存文件读取一次后直接删除

##### 1.3.1 Upgrade at 2014-02-18
- 修复回复评论时不发送邮件的BUG
- 优化邮件发送效率

##### 1.3.0 Upgrade at 2014-01-21
 - 添加联系我邮箱配置
 
##### 1.2.6 Upgrade at 2012-07-11
- 修复接收邮箱为空时 无法获取 博主邮箱 导致无法发送邮件的BUG
- 修复已经设置邮件标题 却无效的BUG
- 修复评论者对博主的回复进行回复时，发送邮件的格式依然选择博主格式时的逻辑BUG
- 修复由于没有设置字符类型 和 编码类型 可能导致邮件乱码的BUG，字符类型设置为 UTF-8，编码类型为 base64
- 修复评论时间  时错误的BUG
- 邮件标题增加不能为空的校验
- 整理代码格式，提高可读性

