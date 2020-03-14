# jupyter notebook



### 生成配置文件

```
jupyter notebook --generate-config
```



### 主要配置项

```python
## 登录密码，默认情况没有密码，每次启动服务器后都会产生一个随机数token
## 配置了密码后不再产生token，直接使用密码登陆
## 密码生成方法见下文
c.NotebookApp.password = 'sha1:e4ac9ea2e432:ce17c208cac9c15c59dd6f34ffe2a262f6d65bf3'

## 服务的端口，用默认的8888即可，也可指定任意非保留端口
c.NotebookApp.port = 8888

## 是否自动弹出浏览器，服务器端一般设置为不弹出
c.NotebookApp.open_browser = False

## jupyter的根目录，不设置的话就是启动命令所在的目录
c.NotebookApp.notebook_dir = '/home/usr'

## 允许远程访问，打开IP限制
c.NotebookApp.allow_remote_access = True
c.NotebookApp.ip = '*'
```



### 生成登陆密码

1. 命令行输入 `ipython` ，进入REPL环境
2. 执行：`from notebook.auth import passwd;passwd()`
3. 根据提示输入明文密码
4. 生成hash后的密码类似如下：

```
In [1]: from notebook.auth import passwd; passwd()
Enter password:
Verify password:
Out[1]: 'sha1:e4ac9ea2e432:ce17c208cac9c15c59dd6f34ffe2a262f6d65bf3'
```



### 运行

```bash
jupyter notebook
```



### 参考资料

<https://imshuai.com/jupyter-notebook-introduction-configuration>