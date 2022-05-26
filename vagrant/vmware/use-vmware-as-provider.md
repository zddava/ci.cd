# 用vmware做provider

1. 下载 [vmware-utility](https://www.vagrantup.com/docs/providers/vmware/vagrant-vmware-utility)

2. 安装vmware-desktop插件

    vagrant plugin install vagrant-vmware-desktop

3. 下载box(可以省略)，找provider是vmware-desktop的，HashiCorp提供的[下载Box的网站](https://app.vagrantup.com/boxes/search)

4. 安装box，下载box的才需要

    vagrant box add [box_name] [box_path]

5. 编写Vagrantfile

    Vagrant.configure("2") do |config|
        config.vm.box = "generic/ubuntu2004"
    end

6. 启动

    vagrant up --provider vmware_desktop

7. [关键参数](https://www.vagrantup.com/docs/providers/vmware/configuration#nat_device)
