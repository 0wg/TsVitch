# 构建 NSP forwarder （桌面图标）

1. make 编译
    ```shell
    make
    make tsvitch.nacp
   ```
2. hacbrewpack 打包
   新建 switch-hacbrewpack 目录，将设备key放置在目录下命名为 prod.keys
   ```shell
   mv build/exefs/main switch-hacbrewpack/exefs/main
   mv build/exefs/main.npdm switch-hacbrewpack/exefs/main.npdm
   mv tsvitch.nacp switch-hacbrewpack/control/control.nacp
   cp ../../resources/icon/icon.jpg switch-hacbrewpack/control/icon_AmericanEnglish.dat
   
   cd switch-hacbrewpack
   hacbrewpack -k prod.keys --titleid 010ff000ffff0002 --titlename tsvitch --noromfs --nologo
   ```

# 感谢

1. https://github.com/switchbrew/nx-hbloader
2. https://github.com/The-4n/hacBrewPack
