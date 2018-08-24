### React-native 官方 demo
- 按官网提供方式安装 java jdk1.8.x, python 2.7.x,  android-studio,  android-sdk 
- 配置jdk, android 环境变量。
- 安装 react-native-cli (1.2.0)
- 安装依赖 react-native (0.55.4)  // 注意指定版本,之前一直使用最新版本，demo跑不起来。
- 连接设备（使用真机调试）， 使用Android studio 中模拟器 跑不起来。
- 配置adb 环境变量 （方便在任意cmd窗口查询设备连接情况）
    - 注： 之前我自行下载adb 工具， 发现跟sdk中adb版本不匹配，报错。
    - 使用 sdk platform-tools 目录下自带adb.exe 工具。
- 测试设备连接情况
    - adb devices
        若为
        ```
        List of devices attached
        6EB0217705000686        device
        ```
        则 设备已连接。
    - 若显示 
        ```
        List of devices attached

        D:\wenrongjiao.com\react-native\my_first_app>
        ```
        则 表示无设备连接
    - 还有一种是已连接但是 显示 offline 则执行以下命令：
        ```
        adb kill-server
        adb start-server
        ```
        重新开启服务。
    
- 使用react-native-cli脚手架初始化项目
    ```
    react-native init youProjectName
    ```
- 修改 react-native 依赖包版本
    ```
    npm install react-native@0.55.4
    ```
- 编译运行项目
    ```
    react-native run-android
    ```
    等待编译安装（初次编译安装时间比较长，可能要十几分钟）
- 编译成功，设备上显示 Welcome to React Native! 字样。