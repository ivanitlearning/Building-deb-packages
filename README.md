# Building .deb packages
Repo for [tutorial on building deb packages](https://ivanitlearning.wordpress.com/2019/10/27/writing-your-own-deb-package/).

### Prep
Download the [mysql-5.5.50 server package](https://downloads.mysql.com/archives/community/) first, before git clone.
```
ivan@ubuntu:~$ wget https://downloads.mysql.com/archives/get/file/mysql-5.5.50-linux2.6-x86_64.tar.gz
# Then unzip to subdir usr/local of the directory containing the DEBIAN directory
ivan@ubuntu:~$ tar -C mysql.server-5.5.50/usr/local -xzvf mysql-5.5.50-linux2.6-x86_64.tar.gz
# ...
ivan@ubuntu:~$ tree -a -L 4 mysql.server-5.5.50
mysql.server-5.5.50
├── DEBIAN
│   ├── control
│   ├── postinst
│   ├── postrm
│   ├── preinst
│   └── prerm
└── usr
    └── local
        └── mysql-5.5.50-linux2.6-x86_64
            ├── bin
            ├── COPYING
            ├── data
            ├── docs
            ├── include
            ├── INSTALL-BINARY
            ├── lib
            ├── man
            ├── mysql-test
            ├── README
            ├── scripts
            ├── share
            ├── sql-bench
            └── support-files

15 directories, 8 files

```
