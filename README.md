20241023 日报：
 1： 下载并且编译 
     DC1E OS6.2交付分支（2024.8.27）：
       Android：
        repo init -u https://snc-gerrit.zeekrlife.com/a/all/manifests -b aptiv_develop_sa8295p_postcs1_270
        repo sync
    268分支和流程文档的编译过程中都出现过错误；
    today work
    和yangweny熟悉业务流程；
    根据技术文档和需求文档 熟悉业务流程
    zeekr/android/platform/vendor/zeekr/interfaces/camera
    zeekr/android/platform/vendor/zeekr/interfaces/impl/camera
    zeekr/android/platform/vendor/zeekr/modules/cameradevicemanager
    zeekr/android/platform/vendor/zeekr/modules/soundrecorder
    zeekr/android/platform/vendor/zeekr/interfaces/carcameramanager
    zeekr/android/platform/vendor/zeekr/interfaces/impl/carcameramanager
 20241024 日报：
    1：阅读confirence 入职流程文档；查看Android 框架源码；
    2： 和yangwenyo现场熟悉了 紧急录音，视频；自动泊车，停摆泊车，哨兵模式

today work
    1：参考confurence入职流程文档 提交一个patch;
    2:申请 vendor/zeekr/interface（modules） 其他模块的代码，单独编译
    3：申请svn ：13：3690、IVI 权限
    4：熟悉JFrog刷机
    5： 编译自己的库 ，自己打印一些log,推到车机里面，跑起来。   
    pwd: /home/e-qiang.chen3/snc-android/test_device/lagvm/LINUX/android

20241025 日报：
    1：参考confurence入职流程文档 提交一个patch，已完成。没有caseId号码；
    2：申请 vendor/zr/interface（modules） 其他模块的代码，单独编译 ，其中 cameradevicemanager 单独编译报错，今天解决；
    3：申请svn ：13：3690、IVI 权限 已申请完成
    today work 
    1: cameradevicemanager 单独编译报错，今天解决
    2：代码路径：vendor/zeekr/interfaces/impl/carcameramanager
    [8295DHU][IVI]CarCameraManager 注释密度提升

20241026 日报：

    1、主线分支 zeekr_mainline_dev 的 CarCameraManager 编译通过

    2、参考 gerrit 提交 ，补充注释密度

        vendor/zeekr/interfaces/impl/carcameramanager

        git branch

        ​zeekr_release_sa8295p_postcs_ef_110

        ​git checkout (-b) zeekr_mainline_dev 

        ​git checkout  zeekr_mainline_dev 

        ​cd  vendor/zeekr/interfaces/impl/carcameramanager

        ​/home/e-qiang.chen3/snc-android/hlos_dev_la/lagvm/LINUX/android/vendor/zeekr/interfaces/impl/carcameramanager/1.0

        cd /vendor/zeekr/interfaces/impl/carcameramanager/1.0

        mm -B

    2024年10月29日

    1： 下载并且编译 

        DC1E OS6.2交付分支（2024.8.27）：

        ​    Android：

        ​    repo init -u https://snc-gerrit.zeekrlife.com/a/all/manifests -b aptiv_develop_sa8295p_postcs1_270

        ​    repo sync

        ​      268分支和流程文档的编译过程中都出现过错误；

        https://devops-confluence.zeekrlife.com/pages/viewpage.action?pageId=102184438

        zeekr_repo init -b zeekr_develop_sa8295p_postcs -m 3rd.xml

        zeekr_repo sync

    zeekr_develop_sa8295p_postcs 分支:

    cd test_device/lagvm/LINUX/android/

    zeekr_build

    source build/envsetup.sh

    lunch zeekr_dhu-userdebug  （user版本 lunch zeekr_dhu-user）

    lunch zeekr_dhu_sa8295-userdebug

    export ZEEKR_PROJECT_NAME="ONEIMAGE-POSTCS1"

    export PRODUCT_ZEEKR_VEHICLE_TYPE="ONEIMAGE-POSTCS1"

    make

    e-qiang.chen3@android:~/android_zeekr_develop_sa8295p_postcs/hlos_dev_la/lagvm/LINUX/android/build$ lunch

    You're building on Linux

    Lunch menu... pick a combo:

    1. aosp_arm-eng
    2. aosp_arm64-eng
    3. aosp_blueline_car-userdebug
    4. aosp_bonito_car-userdebug
    5. aosp_bramble_car-userdebug
    6. aosp_car_arm-userdebug
    7. aosp_car_arm64-userdebug
    8. aosp_car_x86-userdebug
    9. aosp_car_x86_64-userdebug
    10. aosp_cf_arm64_auto-userdebug
    11. aosp_cf_arm64_phone-userdebug
    12. aosp_cf_x86_64_foldable-userdebug
    13. aosp_cf_x86_64_pc-userdebug
    14. aosp_cf_x86_64_phone-userdebug
    15. aosp_cf_x86_64_tv-userdebug
    16. aosp_cf_x86_auto-userdebug
    17. aosp_cf_x86_phone-userdebug
    18. aosp_cf_x86_tv-userdebug
    19. aosp_coral_car-userdebug
    20. aosp_crosshatch_car-userdebug
    21. aosp_flame_car-userdebug
    22. aosp_oriole_car-userdebug
    23. aosp_raven_car-userdebug
    24. aosp_redfin_car-userdebug
    25. aosp_sargo_car-userdebug
    26. aosp_sunfish_car-userdebug
    27. aosp_trout_arm64-userdebug
    28. aosp_trout_x86-userdebug
    29. aosp_x86-eng
    30. aosp_x86_64-eng
    31. arm_krait-eng
    32. arm_v7_v8-eng
    33. armv8-eng
    34. armv8_cortex_a55-eng
    35. armv8_kryo385-eng
    36. atoll-userdebug
    37. beagle_x15-userdebug
    38. beagle_x15_auto-userdebug
    39. car_ui_portrait-userdebug
    40. car_x86_64-userdebug
    41. cuttlestone_x86_64_phone-userdebug
    42. cuttlestone_x86_phone-userdebug
    43. db845c-userdebug
    44. gsi_car_arm64-userdebug
    45. gsi_car_x86_64-userdebug
    46. hikey-userdebug
    47. hikey64_only-userdebug
    48. hikey960-userdebug
    49. hikey960_tv-userdebug
    50. hikey_tv-userdebug
    51. msm8909-userdebug
    52. msm8909go-userdebug
    53. msm8996-userdebug
    54. msmnile-userdebug
    55. msmnile_au-user
    56. msmnile_au-userdebug
    57. msmnile_gvmq-user
    58. msmnile_gvmq-userdebug
    59. msmnile_tb-user
    60. msmnile_tb-userdebug
    61. pixel3_mainline-userdebug
    62. poplar-eng
    63. poplar-user
    64. poplar-userdebug
    65. qemu_trusty_arm64-userdebug
    66. qssi-userdebug
    67. sdk_car_arm-userdebug
    68. sdk_car_arm64-userdebug
    69. sdk_car_portrait_x86_64-userdebug
    70. sdk_car_x86-userdebug
    71. sdk_car_x86_64-userdebug
    72. sdm845-userdebug
    73. silvermont-eng
    74. sm6150-userdebug
    75. sm6150_au-user
    76. sm6150_au-userdebug
    77. uml-userdebug
    78. yukawa-userdebug
    79. yukawa_sei510-userdebug
    80. zeekr_dhu_sa8295-user
    81. zeekr_dhu_sa8295-userdebug
    82. zeekr_dhu_sa8295_r-user
    83. zeekr_dhu_sa8295_r-userdebug

    out/soong/.bootstrap/soong-sdk

    out/target/product/zeekr_dhu_sa8295/data/fuzz/arm64/vendor.zeekr.hardware.carcameramanager@1.0-vts.fuzzer/vendor.zeekr.hardware.carcameramanager@1.0-vts.fuzzer

    zeekr_develop_sa8295p_postcs

    这个分支上新建impl

    ///android_zeekr_develop_sa8295p_postcs/hlos_dev_la/lagvm/LINUX/android/vendor/zeekr/interfaces/

    单独编译 /vendor/zeekr/interfaces/impl/carcameramanager

    pwd:

    hlos_dev_la/lagvm/LINUX/android/vendor/zeekr/interfaces

    cd .

    pwd:/vendor/zeekr/interfaces

    mkdir -p impl

    cd cd impl/

    访问 ：https://snc-gerrit.zeekrlife.com/admin/repos

    git clone url

    /interfaces/impl/carcameramanager/1.0

    ls
    mm
    /**
    * 函数名: ZeekrAudioManager
    * 描述: 
    * 参数:
    * 返回值:
    */

