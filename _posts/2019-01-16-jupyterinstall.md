---
layout: post
title:  "安装Jupyter Notebook"
date:   2019-01-16 11:45:00 +0800
---
# 安装Jupyter Notebook

关注GitHub上一个印度小哥哥AI项目，短短几天时间就有2000多fork，这个项目用Jupyter比较方便，也有好多朋友安利，安装Jupyter，安装时出了一些问题，现在将安装步骤及问题处理做个简单的记录整理。
[Jupyter官网]（https://jupyter.org/）

## 安装步骤
1、安装Anaconda

2、运行Jupyter Notebook时出现环境变量问题，如下
(```)
The Jupyter HTML Notebook.

这将启动一个基于tornado的HTML笔记本服务器，它提供一个html5/
javascript笔记本客户端。

Traceback (most recent call last):
  File "/anaconda2/bin/jupyter-notebook", line 11, in <module>
    sys.exit(main())
  File "/anaconda2/lib/python2.7/site-packages/jupyter_core/application.py", line 266, in launch_instance
    return super(JupyterApp, cls).launch_instance(argv=argv, **kwargs)
  File "/anaconda2/lib/python2.7/site-packages/traitlets/config/application.py", line 657, in launch_instance
    app.initialize(argv)
  File "<decorator-gen-7>", line 2, in initialize
  File "/anaconda2/lib/python2.7/site-packages/traitlets/config/application.py", line 89, in catch_config_error
    app.print_help()
  File "/anaconda2/lib/python2.7/site-packages/traitlets/config/application.py", line 385, in print_help
    self.print_subcommands()
  File "/anaconda2/lib/python2.7/site-packages/traitlets/config/application.py", line 377, in print_subcommands
    print(os.linesep.join(lines))
UnicodeDecodeError: 'ascii' codec can't decode byte 0xe5 in position 4: ordinal not in range(128)
(```)

3、运行以下程序，修改环境变量
(```)
$ LANG=zn jupyter-notebook
(```)

查询环境变量
(```)
$ env
TERM_PROGRAM=Apple_Terminal
SHELL=/bin/bash
TERM=xterm-256color
TMPDIR=/var/folders/sb/rlrhbds13zl8g_c03rfxmdyw0000gn/T/
CONDA_SHLVL=1
Apple_PubSub_Socket_Render=/private/tmp/com.apple.launchd.JZc66mnlRg/Render
CONDA_PROMPT_MODIFIER=
TERM_PROGRAM_VERSION=404
TERM_SESSION_ID=C432B2C0-F7D2-40D7-92B1-096999948409
USER=xinchen
CONDA_EXE=/anaconda2/bin/conda
SSH_AUTH_SOCK=/private/tmp/com.apple.launchd.yFaU8Oj05F/Listeners
PATH=/anaconda2/bin:/Library/Frameworks/Python.framework/Versions/2.7/bin:/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin
CONDA_PREFIX=/anaconda2
PWD=/Users/xinchen
LANG=zh
XPC_FLAGS=0x0
XPC_SERVICE_NAME=0
SHLVL=1
HOME=/Users/xinchen
CONDA_PYTHON_EXE=/anaconda2/bin/python
LOGNAME=xinchen
CONDA_DEFAULT_ENV=base
_=/usr/bin/env
(```)
