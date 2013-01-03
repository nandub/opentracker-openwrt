To install opentracker on OpenWRT:

    # cd ~
    # svn co svn://svn.openwrt.org/openwrt/trunk/ openwrt
    # cd openwrt
    # cp ./feeds.conf.default ./feeds.conf
    # echo 'src-git opentracker git://github.com/nandub/opentracker-openwrt.git' >> ./feeds.conf
    # ./scripts/feeds update -a
    # ./scripts/feeds install opentracker

Then configure for your system:

    # make menuconfig

Select your system type and the options you want and choose:

    Application ---> [*] opentracker

Then save and close the configuration menu, then allow OpenWRT to resolve dependencies:

    # make defconfig

Then build:

    # make

If you have a multicore processor, you can build faster using `-j`,
however the OpenWRT build process is not highly parallelized so your milage may vary.

    # make -j 4

To update the version of opentracker:

    # rm ./dl/opentracker-*
    # ./scripts/feeds update opentracker
    # make

