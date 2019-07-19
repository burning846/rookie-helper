# Anaconda



* Download: Visit the [official website](https://www.anaconda.com/) to DOWNLOAD the bash file.

* Install: Just run`bash <filename>` , For example `bash Anaconda3-2018.12-Linux-x86_64.sh`
  * There is an option which can automatically update your `~/.bashrc`  which can add `Anaconda/bin` to your PATH.
  * After installation the bash file can also download and install *Visual Studio Code*, but if you use a server WITHOUT display screen, VScode is useless.
  * After installation, run `source ~/.bashrc` to update your PATH to use `conda`. Restart the terminal or reconnect the server can also work.
* Create new environment: `conda create -n <env_name> python=x.x`
* Activate an environment: `source activate <env_name>`
* Install Package: `conda install <package_name>`
  * Add version if needed: `conda install <package_name>=<version_number>`. for example `conda install opencv-python=4.1.0.25`



* 下载：访问[官网](https://www.anaconda.com/)下载安装包
* 安装：在命令行运行 `bash <filename>`，比如 `bash Anaconda3-2018.12-Linux-x86_64.sh`
  * 安装中有一个选项让你更新`~/.bashrc`这个文件，从而可以在你连接时自动将`Anaconda/bin` 加入到你的系统路径中。
  * 安装结束后，bash安装文件会询问是否安装*Visual Studio Code*，如果你用的是没有显示设备的服务器，建议不安装
  * 安装结束后，运行 `source ~/.bashrc`  来更新你的系统路径从而可以使用`conda` 命令，重启终端或者重新连接服务器也可以起到同样的效果
* 创建新环境：`conda create -n <env_name> python=x.x`
* 激活一个环境：`source activate <env_name>`
* 安装库文件：`conda install <package_name>`
  * 如果需要特定版本的库的话，可以加上版本号，如`conda install opencv-python=4.1.0.25`