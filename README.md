Workers 和 Snippets 部署 VLESS + 木马 + shadowsocks
中文|英语

Telegram交流反馈小组：https://t.me/eooceu

基于 Cloudflare Workers & Snippets 的性能 VLESS+trojan 代理服务

YouTube视频部署教程：https://youtu.be/GEcKz2NoKlM

Shadowsocks部署视频教程：https://youtu.be/hUPN_69Atow

页面部署视频教程：https://www.youtube.com/watch?v=kNi6OwJ_e5k

功能特性
🚀 基于 Cloudflare Workers 和 snippets 的性能代理
🌐 vless + trojan 双协议支持
🔐密码保护的主页访问
📱支持多种客户端(v2rayN,shadowrocket,loon,karing,clash,sing-box等)
🌐 自动故障转移和负载均衡
📊 实时连接测试和状态监控
📊默认取消speedtest测速
环境指标配置
简单参数
指标名	描述	默认值	效果
PASSWORD	主页访问密码	123456	your_web_password
工人任选变量
指标名	描述	默认值	效果
UUID或AUTH或uuid	用户UUID	5dc15e15-f285-4a9d-959b-0e4fbdd77b63	your-uuid
PROXYIP或proxyip或proxyIP	代理服务器IP列表	13.230.34.30	tw.tp81.netlib.re
SUB_PATH或subpath	订阅路径	link	sub
DISABLE_TROJAN或CLOSE_TROJAN	是否关闭木马协议，true关闭，false开启	false	默认开启
步骤部署
登录 Cloudflare 仪表板

访问Cloudflare 仪表板
登录您的账户
创建Worker

点击“工人和页面”
点击“创建应用程序”
选择“创建工人”
输入Worker名称(不要带vless,proxy之类的关键词，建议默认)
上传代码

将_worker.js文件内容复制到编辑器
点击右上角“部署”
配置环境变量

在Worker设置中找到“Settings”→“Variables”
添加所需的环境变量并绑定自定义域名
点击“保存”
访问域名

输入登录密码进入主页查看相关订阅链接
snippets /workers 路径进阶方式
相关路径说明
图像
类型	效果	说明
默认路径	/?ed=2560	使用代码里设置的默认值proxyip
代理IP	/?ed=2560&proxyip=proxyip.domain.com或proxyip=proxyip.domain.com	使用域名形式proxyip
带proxyip的端口	/?ed=2560&proxyip=ip:port或/proxyip=ip:port	使用带端口的proxyip
袜子5	/?ed=2560&proxyip=socks://user:pass@host:port或/proxyip=socks://user:pass@host:port	使用全局SOCKS5出站协议头socks5
HTTP	/?ed=2560&proxyip=http://user:pass@host:port或/proxyip=http://user:pass@host:port	使用 HTTP 全局/HTTPS 出站
cloudns 域名解析配置片段统一使用的域名
_acme-challenge
Shadowsocks 节点参数对照图
节点路径为SSpath变量或uuid引用，示例：/5dc15e15-f285-4a9d-959b-0e4fbdd77b63/?ed=2560

带proxyip的示例：/5dc15e15-f285-4a9d-959b-0e4fbdd77b63/?ed=2560&proxyip=xxxx v2rayN上设置全局socks5或http出站

小火箭示例:/5dc15e15-f285-4a9d-959b-0e4fbdd77b63/proxyip=xxxx设置socks5或http全局出站,karing,nekobox一样设置

许可证
GPL 2.0