MODIFY SNC8295-5484 [8295DHU][IVI] carcameramanager基础代码质量检查注释密度优化

Root cause: 代码注释密度低于20%了, 按照代码检测规定需要增加注释.

Solution: 按照代码检测规定需要增加注释.

Test suggest: 只增加注释, 没有更改代码, 无需测试.

test case: 无.

 git gerrit

git push origin HEAD:refs/for/zeekr_mainline_dev

git config --global core.autocrlf false 

git config --global core.autocrlf false 

2024年11月2日

https://devops-confluence.zeekrlife.com/pages/viewpage.action?pageId=61798636

新建文件夹：

aptiv_develop_sa8295p_postcs1_270:

切换到docker环境

zeekr_build;
 1： 下载并且编译 
   DC1E OS6.2交付分支（2024.8.27）：
​    Android：
​    老版本不对:  repo init -u https://snc-gerrit.zeekrlife.com/a/all/manifests -b aptiv_develop_sa8295p_postcs1_270 
​    repo sync
   新版本 ： zeekr_repo init -u https://snc-gerrit.zeekrlife.com/a/all/manifests -b aptiv_develop_sa8295p_postcs1_270 -m 3rd.xml
​	zeekr_repo sync    
   cd test_device/lagvm/LINUX/android/
   source build/envsetup.sh
   lunch
    270分支
    lunch zeekr_dhu-userdebug
    选择 userdebug版本 
    export ZEEKR_PROJECT_NAME="ONEIMAGE-POSTCS1"
    export PRODUCT_ZEEKR_VEHICLE_TYPE="ONEIMAGE-POSTCS1"
    make -j8

