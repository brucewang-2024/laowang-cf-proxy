Workers 和 Snippets 部署 VLESS + 木马
中文|英语

Telegram 讨论与反馈群组：https://t.me/eooceu

基于 Cloudflare Workers 的高性能 VLESS+木马代理服务

特征
🚀 基于 Cloudflare Workers 的高性能代理
🌐 支持 vless + 木马
🔐 受密码保护的主页访问
📱 支持多种客户端（v2rayN、shadowrocket、loon、karing、clash、sing-box 等）
🌐 自动故障转移和负载均衡
📊 实时连接测试和状态监控
🎨 现代响应式界面
环境变量
必需变量
多变的	描述	默认	例子
PASSWORD	首页访问密码	123456	your_web_password
可选变量
多变的	描述	默认	例子
UUID//AUTH​uuid	用户 UUID	5dc15e15-f285-4a9d-959b-0e4fbdd77b63	your-uuid-here
PROXYIP//proxyip​proxyIP	代理服务器 IP 列表	13.230.34.30	ip1,ip2,ip3
SUB_PATH/subpath	订阅路径	link	sub
DISABLE_TROJAN/CLOSE_TROJAN	禁用木马，设置为 true 禁用，设置为 false 启用	false	默认设置已启用
部署步骤
方法一：通过 Cloudflare 控制面板
登录 Cloudflare 控制面板

访问Cloudflare 控制面板
登录您的帐户
创建工作进程

点击“员工和页面”
点击“创建申请”
选择“创建工作人员”
输入工作进程名称（避免使用 vless、proxy 等关键字，建议使用默认值）
上传代码

_worker.js将文件内容复制到编辑器
点击右上角的“部署”按钮
配置环境变量

在“工作程序设置”中找到“设置”→“变量”。
添加所需的环境变量并绑定自定义域
点击“保存”
访问自定义域

输入登录密码以访问主页并查看订阅链接
执照
GPL 2.0
