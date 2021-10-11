# tools
工具库

### 安装

在当前目录下执行以下命令：
```bash
bash install
```

### 配置

创建环境配置文件：
```bash
# 进入到环境配置目录
cd $HOME/.tools-config/env

# 创建&编辑 Elasticsearch 测试环境配置
cp es-env.example es-test
vim es-test

# 创建&编辑 Elasticsearch 生产环境配置
cp es-env.example es-production
vim es-production
```

设置默认的环境配置，在`.bashrc`文件中加入以下代码：
```bash
# 设置 Elasticsearch 的默认环境配置
# 把测试环境配置作为默认的环境配置，以防止直接操作生产环境的数据。只有在需要的时候才临时切换到生产环境。
source $HOME/.tools-config/env/es-test
```

### 切换环境配置

打开一个新的Bash。

列出所有的环境：
```bash
tools-ls-envs
```

Elasticsearch切换为生产环境：
```bash
source $HOME/.tools-config/env/es-production
```

操作完毕，关闭当前Bash。