\```

2024年11月5日日报

    Z:\android_zeekr_develop_sa8295p_postcs\hlos_dev_la\lagvm\LINUX\android\device\zeekr\sa8295_common\config\watermark
    android/device/zeekr/sa8295_common/config/watermark 你自己下到堡垒机上

    hlos_dev_la/lagvm/LINUX/android/device/zeekr/sa8295_common/config/watermark$

    **__FILE__** ：正在编译文件的文件名**__LINE__** ：正在编译文件的行号 DATE__**：编译时刻的日期字符串 如“Sep 22 2020”

    TIME__**：编译时刻的时间字符串 如”10:00:00“  STDC__**：判断该文件是不是标准C程序 **__func__**：它指示所在的函数

    zeekr_onCameraDataChangeNotify(const ZeekrCamMsg &msg) {

    // std::chrono::system_clock::time_point now_time = std::chrono::system_clock::now();

    /* this_thread::sleep_for(std::chrono::milliseconds(33));

    {

    frame_count++;

    } */

    // std::thread::id this_id = std::this_thread::get_id();

    // cout << "enter zeekr_onCameraDataChangeNotify 回调函数,线程id:" << this_id << endl;

    // std::this_thread::sleep_for(std::chrono::milliseconds(500));

    // cout << "first pid get memory success msg_type= " << msg.msg_type << " msg_content= " << msg.msg_content

    //  << " memory addr= " << msg.mem.handle() << " size:" << msg.size << " format:" << msg.format << endl;

    //auto duration = std::chrono::duration_cast<std::chrono::milliseconds>(now_time - global_start_time);

    //每500ms，给心跳线程发送信息

    /// if(duration.count()%notifyTime==0){

    // if(zKKER_CameraDeviceStatus==ZKKER_CameraDeviceStatus::CAMERA_DEVICE_STATUS_ERROR || zKKER_CameraDeviceStatus==ZKKER_CameraDeviceStatus::CAMERA_DEVICE_STATUS_DISCONNECTED){  // return ::android::hardware::Return<void>();

    // }

    // if(zKKER_CameraDeviceStatus==ZKKER_CameraDeviceStatus::CAMERA_DEVICE_STATUS_CONNECTED){

    https://devops-jira.zeekrlife.com/secure/RapidBoard.jspa?rapidView=2466&projectKey=SNC8295&view=planning&selectedIssue=SNC8295-6395&quickFilter=7231&issueLimit=100

    https://devops-jira.zeekrlife.com/browse/SNC8295-6395

    command = ['ffprobe', '-show_frames', '-print_format', 'json', video_file]

    // auto end = std::chrono::system_clock::now();

    // auto duration = std::chrono::duration_cast<std::chrono::milliseconds>(end - start);

    // cout << "耗时：" << duration.count() << " 毫秒" << endl;

    // frame_count += duration.count();

    // std::this_thread::sleep_for(std::chrono::seconds(1));

    //模拟哨兵模式看30秒

    // this_thread::sleep_for(chrono::seconds(30));

    //一分钟之后，关闭AVM:,切换下一个

    while(1){

    if((chrono::duration_cast<chrono::seconds>(chrono::system_clock::now()- global_start_time)).count()>60){

    //关闭AVM:

    closeinput(inputId);

    break;

    }

    }

    提交代码反馈情况：

    1：我给陶工看了 推rgba 和不推rgba的情况，陶工说按照需求，不用提交rgba了；

    2：open(index.xml)文件，解析到前雾灯，其中的index =58 59 这个在代码中怎么体现？

    就是不注释xml 文件中的 前雾灯行不行？

    \## 常用账号密码



    | 网站服务器                       | 名称   | 账号     | 密码       |   |   |

    | ------------------------------------------------------- | -------- | ------------- | ---------------- | ---- | ---- |

    | samba                          |     | e-qiang.chen3 | 6J9xwJoWoZHG6o$t |   |   |

    | 10.136.137.97                      | 云堡垒机 | e-Qiang.Chen3 | 0537692@Hzw   |   |   |

    | https://hw-gerrit-dmz.zeekrlife.com           |     | e-qiang.chen3 | ZhLqgi6D8m    |   |   |

    |                             |     |        |         |   |   |

    | https://snc-gerrit.zeekrlife.com/admin/repos      |     |        |         |   |   |

    | http://10.114.198.13:3690/SNC_Cockpit/软件开发/Team/IVI | svn   | e_Qiang.Chen3 | 0537692@Hzw   |   |   |



    1：e-Qiang.Chen3

    e-qiang.chen3

    0537692@Hzw

    https://sre-cmdb.zeekrlife.com/#/wkf-form/execute/account/ramuser/5617 

    samba

    账号 : e-qiang.chen3 

    密码 : 6J9xwJoWoZHG6o$t

    10.136.137.97

    云堡垒机用户名密码

    https://jump.zeekrlife.com

    e-Qiang.Chen3

    0537692@Hzw

    SSH e-qiang.chen3@10.136.137.97:29992(zk-snc-full-build-rd-dev-ecs02)

    \\10.136.137.97\e-qiang.chen3

    账户：e-qiang.chen3

    密码：ZhLqgi6D8m

    https://hw-gerrit-dmz.zeekrlife.com

    https://snc-gerrit.zeekrlife.com/settings/

    buFNCm4jFawNEVRmdxspVPavp4Bv55gE/PNVki9Z+w

    https://hw-gerrit-dmz.zeekrlife.com/settings/

    SNMbfbTAfzwAFsMrWZhD4HeuQdig7IY1OCiunP9RNw

    CM2E交付分支（2024.7.16）：

    Android：

    ​    zeekr_repo init -u https://snc-gerrit.zeekrlife.com/a/all/manifests -b aptiv_develop_sa8295p_postcs1_268

    ​    zeekr_repo sync

    DC1E OS6.2交付分支（2024.8.27）：

    Android：

​    zeekr_repo init -u https://snc-gerrit.zeekrlife.com/a/all/manifests -b aptiv_develop_sa8295p_postcs1_270 -m 3rd.xml

​    zeekr_repo sync

编译：

cd test_device/lagvm/LINUX/android/

zeekr_build

source build/envsetup.sh

lunch zeekr_dhu-userdebug  （user版本 lunch zeekr_dhu-user）

export ZEEKR_PROJECT_NAME="ONEIMAGE-POSTCS1"

export PRODUCT_ZEEKR_VEHICLE_TYPE="ONEIMAGE-POSTCS1"

make

git代码仓库地址:

https://snc-gerrit.zeekrlife.com/admin/repos

SVN:

old_密码：4UeWwmc460

new_密码: 0537692@Hzw

个人登录 http://10.114.198.13:6060/adminPage/login 可以修改初始密码

用户名:e_Qiang.Chen3，  访问http://10.114.198.13:3690/SNC_Cockpit/软件开发/Team/IVI

new_pass:0537692@Hzw

 //zKKER_CameraDeviceStatus==ZKKER_CameraDeviceStatus::CAMERA_DEVICE_STATUS_ERROR ||

  // if(zKKER_CameraDeviceStatus==ZKKER_CameraDeviceStatus::CAMERA_DEVICE_STATUS_DISCONNECTED){

  //cout<<"camera disconnect"<<endl;

  // return ::android::hardware::Return<void>();

  //}

  // }

 // return ::android::hardware::Return<void>();

 // cout << "closeinput方法的 inputId=" << inputId << endl;

 // std::thread::id this_id = std::this_thread::get_id();

 //std::cout << "closeinput方法 线程id: " << this_id << '\n';

 //else if(strcmp(caseNo.c_str(),"case5 return 0;}

日常工作思考总结：

20241021 日报：

 1：入场办理，电脑领取，搭建环境

 2：按照公告 新员工入职向导 极客堡垒机申请，申请工作已完成，等通知；

 3：学习DHU需求文档；

 20241022 日报：

 1：学习DHU需求文档和网页文档

 2：网页系统相关权限都获取到了相关的访问权限

 3：配置samba，使window 和编译服务器 10.136.137.97:29992 实现文件共享

 4：MobaXterm 远程连接10.136.137.97 成功

 5： 腾讯会议 车载 Camera 代码流程讲解

 today work

 6：按照文档流程实现代码编译

 7：和杨文勇熟悉业务流程

 20241023 日报：

 1： 下载并且编译 

   DC1E OS6.2交付分支（2024.8.27）：

​    Android：

​    repo init -u https://snc-gerrit.zeekrlife.com/a/all/manifests -b aptiv_develop_sa8295p_postcs1_270

​    repo sync

   268分支和流程文档的编译过程中都出现过错误；

  today work

  和杨文勇熟悉业务流程；

  根据技术文档和需求文档 熟悉业务流程

   zeekr/android/platform/vendor/zeekr/interfaces/camera

   zeekr/android/platform/vendor/zeekr/interfaces/impl/camera

   zeekr/android/platform/vendor/zeekr/modules/cameradevicemanager

   zeekr/android/platform/vendor/zeekr/modules/soundrecorder

   zeekr/android/platform/vendor/zeekr/interfaces/carcameramanager

   zeekr/android/platform/vendor/zeekr/interfaces/impl/carcameramanager

  20241024 日报：

  1：阅读confirence 入职流程文档；查看Android 框架源码；

  2： 和杨文勇老师现场熟悉了 紧急录音，视频；自动泊车，停摆泊车，哨兵模式

  today work

   1：参考confurence入职流程文档 提交一个patch;

   2:申请 vendor/zeekr/interface（modules） 其他模块的代码，单独编译

   3：申请svn ：13：3690、IVI 权限

   4：熟悉JFrog刷机

   5： 编译自己的库 ，自己打印一些log,推到车机里面，跑起来。  

pwd: /home/e-qiang.chen3/snc-android/test_device/lagvm/LINUX/android

  20241025 日报：

  1：参考confurence入职流程文档 提交一个patch，已完成。没有caseId号码；

  2：申请 vendor/zeekr/interface（modules） 其他模块的代码，单独编译 ，其中 cameradevicemanager 单独编译报错，今天解决；

 3：申请svn ：13：3690、IVI 权限 已申请完成

   today work 

 1: cameradevicemanager 单独编译报错，今天解决

2：代码路径：vendor/zeekr/interfaces/impl/carcameramanager

  [8295DHU][IVI]CarCameraManager 注释密度提升

  20241026 日报：

  1、主线分支 zeekr_mainline_dev 的 CarCameraManager 编译通过

  2、参考 gerrit 提交 ，补充注释密度

vendor/zeekr/interfaces/impl/carcameramanager

  git branch

​    \* zeekr_release_sa8295p_postcs_ef_110

​    git checkout (-b) zeekr_mainline_dev 

​    git checkout  zeekr_mainline_dev 

​    cd  vendor/zeekr/interfaces/impl/carcameramanager

​    /home/e-qiang.chen3/snc-android/hlos_dev_la/lagvm/LINUX/android/vendor/zeekr/interfaces/impl/carcameramanager/1.0   cd /vendor/zeekr/interfaces/impl/carcameramanager/1.0

   mm -B

 2024年10月27日  周六

 2024年10月28日  周末

 2024年10月29日

  1： 下载并且编译 

   DC1E OS6.2交付分支（2024.8.27）：

​    Android：

​    repo init -u https://snc-gerrit.zeekrlife.com/a/all/manifests -b aptiv_develop_sa8295p_postcs1_270

​    repo sync

   268分支和流程文档的编译过程中都出现过错误；

   https://devops-confluence.zeekrlife.com/pages/viewpage.action?pageId=102184438

  zeekr_repo init -b zeekr_develop_sa8295p_postcs -m 3rd.xml

  zeekr_repo sync

zeekr_develop_sa8295p_postcs 分支:

cd test_device/lagvm/LINUX/android/

zeekr_build

source build/envsetup.sh

lunch zeekr_dhu-userdebug  （user版本 lunch zeekr_dhu-user）

lunch zeekr_dhu_sa8295-userdebug

export ZEEKR_PROJECT_NAME="ONEIMAGE-POSTCS1"

export PRODUCT_ZEEKR_VEHICLE_TYPE="ONEIMAGE-POSTCS1"

make

e-qiang.chen3@android:~/android_zeekr_develop_sa8295p_postcs/hlos_dev_la/lagvm/LINUX/android/build$ lunch

You're building on Linux

Lunch menu... pick a combo:

1. aosp_arm-eng
2. aosp_arm64-eng
3. aosp_blueline_car-userdebug
4. aosp_bonito_car-userdebug
5. aosp_bramble_car-userdebug
6. aosp_car_arm-userdebug
7. aosp_car_arm64-userdebug
8. aosp_car_x86-userdebug
9. aosp_car_x86_64-userdebug
10. aosp_cf_arm64_auto-userdebug
11. aosp_cf_arm64_phone-userdebug
12. aosp_cf_x86_64_foldable-userdebug
13. aosp_cf_x86_64_pc-userdebug
14. aosp_cf_x86_64_phone-userdebug
15. aosp_cf_x86_64_tv-userdebug
16. aosp_cf_x86_auto-userdebug
17. aosp_cf_x86_phone-userdebug
18. aosp_cf_x86_tv-userdebug
19. aosp_coral_car-userdebug
20. aosp_crosshatch_car-userdebug
21. aosp_flame_car-userdebug
22. aosp_oriole_car-userdebug
23. aosp_raven_car-userdebug
24. aosp_redfin_car-userdebug
25. aosp_sargo_car-userdebug
26. aosp_sunfish_car-userdebug
27. aosp_trout_arm64-userdebug
28. aosp_trout_x86-userdebug
29. aosp_x86-eng
30. aosp_x86_64-eng
31. arm_krait-eng
32. arm_v7_v8-eng
33. armv8-eng
34. armv8_cortex_a55-eng
35. armv8_kryo385-eng
36. atoll-userdebug
37. beagle_x15-userdebug
38. beagle_x15_auto-userdebug
39. car_ui_portrait-userdebug
40. car_x86_64-userdebug
41. cuttlestone_x86_64_phone-userdebug
42. cuttlestone_x86_phone-userdebug
43. db845c-userdebug
44. gsi_car_arm64-userdebug
45. gsi_car_x86_64-userdebug
46. hikey-userdebug
47. hikey64_only-userdebug
48. hikey960-userdebug
49. hikey960_tv-userdebug
50. hikey_tv-userdebug
51. msm8909-userdebug
52. msm8909go-userdebug
53. msm8996-userdebug
54. msmnile-userdebug
55. msmnile_au-user
56. msmnile_au-userdebug
57. msmnile_gvmq-user
58. msmnile_gvmq-userdebug
59. msmnile_tb-user
60. msmnile_tb-userdebug
61. pixel3_mainline-userdebug
62. poplar-eng
63. poplar-user
64. poplar-userdebug
65. qemu_trusty_arm64-userdebug
66. qssi-userdebug
67. sdk_car_arm-userdebug
68. sdk_car_arm64-userdebug
69. sdk_car_portrait_x86_64-userdebug
70. sdk_car_x86-userdebug
71. sdk_car_x86_64-userdebug
72. sdm845-userdebug
73. silvermont-eng
74. sm6150-userdebug
75. sm6150_au-user
76. sm6150_au-userdebug
77. uml-userdebug
78. yukawa-userdebug
79. yukawa_sei510-userdebug
80. zeekr_dhu_sa8295-user
81. zeekr_dhu_sa8295-userdebug
82. zeekr_dhu_sa8295_r-user
83. zeekr_dhu_sa8295_r-userdebug

out/soong/.bootstrap/soong-sdk

out/target/product/zeekr_dhu_sa8295/data/fuzz/arm64/vendor.zeekr.hardware.carcameramanager@1.0-vts.fuzzer/vendor.zeekr.hardware.carcameramanager@1.0-vts.fuzzer

zeekr_develop_sa8295p_postcs

这个分支上新建impl

///android_zeekr_develop_sa8295p_postcs/hlos_dev_la/lagvm/LINUX/android/vendor/zeekr/interfaces/

单独编译 /vendor/zeekr/interfaces/impl/carcameramanager

pwd: hlos_dev_la/lagvm/LINUX/android/vendor/zeekr/interfaces

cd .

pwd:

/vendor/zeekr/interfaces

mkdir -p impl

cd cd impl/

访问 ：https://snc-gerrit.zeekrlife.com/admin/repos

git clone url

/interfaces/impl/carcameramanager/1.0

ls

mm

MODIFY SNC8295-5484 [8295DHU][IVI] carcameramanager基础代码质量检查注释密度优化

Root cause: 代码注释密度低于20%了, 按照代码检测规定需要增加注释.

Solution: 按照代码检测规定需要增加注释.

Test suggest: 只增加注释, 没有更改代码, 无需测试.

test case: 无

git push origin HEAD:refs/for/zeekr_mainline_dev

git config --global core.autocrlf false 

git config --global core.autocrlf false 

2024年10月30日 日报

 代码编译测试没问题 提交；

 需求自动化测试

 [370500, 369789]

1、UserCase

1.1 DVR 一般录像主视角录制

1.2 DVR 一般录像全视角录制

1.3 DVR 紧急录像主视角录制

1.4 DVR 紧急录像全视角录制

1.5 DVR 泊车录像

\# 2、Black Box

\## 2.1 Architecture

zeek_native_dvr 模块 通过Audio模块获取原始的音频流pcm，经过MediaCodec编码后成ACC， 同时从AI_Camera 获取编码后的H265视频流，经Muxer合成

DVR的一般录像、紧急录像和泊车录像；这些mp4文件通过gallery 呈现，用户也可通过SystemUI 控制DVR的开启和关闭；

可以通过Vehicle hal 获取和接收 电源模式的变化来自动控制DVR的录制，获取水印信号的变化实时记录整车的运行状态；

| 1  | DVRManager    | 1、DVR 一般录像主视角录像2、 DVR 一般录像全视角录像3、 DVR 紧急录像主视角录像4、 DVR 紧急录像全视角录像5、 DVR 泊车录像6、 DVR 红外录像 |

| ---- | ----------------- | ------------------------------------------------------------ |

| 2  | StatusManager   | 1、从AI_Camera 获取和监听 ADCU Status 状态、camera 的link lock 和 video lock 状态、ADCU 的摄像头故障状态，控制DVR录制的启动和停止2、从CommonFwk 获取和监听 usb 的状态，控制DVR录制的启动和停止3、从Vehicle hal 获取和监听 整车的电源状态，控制DVR录制的启动和停止4、从Vehicle hal 或者 智驾someip 获取水印状态，转化成 水印icon的信息，供AI Camera 获取5、从CommonFwk 获取经纬度信息，提供给DVR 的文件索引6、DVR 功能开关状态、录音开关状态、分段时长状态、主视角和全视角切换状态、分辨率切换状态、紧急录像的触发事件、泊车录像的触发启停事件回复默认设置等状态的处理7、记忆状态的管理8、超级省电状态、无恒模式状态的处理9、异常状态的处理 （视频采集故障、录像失败、u盘无法写入，写入慢等） |

| 3  | ConfigManager   | 1、根据配置字（前后排、智驾、车型项目等）做平台化的适配2、项目配置化 |

| 4  | FileManager    | 1、DVR 索引文件的增删改查2、支持DVR mp4文件 创建、删除3、文件锁4、DVR初始化 usb 文件扫描5、文件目录空间的计算 |

| 6  | ProxyManager   | 1、对接Vehicle hal ，从Vehicle hal 获取和监听 状态变化2、对接LogMaster hal ,提供 埋点的接口给到 DVR 业务使用3、对接 Diag hal ,提供工厂产线的业务处理能力（例如 恢复出厂设置） |

| 7  | MemoryPoolManager | 1、提供内存池的能力                     |

| 8  | CodecManager   | 1、提供编码能力，支持音频编码                |

| 9  | MuxerManager   | 1、提供合成的能力，支持DVR一般录像主视角、全视角、DVR紧急录像主视角、全视角、DVR泊车录像的mp4的合成； |

| 10  | PermissionManager | 1、处理mic权限2、处理位置权限                |

| 11  | DVRService    | 1、对接AIDL接口，是外部调用的总入口             |

| 12  | CameraManager   | 1、从 AI Camera 获取 DVR 录制需要视频流，调用内存池的接口进行缓存，最终由DVRManager 写入u盘 |

zeekr_natvie_dvr 对 AI Camera 的需求

| index | 需求大类   | 需求item                           |

| ----- | ------------ | ------------------------------------------------------------ |

| 1   | 基本功能要求 | 1、提供 H265 每帧的 AMediaCodecBufferInfo 数据2、提供 H265 每帧的 对应的RGBA 数据，用于生成缩略图3、提供 H265 buffer 对应的AMediaFormat 信息4、ADCU camera 的故障状态，用于通知上层显示异常状态5、Video lock 和 link lock 状态，用于哨兵 开启和关闭状态处理6、getcameralistsize（需要真实的camera list）7、getCameraCharacteristics (需要当前项目camear 的信息) |

| 2   | 异常场景   | 1、当编码器异常的时候，通知到zeek_native_dvr2、当zeekr_native_dvr 收不到 mediaformat 的信息时，AI camera 需要做异常处理 |

\# 4、Class Definition

\# 4.1 Class A

4.1.1 Attribute 

4.1.2 Operations

\# 5、DataType Definition

\# 6、Sequence Diagrams

\# 7、 Resource Estimation

设计原因：

原先的CarCameraManger的 DVRManager 代码行数超过 4000行，包括了 DVR的一般录像、紧急录像和泊车录像，维护难度大

设计目的：

从 DVR 的业务进行拆分，便于后续的维护

设计说明（类层级）

ZeekrNativeDVR 

功能：AIDL接口实现

DVRManager

功能：DVR业务总入口

DVRGeneralRecoder

功能：DVR一般录像业务总入口，包括UNSVD前视角和全视角，

实现两路MP4CacheWritter缓存写入mp4（5s写一次，根据分段时长一共写1分钟、3分钟、5分钟）

DVREmergencyRecoder

功能：DVR紧急录像业务总入口，包括EVENT和AVM，

实现两路MP4CacheWritter缓存写入mp4（30s一次写完）

DVRParkRecoder

功能：DVR泊车录像业务总入口，包括PARK，

使用MP4CacheWritter实时写入mp4

MP4Writter

功能：MP4文件写入基类，封装muxer，mp4开始时间，

MP4RealtimeWritter

功能：继承MP4Writter，实时写入方案

MP4CacheWritter

功能：继承MP4Writter，缓存写入方案

CameraManager（暂定）

功能：管理Camera

Camera

功能：通过AI Camera获取H265编码数据

FrontViewCamera

功能：继承Camera，前视角H265编码数据

FullViewCamera

功能：继承Camera，全视角H265编码数据

InfraredCamera

功能：继承Camera，红外相机H265编码数据

AVMCamera

功能：继承Camera，泊车AVMH265编码数据

MemoryPool

功能：内存池，缓存5s、30s数据，单独设计

Memory

功能：内存基类

H265Memory

ACCMemory

功能：可选，音频内存

StatusManager

功能：对接VHAL，SomeIP，PowerStatus，MenuStatus等

AudioCodec

功能：音频编码器，ACC编码

TaskManager

功能：线程池处理Task

Task 功能：任务封装

Timer

功能：定时器，循环触发事件

IndexOperator

功能：更新info.txt

InnerIndexOperator

功能：更新Inner info.txt

FloderOperator

功能：创建、删除文件夹

WaterMarkManger

功能：水印信号管理，水印layout

ConfigManager

功能：Config，记忆状态等

FeatureSupport

功能：根据配置字，控制DVR功能

循环删除模块

当前CarCameraManager 当中存在的线程情况：

| index | 线程名称              | 创建此线程的原因 | 线程工作机制                         | 线程生命周期常驻/临时 | 备注                   |

| ----- | ----------------------------------- | ---------------- | ------------------------------------------------------------ | --------------------- | ----------------------------------------- |

| 1   | SentryManager::mSentryProcessThread |         | 哨兵录制线程                         | 临时         | 哨兵启动时创建线程，哨兵结束后销毁    |

| 2   | SentryManager::mDataProcessThread  |         | 数据处理线程                         | 临时         | 哨兵启动时创建线程，哨兵结束后销毁    |

| 3   | SentryManager::mThumnailThread   |         | 数据上传线程，供手机APP远程查看               | 临时         | 哨兵启动时创建线程，哨兵结束后销毁    |

| 4   | TaskManager::workers        |         | 队列线程池，由DVRManager向其中添加工作线程，用于一般录像和泊车录像缓存 | 常驻         |                      |

| 5   | DVRFileOperater::mWriteIndexThread |         | 写文件系统线程(DVR和哨兵)，更新infoIndex.txt，通知图库    | 临时 ？？？      | 跟随进程生命               |

| 6   | DVRFileOperater::mCheckSpaceThread |         | 检测存储空间                         | 临时         | DVR一般录制时启动线程，一般录像结束时释放 |

| 7   | DVRManager::mEncodeCaptureThread  |         |                               |            |                      |



| 8  | DVRManager::mDVREmRecordThread       |   | DVR紧急录制线程     | 临时 | 紧急录制时启动，紧急录制结束后销毁        |

| ---- | ------------------------------------------ | ---- | ------------------------ | ---- | ------------------------------------------------ |

| 9  | DVRManager::mDVRWriteLastOnceThread    |   | 一般录制时写尾帧数据线程 | 临时 | DVR一般录制时启动线程，一般录像结束时释放    |

| 10  | CarCameraManager::mVideoEncodeDaemonThread |   | 检测编码器线程      | 常驻 | 跟随进程生命                   |

| 11  | ZeekrCameraManager::mThreadVec       |   | 哨兵取流线程       | 临时 | 哨兵启动时创建线程，哨兵结束后销毁        |

| 12  | ZeekrCameraManager::mDvrCaptureThread   |   | DVR一般录像取流线程   | 临时 | DVR一般录像启动时创建线程，DVR一般录像结束后销毁 |

| 13  | ZeekrCameraManager::mDvrAvmCaptureThread  |   | AVM取流线程       | 临时 | 泊车录像启动时创建线程，泊车录像/哨兵结束时销毁 |

| 14  | DVRMenuStatus::hornMonitorThread      |   | 定时器线程        | 临时 | 汽车鸣笛时创建线程，鸣笛停止销毁         |

zeekr_natvie_dvr 需要的task

背景；1、因u盘的写入速率、usb2.0 和 usb 3.0 的写入 速率限制，以及 DVR 不同分辨率场景，多路并发写文件的场景 等 需要制定 DVR 写入策略和 海康u盘的写入性能指标，以及 异常处理；

一、视频写文件 和 性能指标 设计

当前写文件不同分辨率的场景

144W 1600X900

147W 1920X768

200W 1920X1080

600W 3840X1536

并发的最高负载

1、一路 一般录像前视 3840x1536

2、一路 一般录像周视 5760X2048

3、一路 紧急录像前视 3840X1536

4、一路 紧急录像周视 5760X2048

5、一路 泊车录像AVM 3840X1536

6、一般录像周视拆分场景 6路 同时写入 1920X1024X6

Usb 2.0 的写入速率（）

U盘的写入速率

综上信息 ，决策出 一般录像 

二、落盘优化方案设计

[[SNCABF8295-92631\] 【CS1E】【哨兵模式】【偶现】哨兵模式封面显示白屏 - Jira](https://devops-jira.zeekrlife.com/browse/SNCABF8295-92631)

哨兵生成缩略图后，缩略图缓存在操作系统的文件缓存中，尚未落盘，需要等操作系统统一进行落盘，但是CS1E的车型开关车门的时候会让U盘继电器掉电（省电策略），这个掉电就会导致U盘断电，自动卸载，导致原先在操作系统文件缓存中的缩略图没有落到U盘中，下次U盘上电挂载时，就会导致缩略图为空

Next: 需要安波福和U盘供电策略系统沟通一下，看是否有方案在U盘掉电前将文件缓存中的数据落盘。

背景：

1、由于DVR 内外置兼容设计，在8295 平台 针对文件的索引 沿用的外置DVR的 info.txt 的方案（即 8295 平台 内置DVR 和外置DVR 采用info.txt 进行哨兵和DVR的索引 ）

当前 info.txt 方案弊端

1、随着256G 、512G 以及1T的 大容量u盘 使用，增删改查 的耗时 增加

2、多路DVR的方案 使得 DVR 一般录像、紧急录像、泊车录像 的info.txt 更加臃肿

3、[[SNCABF8295-92524\] 【CS1E】【DVR】【偶现】正常录制视频界面停留在一般录像界面一段时间后视频全部不显示 - Jira](https://devops-jira.zeekrlife.com/browse/SNCABF8295-92524)

DVR的删除功能 和 新增 依赖文件锁 以及 行为同步

1、删除的功能执行时 需要拿到最新的info.txt 数据（缓存） ，然后再修改（同时更新缓存），再写入（先open 文件fd，清空文件，然后上锁，写入后解锁）；（此过程不能被其他的删除和新增打断）

2、新增的功能执行时，需要先拿到最新的info.txt 数据（缓存） ，然后再新增（排序，同时更新缓存），再写入（先open 文件fd，清空文件，然后上锁，写入后解锁）；（此过程不能被其他的删除和新增打断）

3、文件锁 需要先open之后，才能拿到fd，进行文件的上锁和解锁；

数据库的方案的优劣对比

优势：

劣势：

架构结合其他友商的情况，推荐 使用 数据库 进行存储； 

方案设计：

1、DVR

1.1 数据库的存储 u盘 和 ufs

1.2 数据表和字段

2、哨兵

2.1 数据库的存储 u盘 还是 ufs

2.2 数据表和字段 

1.1 哨兵录像存储

\# 2、Black Box

\## 2.1 Architecture

zeek_native_sentry 模块 从AI_Camera 获取编码后的H265视频流，实时缓存，当收到Vehicle hal 上报的报警事件时，sentry 合成 H265的视频流为Mp4，然后 通过gallery 呈现；

| 序号 | 模块名称     | 模块功能描述                         | comment    |

| ---- | ----------------- | ------------------------------------------------------------ | -------------- |

| 1  | SentryManager   | 1、哨兵录像的存储                      |        |

| 2  | StatusManager   | 1、从AI Camera 获取和监听 ADCU status 状态、Camera的link lock 、video link 状态，控制哨兵录制的开启和关闭状态2、从CommonFWK 获取和监听 usb的状态，控制哨兵的存储状态3、从CommonFWK 获取经纬度信息，提供给到 哨兵视频索引文件进行存储4、从 Vehicle hal 获取 哨兵alert 和 alarm 的触发事件 |        |

| 3  | ConfigManager   | 1、根据配置字（前后排、智驾、车型项目等）做平台化的适配   |        |

| 4  | FileManager    | 1、哨兵 索引文件的增删改查2、支持哨兵 mp4文件 创建、删除3、文件锁4、哨兵 初始化 usb 文件扫描5、文件目录空间的计算 |        |

| 5  | ProxyManager   | 1、对接Vehicle hal ，从Vehicle hal 监听 哨兵的报警 状态变化2、对接LogMaster hal ,提供 埋点的接口给到 DVR 业务使用3、对接 Diag hal ,提供工厂产线的业务处理能力（例如 恢复出厂设置） |        |

| 6  | MemoryPoolManager | 1、提供内存池的能力                     |        |

| 7  | MuxerManager   | 1、提供合成的能力，支持哨兵录像的mp4的合成；         |        |

| 8  | PermissionManager | 1、处理位置权限                       | 待确认是否需要 |

| 9  | SentryService   | 1、对接AIDL接口，是外部调用的总入口             |        |

| 10  | CameraManager   | 1、从 AI Camera 获取 DVR 录制需要视频流，调用内存池的接口进行缓存，最终由DVRManager 写入u盘 |        |

3.3 zeekr_natvie_sentry 对 AI Camera 的需求

| index | 需求大类   | 需求item                           |

| ----- | ------------ | ------------------------------------------------------------ |

| 1   | 基本功能要求 | 1、提供 H265 每帧的 AMediaCodecBufferInfo 数据2、提供 H265 每帧的 对应的RGBA 数据，用于生成缩略图3、提供 H265 buffer 对应的AMediaFormat 信息4、ADCU camera 的故障状态，用于通知上层显示异常状态5、Video lock 和 link lock 状态，用于哨兵 开启和关闭状态处理6、getcameralistsize（需要真实的camera list）7、getCameraCharacteristics (需要当前项目camear 的信息) |

| 2   | 异常场景   | 1、当编码器异常的时候，通知到zeek_native_sentry2、当zeekr_native_sentry 收不到 mediaformat 的信息时，AI camera 需要做异常处理 |

1、DVR 一般录像 video合成

1.1 Video Encoder 模块 实时缓存30秒的H264 数据

1.2 DVRManager 模块 每隔30秒取一次 缓存中的所有 H264 数据，通过Muxer写入，并且clear Video Encoder 中的缓存；

  以3分钟的固定时长为例，就循环取6次 30秒的视频，写入muxer，最后一次 写入muxer 后，stop muxer，生成最终的mp4 文件；

  以2分2秒的非固定时长为例，（非固定时长由用户手动触发DVR录制开关，暂停录制产生），循环取4次 30秒的视频，写入muxer，当点击录制按钮的关闭DVR的时候，将video encoder 中 最后缓存的H264 视频，最后一次 写入muxer 后，stop muxer，生成最终的mp4 文件；

2、DVR 一般录像 video 和 Audio 合成

3、哨兵 录像存储

3.1 、虹软算法H264数据回调处理： 缓存30s的H264数据，以链表头尾时间戳差计算30s。

3.2 、muxer合成： 收到哨兵信号， 从缓存copy一份30s的数据，并且将原缓存数据清空，然后等待1分钟后再一次将缓存数据一次性拷贝 muxer合成

4、DVR 文件索引同步算法

4.1、U盘插上 后读取DVR目录内部视频文件索引，组装json文件，组装的同时从旧的info.txt 中拷贝 经纬度信息，最终生成最新的json 以w+的模式写入到info.txt 文件中

Linux环境常用命令：

1. 查找文件或者内容：find /vendor –name *rtc*、grep –rin ‘key’ path
2. 杀进程：ps –A | grep android.hardware.media.c2@1.0-service-dolby | xargs kill
3. 生成md5： md5sum /mnt/androidwritable/dolby_libs/libcodec2_soft_dcxdec.so
4. 启动设置： am start -a android.settings.SETTINGS
5. 开关服务：

​		•    启动服务：setprop ctl.start bootanim

​		•    关闭服务： setprop ctl.stop bootanim

6. 开关selinux：setenforce 1/0
7. 切换owner：chown -r u0_a23:ext_data_rw apk
8. 更改读、写、执行权限： chmod a+x binary
9. 查看文本内容：head、tail、more、cat
10. 修改文本：vi、vim
11. 文件操作：copy、mv、delete、touch

Git常用仓库:

 zeekr/android/platform/vendor/zeekr/interfaces/camera

   zeekr/android/platform/vendor/zeekr/interfaces/impl/camera

   zeekr/android/platform/vendor/zeekr/modules/cameradevicemanager

   zeekr/android/platform/vendor/zeekr/modules/soundrecorder

   zeekr/android/platform/vendor/zeekr/interfaces/carcameramanager

   zeekr/android/platform/vendor/zeekr/interfaces/impl/carcameramanager

Git常用命令:

​	git status

​	git log 

​	git checkout branchA

​	git checkout -b branchA

​	git add -p

​	git add /path/*.

​	git add xxx.file

​	git add .

​	git commit 

​	git push origin HEAD:refs/for/zeekr_mainline_dev

​    git push origin HEAD:refs/for/zeekr_release_sa8295p_postcs_ef_110

​	git branch 

​	git branch -a 

​	git pull

​	git branch -vv

编译Android常用命令

cd test_device/lagvm/LINUX/android/

zeekr_build

source build/envsetup.sh

 lunch   

 lunch zeekr_dhu-userdebug  （user版本 lunch zeekr_dhu-user）

//代码提交规范

MODIFY SNC8295-5484 [8295DHU][IVI]carcameramanager基础代码质量检查注释密度优化

Root cause: 代码注释密度低于20%了, 按照代码检测规定需要增加注释.

Solution: 按照代码检测规定需要增加注释.

Test suggest: 只增加注释, 没有更改代码, 无需测试.

test case: 无

\# case 5

   os.system("adb shell ./vendor/bin/hw/cameramanagerextAutoTest closeinput")

  \# case 6

  os.system("adb shell ./vendor/bin/hw/cameramanagerextAutoTest opendmc")

  \# case 7

  os.system("adb shell ./vendor/bin/hw/cameramanagerextAutoTest closedmc")

  \# case 8

  os.system("adb shell ./vendor/bin/hw/cameramanagerextAutoTest openomc")

  \# case 9

  os.system("adb shell ./vendor/bin/hw/cameramanagerextAutoTest closeomc")

  \# case 10

  os.system("adb shell ./vendor/bin/hw/cameramanagerextAutoTest open_avm")

  \# case 11

  os.system("adb shell ./vendor/bin/hw/cameramanagerextAutoTest close_avm")

  \# case 12

  os.system("adb shell ./vendor/bin/hw/cameramanagerextAutoTest openavm1")

  \# case 13

  os.system("adb shell ./vendor/bin/hw/cameramanagerextAutoTest closeavm1")

  \# case 14

  os.system("adb shell ./vendor/bin/hw/cameramanagerextAutoTest opendvr")

  os.system("adb shell ./vendor/bin/hw/cameramanagerextAutoTest closedvr")

  \# case 15

  os.system("adb shell ./vendor/bin/hw/cameramanagerextAutoTest openpas3_101")

  \# case 16

  os.system("adb shell ./vendor/bin/hw/cameramanagerextAutoTest openpas3_102")

  \# case 17

  os.system("adb shell ./vendor/bin/hw/cameramanagerextAutoTest openpas3_103")

  \# case 18

  os.system("adb shell ./vendor/bin/hw/cameramanagerextAutoTest openpas3_104")

  \# case 19

  os.system("adb shell ./vendor/bin/hw/cameramanagerextAutoTest open_camera_mosaic")

  \# case 20

  os.system("adb shell ./vendor/bin/hw/cameramanagerextAutoTest openpas3mosaic_101")

  \# case 21

  os.system("adb shell ./vendor/bin/hw/cameramanagerextAutoTest openpas3mosaic_102")

  \# case 22

  os.system("adb shell ./vendor/bin/hw/cameramanagerextAutoTest openpas3mosaic_103")

  \# case 23

  os.system("adb shell ./vendor/bin/hw/cameramanagerextAutoTest openpas3mosaic_104")

  \# case 24

  os.system("adb shell ./vendor/bin/hw/cameramanagerextAutoTest openadcu_8")

  \# case 25

  os.system("adb shell ./vendor/bin/hw/cameramanagerextAutoTest openadcu_9")

  \# case 26

  os.system("adb shell ./vendor/bin/hw/cameramanagerextAutoTest openadcu_10")

  \# case 27

  os.system("adb shell ./vendor/bin/hw/cameramanagerextAutoTest openadcu_11")

  \# case 28

  os.system("adb shell ./vendor/bin/hw/cameramanagerextAutoTest openadcumosaic_8")

  \# case 29

  os.system("adb shell ./vendor/bin/hw/cameramanagerextAutoTest openadcumosaic_9")

  \# case 30

  os.system("adb shell ./vendor/bin/hw/cameramanagerextAutoTest openadcumosaic_10")

  \# case 31

  os.system("adb shell ./vendor/bin/hw/cameramanagerextAutoTest openadcumosaic_11")

  \# case 32

  os.system("adb shell ./vendor/bin/hw/cameramanagerextAutoTest startsafe_4")

  \# case 33

  os.system("adb shell ./vendor/bin/hw/cameramanagerextAutoTest startsafe_1")

  \# case 34

  os.system("adb shell ./vendor/bin/hw/cameramanagerextAutoTest startsafe_close")

#鱼眼校正
https://www.zywvvd.com/notes/study/camera-imaging/fisheye-cali/fisheye-cali/#%E7%95%B8%E5%8F%98%E7%9F%AB%E6%AD%A3

# Using an I2C infrared camera
https://www.yoctopuce.com/EN/article/using-an-i2c-infrared-camera


1. 相机简史 	https://blog.csdn.net/liujun3512159/article/details/124371792
2. 安卓相机架构概览 	https://blog.csdn.net/liujun3512159/article/details/124371977
3. 应用层 	https://blog.csdn.net/liujun3512159/article/details/124372917
4. 服务层 	https://blog.csdn.net/liujun3512159/article/details/124374440
5. 硬件抽象层 	https://blog.csdn.net/liujun3512159/article/details/124391598
6. 硬件抽象层实现 	https://blog.csdn.net/liujun3512159/article/details/124392153
7. 驱动层 V4L2框架	https://blog.csdn.net/liujun3512159/article/details/124393178
8. 高通KMD	https://blog.csdn.net/liujun3512159/article/details/124393277
9. 硬件层 	https://blog.csdn.net/liujun3512159/article/details/124416237
10. 安卓相机架构总结 	https://blog.csdn.net/liujun3512159/article/details/124416344
11. 手机相机的未来与发展 	https://blog.csdn.net/liujun3512159/article/details/124416367
12. https://blog.csdn.net/djfjkj52/article/details/137497593

https://docs.radxa.com/nio/nio12l/hardware-design/hardware-interface
硬件接口说明

<img width="2700" height="1738" alt="image" src="https://github.com/user-attachments/assets/e800cf6b-d5c8-4f3c-aa13-185573e53ba8" />

<img width="2700" height="1738" alt="image" src="https://github.com/user-attachments/assets/3ebb695c-d5b3-43d4-b052-5fc44e1978b3" />

Scrcpy投屏软件，下载需要配置环境变量，不配置默认在exe所在的文件夹上面执行cmd 。就可以打开投屏软件。
adb shell mount -o remount,rw /vendor /odm /system 
out/release/packages/ivi/system_z/system/lib64/libradioservice.z.so

Gerrrit常用命令:
git branch -a ,git branch -vv ;
git status
git log
git pull -r
git remote -v
git diff --cached
git rebase -i
git reset --hard HEAD~1
git branch -d 
gis stash
git stash
git checkout --.(重要)
chmod 777  -R ./
git rebase -i HEAD~2
git config --global core.editor vim

执行以下命令，配置hook
curl -Lo .git/hooks/commit-msg http:/xxx/hooks/commit-msg
chmod +x .git/hooks/commit-msg

丢弃修改，直接拉取新代码
repo sync -d
repo forall -c 'git reset --hard'repo forall -c 'git clean -f -d'
repo sync -c
git cherry-pick -x  commit Hash
周立功 ：
通道0:私有CAN
通道1 公共CAN
通道２ 公共CAN  
通道３:私有CAN



 




someipsd.entry.serviceid == 0xserviceId and someip.serviceid==0xserviceId


git push origin HEAD:refs/for/branch_name
git commit -m '
TicketNo:
Description:
Team:
Feature or Bugfix:
Change-Id: dfadffdasfsfadsfasdfasfhash
'
  //将别人提交到Gerrit中的代码 下载到本地
 git fetch http://chenq@gerrit_url refs/changes/数字/数字/1 && git cherry-pick FETCH_HEAD
 git cherry-pick --continue
 周立功ZcanPro ,CanOE
 git checkout -b local_branch  remote_branch/local_branch

 刷机/刷台架

 log 技巧
  setprop  Key Value ,  getprop  Key
   rm -rf /
   ps -A |grep 
   logcat |grep 
 MCU  AT 指令

https://chinese.alibaba.com/product-detail/MAX9296-GMSL-Camera-Board-Waveshare-Equipped-1601349270339.html   
 
https://blog.csdn.net/2301_77080582/article/details/144116584 

vsomeip.json
{
  "logging": {
    "level": "info",
    "console": "false",
    "syslog": {
      "enable": "true"
    }
  },
  "routing": "someipd",
  "services": [],
  "clients": [
    {
      "service": "27665",
      "instance": "1",
      "is_signal": "false",
      "initial_delay_min": "0",
      "initial_delay_max": "100",
      "repetitions_base_delay": "30",
      "repetitions_max": "3",
      "ttl": "3",
      "reliable": [
        "30501"
      ],
	  "strict-port": "true",
      "eventgroups": [
        {
          "eventgroup": "1"
        },
        {
          "eventgroup": "2"
        },
        {
          "eventgroup": "3"
        }
      ]
    }
  ]
}

someipd.json

{
  "unicast" : "192.168.40.7",
  "netmask" : "255.255.255.0",
  "active-if-status-checking": "false",
  "diagnosis" : "0x45",
  "diagnosis_mask" : "0xff00",
  "network" : "someip",
  "tls_version" : "TLS1_3_VERSION",
  "alg_Type" : 1,
  "work_mode" : 0,
  "logging" :
  {
    "level" : "info",
    "console" : "false",
    "file" : {"enable" : "false", "path" : "/tmp/someip.log", "size" : "10485760", "num" : "5"},
    "syslog" : { "enable" : "true" }
  },
  "enable_sched_rr" : "false",
  "applications" :
  [
      {
          "name" : "someipd",
          "id" : "0x1240",
          "max_dispatchers" : "8",
          "threads" : "8"
      },
      {
          "name" : "Huap",
          "id" : "0x1278",
          "max_dispatchers" : "1",
          "threads" : "2"
      },
      {
          "name" : "TBoxHal",
          "id" : "0x1343",
          "max_dispatchers" : "1",
          "threads" : "2"
      },
      {
          "name" : "AdsHal",
          "id" : "0x1355",
          "max_dispatchers" : "8",
          "threads" : "8"
      }
  ],
  "services" :
  [
      {
          "service" : "0x4009",
          "instance" : "0x0001",
          "reliable" : "30507"
      },
      {
          "service" : "0x8D0B",
          "instance" : "0x0001",
          "reliable" : "30507"
      },
      {
          "service" : "0x8D01",
          "instance" : "0x0001",
          "reliable" : "30507"
      }
  ],
  "clients" :
  [
      {
        "service" : "0x6809",
        "instance" : "0x0001",
        "reliable" : ["30501"]
      },
      {
        "service" : "0x6802",
        "instance" : "0x0001",
        "reliable" : ["30501"]
      },
      {
        "service" : "0x6803",
        "instance" : "0x0001",
        "reliable" : ["30501"]
      },
      {
        "service" : "0x6801",
        "instance" : "0x0001",
        "reliable" : ["30501"]
      },
      {
        "service" : "0x6801",
        "instance" : "0x0002",
        "reliable" : ["30501"]
      },
      {
        "service" : "0x6851",
        "instance" : "0x0001",
        "reliable" : ["30501"]
      },
      {
        "service" : "0x4010",
        "instance" : "0x0002",
        "reliable" : ["30501"]
      },
      {
        "service" : "0x6C03",
        "instance" : "0x0001",
        "reliable" : ["30501"]
      },
      {
        "service" : "0x6C0B",
        "instance" : "0x0001",
        "reliable" : ["30501"]
      },
      {
        "service" : "0x6C11",
        "instance" : "0x0001",
        "reliable" : ["30501"]
      },
      {
        "service" : "0x6C14",
        "instance" : "0x0001",
        "reliable" : ["30501"]
      },
      {
        "service" : "0x6C07",
        "instance" : "0x0001",
        "reliable" : ["30501"]
      },
      {
        "service" : "0x6C19",
        "instance" : "0x0001",
        "reliable" : ["30501"]
      },
      {
        "service" : "0x6C0A",
        "instance" : "0x0001",
        "reliable" : ["30501"]
      },
      {
        "service" : "0x6C16",
        "instance" : "0x0001",
        "reliable" : ["30501"]
      },
      {
        "service" : "0x6C0C",
        "instance" : "0x0001",
        "reliable" : ["30501"]
      },
      {
        "service" : "0x6C02",
        "instance" : "0x0001",
        "reliable" : ["30501"]
      },
      {
        "service" : "0x6C10",
        "instance" : "0x0001",
        "reliable" : ["30501"]
      },
      {
        "service" : "0x6C09",
        "instance" : "0x0001",
        "reliable" : ["30501"]
      },
      {
        "service" : "0x6C17",
        "instance" : "0x0001",
        "reliable" : ["30501"]
      },
      {
        "service" : "0x4010",
        "instance" : "0x0001",
        "reliable" : ["30501"]
      },
      {
        "service" : "0x8D07",
        "instance" : "0x0002",
        "reliable" : ["30501"]
      },
      {
        "service" : "0x4421",
        "instance" : "0x0001",
        "reliable" : ["30501"]
      },
      {
        "service" : "0x8D06",
        "instance" : "0x0001",
        "reliable" : ["30501"]
      },
      {
        "service" : "0x6501",
        "instance" : "0x0002",
        "reliable" : ["30514"]
      },
      {
        "service" : "0x6501",
        "instance" : "0x0001",
        "reliable" : ["30501"]
      },
      {
        "service" : "0x6407",
        "instance" : "0x0002",
        "reliable" : ["30514"]
      },
      {
        "service" : "0x6407",
        "instance" : "0x0001",
        "reliable" : ["30501"]
      },
      {
        "service" : "0x6406",
        "instance" : "0x0002",
        "reliable" : ["30514"]
      },
      {
        "service" : "0x6406",
        "instance" : "0x0001",
        "reliable" : ["30501"]
      },
      {
        "service" : "0x64A1",
        "instance" : "0x0002",
        "reliable" : ["30514"]
      },
      {
        "service" : "0x64A1",
        "instance" : "0x0001",
        "reliable" : ["30501"]
      },
      {
        "service" : "0x6408",
        "instance" : "0x0002",
        "reliable" : ["30514"]
      },
      {
        "service" : "0x6408",
        "instance" : "0x0001",
        "reliable" : ["30501"]
      },
      {
        "service" : "0x6306",
        "instance" : "0x0002",
        "reliable" : ["30514"]
      },
      {
        "service" : "0x6306",
        "instance" : "0x0001",
        "reliable" : ["30501"]
      },
      {
        "service" : "0x850E",
        "instance" : "0x0001",
        "reliable" : ["30501"]
      },
      {
        "service" : "0x4710",
        "instance" : "0x0001",
        "reliable" : ["30501"]
      },
      {
        "service" : "0x8D05",
        "instance" : "0x0001",
        "reliable" : ["30501"]
      },
      {
        "service" : "0x64A2",
        "instance" : "0x0002",
        "reliable" : ["30514"]
      },
      {
        "service" : "0x64A2",
        "instance" : "0x0001",
        "reliable" : ["30501"]
      },
      {
        "service" : "0x650C",
        "instance" : "0x0002",
        "reliable" : ["30514"]
      },
      {
        "service" : "0x650C",
        "instance" : "0x0001",
        "reliable" : ["30501"]
      },
      {
        "service" : "0x4701",
        "instance" : "0x0001",
        "reliable" : ["30501"]
      },
      {
        "service" : "0x4305",
        "instance" : "0x0001",
        "reliable" : ["30501"]
      },
      {
        "service" : "0x4303",
        "instance" : "0x0001",
        "reliable" : ["30501"]
      },
      {
        "service" : "0x4303",
        "instance" : "0x0002",
        "reliable" : ["30501"]
      },
      {
        "service" : "0x4303",
        "instance" : "0x0004",
        "reliable" : ["30501"]
      }
  ],
 "ssl-address": {
     "ssl-idu-address": ["192.168.40.26:30507"],
     "ssl-tbox-address": ["192.168.40.254:30507","192.168.40.254:41001","192.168.40.254:41002","192.168.40.254:41003"],
     "ssl-cdc-address": ["192.168.40.7:30507"],
     "ssl-zcu_r-address": ["192.168.40.1"],
     "ssl-zcu_l-address": ["192.168.40.2"]
 },
 "routing": "someipd",
 "service-discovery" :
 {
   "enable" : "true",
   "multicast" : "239.128.60.1",
   "port" : "30490",
   "protocol" : "UDP",
   "initial_delay_min" : "0",
   "initial_delay_max" : "100",
   "repetitions_base_delay" : "30",
   "repetitions_max" : "3",
   "ttl" : "3",
   "cyclic_offer_delay" : "1000",
   "request_response_delay_min" : "0",
   "request_response_delay_max" : "0"
  }
}

vsomeip_cm.json

{
  "applicationName": "/SoftwareComponent/AdaptiveApplicationSwComponentType/CSI_INI_GNSS_CDC/Process_CSI_INI_GNSS_CDC",
  "services": [
    {
      "service": "/Service/ServiceInterface/INI_GNSS",
      "serviceId": 27665,
      "protocolIdUsed": true,
      "majorVersion": 1,
      "minorVersion": 1,
      "events": [
        {
          "event": "gnssInfoRpt",
          "id": 9653,
          "dataType": "/DataType/StdCppImplDataType/ns/ini_gnss/GnssInfo",
          "eventId": 32769,
          "eventGroup": [
            1
          ],
          "reliable": true
        },
        {
          "event": "lbsInfoRpt",
          "id": 28070,
          "dataType": "/DataType/StdCppImplDataType/ns/ini_gnss/LbsInfo",
          "eventId": 32770,
          "eventGroup": [
            2
          ],
          "reliable": true
        },
        {
          "event": "gnssRawInfoRpt",
          "id": 22411,
          "dataType": "/DataType/StdCppImplDataType/ns/ini_gnss/GnssRawInfo",
          "eventId": 32771,
          "eventGroup": [
            2
          ],
          "reliable": true
        }
      ],
      "fields": [],
      "methods": [],
      "instances": [
        {
          "instance": "1",
          "isClient": true,
          "shortName": "/ServiceInstantiation/SOMEIPServiceInstantiation/SOMEIPServiceInstance/CSI_INI_GNSS_CDC",
          "vlan": "someip",
          "reliable": "30501",
          "unreliable": "30501",
          "network": "someip",
          "minorVersion": "1",
          "unicast": "192.168.40.7", //26
          "events": [
            {
              "id": 9653,
              "dataIds": []
            },
            {
              "id": 28070,
              "dataIds": []
            },
            {
              "id": 22411,
              "dataIds": []
            }
          ],
          "methods": [
            {
              "id": 27179,
              "dataIds": []
            }
          ],
          "fields": []
        }
      ]
    }
  ]
}



adb reboot bootloader
fastboot flash boot boot.img
fastboot reboot 











    


