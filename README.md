# falcon-install-and-usage
安装python2.7， 安装pip
把路径定义到python，pip上，使得能够直接调用。

git clone git://github.com/PacificBiosciences/FALCON-integrate.gitcd FALCON-integrate
git checkout master  # or whatever version you want
make init
source env.sh 修改env.sh的文件，使得pythonbase的目录指向安装python2.7的目录。
make config-edit-user
make -j all

由于drobox的网络国内连接不了。所以直接做测试会失败（make test)，所以不做。只要安装过程没报错就说明安装成功。

运行：
修改 input.fofn文件，指向我们的subreads.fasta文件。
修改 fc_run.cfg文件， run_type=local, 去掉 seg_*= XXX,的XXX。
fc_run.py fc_run.cfg
