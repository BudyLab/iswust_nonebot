# NoneBot 版教务处机器人

[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

---

接收用户指令后执行相应教务处查询动作。

> nonebot 参考手册：  
> <https://nonebot.cqp.moe>

## 安装

先安装

```shell
poetry install
```

## 配置

### 创建环境变量

在项目根目录下创建 `.env` 文件，里面填相应的环境变量。

```py
COOLQ_ACCOUNT=xxxxx # 要登陆的 QQ 号
ENCRYPT_KEY=xxxx # 加密的key
T_CN_SOURCE=xxxx # 请求新浪短网址的 key
API_URL=xxx # 后端 API 地址
WEB_URL=xxx # WEB 页面地址
QQAI_APPID=xxx # 语音识别调用时候会用到
QQAI_APPKEY=xxx # 同上
COOLQ_DIR=xxx # coolq 的目录
```

### 配置 bot_config.py

复制一份 `bot_config_base.py` 为 `bot_config.py`。
修改里面相应的信息即可。

## 启动

需要先配置。
需要先配置。
需要先配置。

### 直接执行

启动 `run.py` 即可，如：

```sh
python3 run.py
# or
poetry run python /qbot/run.py
```

会加载代码根目录下的 `bot_config.py` 作为配置文件，你可以根据自己的需要配置。

### 使用 docker-compose 运行

直接运行：

```sh
docker-compose up -d
```

## 语音识别

识别使用的是 <https://ai.qq.com> 的 API，你需要自己去申请一个密钥，填入 .env 即可。
你需要先在环境变量中设置 `COOLQ_DIR`，这样机器人才能读取到语音文件。
