Read Me First
==============

How to build UnityROM-4.10 (Pure Edition) for OnePlus One

Install your Linux Distro

Setup Build Environment

sudo apt-get install  git-core gnupg flex bison gperf build-essential zip curl zlib1g-dev gcc-multilib g++-multilib libc6-dev-i386 lib32ncurses5-dev x11proto-core-dev libx11-dev lib32z-dev ccache libgl1-mesa-dev libxml2-utils xsltproc unzip bison build-essential curl flex git gnupg gperf libesd0-dev liblz4-tool libncurses5-dev libsdl1.2-dev libwxgtk2.8-dev libxml2 libxml2-utils lzop openjdk-7-jdk openjdk-7-jre pngcrush schedtool squashfs-tools xsltproc zip zlib1g-dev g++-multilib gcc-multilib lib32ncurses5-dev lib32readline-gplv2-dev lib32z1-dev flex bison ncurses-dev texinfo gcc gperf patch libtool automake g++ libncurses5-dev gawk subversion expat libexpat1-dev python-all-dev binutils-static libgcc1:i386 bc libcloog-isl-dev libcap-dev autoconf libgmp-dev build-essential gcc-multilib g++-multilib pkg-config libmpc-dev libmpfr-dev android-tools-adb android-tools-fastboot && sudo ln -s /usr/include/asm-generic /usr/include/asm; && sudo add-apt-repository ppa:webupd8team/java && sudo apt-get update && sudo apt-get install oracle-java8-installer && sudo update-java-alternatives -s java-8-oracle && sudo apt-get install oracle-java8-set-default && cd && mkdir ~/bin && PATH=~/bin:$PATH && mkdir -p ~/android/UR4 && curl https://storage.googleapis.com/git-repo-downloads/repo > ~/bin/repo && chmod a+x ~/bin/repo && cd ~/android/UR4


Setup CM Branch & get the roomservice.xml

git config --global user.email "your@email.com" && git config --global user.name "YourName" && cd ~/android/UR4 && repo init -u git://github.com/CyanogenMod/android.git -b cm-13.0 && mkdir -p ~/android/Ur4/.repo/local_manifests && curl -L -o .repo/local_manifests/roomservice.xml -O -L https://raw.github.com/LiquidSmokeX64/Guides-Scripts/master/roomservice.xml && cd ~/android/UR4

Sync up the Repo

cd ~/android/UR4 && repo init -u git://github.com/CyanogenMod/android.git -b cm-13.0 && mkdir -p ~/android/UR4/.repo/local_manifests && curl -L -o .repo/local_manifests/roomservice.xml -O -L https://raw.github.com/LiquidSmokeX64/Guides-Scripts/master/roomservice.xml && cd ~/android/UR4
cd ~/android/UR4 && repo sync --force-sync && cd ~/android/UR4

UnityROM-4 Commits...

cd ~/android/UR4 && repo init -u git://github.com/CyanogenMod/android.git -b cm-13.0 && mkdir -p ~/android/UR4/.repo/local_manifests && curl -L -o .repo/local_manifests/roomservice.xml -O -L https://raw.github.com/LiquidSmokeX64/Guides-Scripts/master/roomservice.xml && cd ~/android/UR4

cd ~/android/UR4 && repo sync --force-sync && cd ~/android/UR4/build/ && git fetch https://github.com/LiquidSmokeX64/android_build cm-13.0 && git cherry-pick 3929eef53258448b5161d8f923fa0b7309f5e8db && cd ~/android/UR4/packages/apps/Settings && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_Settings cm-13.0 && git cherry-pick ed4b9a0aee2271e29ba3dab6e567a83479ce5415 && cd ~/android/UR4/vendor/cm && git fetch https://github.com/LiquidSmokeX64/android_vendor_cm cm-13.0 && git cherry-pick b8319af13940205bd171becc96403f058352fa28 && cd ~/android/UR4/device/oneplus/bacon && git fetch https://github.com/LiquidSmokeX64/android_device_oneplus_bacon cm-13.0 && git cherry-pick d4cbfc721afb64fde6c60a157b411e7b08939b92 && cd ~/android/UR4/packages/apps/CMUpdater && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_CMUpdater cm-13.0 && git cherry-pick d646941ecf10c12c542d35eb9d3e4e82b513e127 && cd ~/android/UR4/packages/apps/CMUpdater && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_CMUpdater cm-13.0 && git cherry-pick da09f22163af7cf9f6bb501a3a1c23c313f957fb && cd ~/android/UR4/packages/apps/CMUpdater && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_CMUpdater cm-13.0 && git cherry-pick af505b604d81b8c99a815394bcb10d3ea421d1b6 && cd ~/android/UR4/packages/apps/CMUpdater && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_CMUpdater cm-13.0 && git cherry-pick 076b2742aeab9bdb63269e0da3474723b5a1fc8c && cd ~/android/UR4/packages/apps/CMUpdater && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_CMUpdater cm-13.0 && git cherry-pick 1c1ae1e0fe63786229fffbb450e463ff84cf40d3 && cd ~/android/UR4/packages/apps/CMUpdater && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_CMUpdater cm-13.0 && git cherry-pick 1ace6d6085b245b25b73bc7bf291cf49f02f96c6 && cd ~/android/UR4/packages/apps/CMUpdater && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_CMUpdater cm-13.0 && git cherry-pick e3f8a17e444980ede793752c6039544197c1b50c && cd ~/android/UR4/kernel/oneplus/msm8974 && git fetch https://github.com/LiquidSmokeX64/android_kernel_oneplus_msm8974 cm-13.0 && git cherry-pick d0e038398d7c8bdec758e6bb49eaf4c5267e84db && cd ~/android/UR4/device/oneplus/bacon && git fetch https://github.com/LiquidSmokeX64/android_device_oneplus_bacon cm-13.0 && git cherry-pick 1cf44922bf3c54d379943286f92c56f4682681c2 && cd ~/android/UR4/device/oneplus/bacon && git fetch https://github.com/LiquidSmokeX64/android_device_oneplus_bacon cm-13.0 && git cherry-pick 65eb004824d9884677097e84fdc0d7db75575b47 && cd ~/android/UR4/vendor/cm && git fetch https://github.com/LiquidSmokeX64/android_vendor_cm cm-13.0 && git cherry-pick c016b950fe3e180b3e740b21ba278ce489e8b74e && cd ~/android/UR4/vendor/cm && git fetch https://github.com/LiquidSmokeX64/android_vendor_cm cm-13.0 && git cherry-pick 03c11bac3d9181fd63b10e1f42f3da3bfa5ab414 && cd ~/android/UR4/vendor/cm && git fetch https://github.com/LiquidSmokeX64/android_vendor_cm cm-13.0 && git cherry-pick b32d4731a5413432efae65db37b9327bd7eb3eaa && cd ~/android/UR4/frameworks/base && git fetch https://github.com/sultanxda/android_frameworks_base cm-12.1 && git cherry-pick 0cbd4a88767d78640b7dd391674575f7d5e517e6 && cd ~/android/UR4/vendor/cm && git fetch https://github.com/LiquidSmokeX64/android_vendor_cm cm-13.0 && git cherry-pick 06cfb38be1dbcd89bb66b2cfc9c21ba082d88af8 && cd ~/android/UR4/vendor/cm && git fetch https://github.com/LiquidSmokeX64/android_vendor_cm cm-13.0 && git cherry-pick 31b7c97d6369a4d8ed183cbc9c809cf86edc310e && cd ~/android/UR4/build/ && git fetch https://github.com/LiquidSmokeX64/android_build cm-13.0 && git cherry-pick e5df7142c557b496ab53ef76619c7311908bb46d && cd ~/android/UR4/build/ && git fetch https://github.com/LiquidSmokeX64/android_build cm-13.0 && git cherry-pick 65172a51c2292e3dcc332ba18b5b02041879ee20 && cd ~/android/UR4/build/ && git fetch https://github.com/LiquidSmokeX64/android_build cm-13.0 && git cherry-pick 6480b9ac47dd5f051500ae99d438a4d69c4d1e9d && cd ~/android/UR4/device/oneplus/bacon && git fetch https://github.com/LiquidSmokeX64/android_device_oneplus_bacon cm-13.0 && git cherry-pick f3253dad248bd2b2d0b890b7bac8b02809118369 && cd ~/android/UR4/vendor/cm && git fetch https://github.com/LiquidSmokeX64/android_vendor_cm cm-13.0 && git cherry-pick c2d1a53d7756de0d0e015bb24be73fa9f59e0dd4 && cd ~/android/UR4/vendor/cm && git fetch https://github.com/LiquidSmokeX64/android_vendor_cm cm-13.0 && git cherry-pick 0fe4c3c137e972b43de32704b95e25fcf7edacd7 && cd ~/android/UR4 && cd ~/android/UR4/vendor/cm && git fetch https://github.com/LiquidSmokeX64/android_vendor_cm cm-13.0 && git cherry-pick ec93c2b01248f6aa719a2a2a71f906637ab8a1d1 && cd ~/android/UR4/vendor/cm && git fetch https://github.com/LiquidSmokeX64/android_vendor_cm cm-13.0 && git cherry-pick 217cd63638cb7bb93fbb809c73fe016acb3f1ad2 && cd ~/android/UR4/packages/apps/Settings && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_Settings cm-13.0 && git cherry-pick 1d09701ff06ad6dcf08292c8309358e667cd85b9 && cd ~/android/UR4/vendor/cm && git fetch https://github.com/LiquidSmokeX64/android_vendor_cm cm-13.0 && git cherry-pick 6fef644a3f7b4bbc8a9a83b5940aa1524e35c537 && cd ~/android/UR4/vendor/cm && git fetch https://github.com/LiquidSmokeX64/android_vendor_cm cm-13.0 && git cherry-pick ac99fa9aaff490443de044406c8208725caa6963 && cd ~/android/UR4/vendor/cm && git fetch https://github.com/LiquidSmokeX64/android_vendor_cm cm-13.0 && git cherry-pick 4075f1e0a756a9e07a274f8eb347fcfc27c3f006 && cd ~/android/UR4/build/ && git fetch https://github.com/LiquidSmokeX64/android_build cm-13.0 && git cherry-pick 1b05a411f66402623f0d82c5dd582e4e63bea457 && cd ~/android/UR4/vendor/cm && git fetch https://github.com/LiquidSmokeX64/android_vendor_cm cm-13.0 && git cherry-pick 15cb2e586372bded2fc24517b4917409250d93cb && cd ~/android/UR4/vendor/cm && git fetch https://github.com/LiquidSmokeX64/android_vendor_cm cm-13.0 && git cherry-pick 627809538ff60a7e5070e6aa898b4f446f1e98d3 && cd ~/android/UR4 && cd ~/android/UR4/device/oneplus/bacon && git fetch https://github.com/LiquidSmokeX64/android_device_oneplus_bacon cm-13.0 && git cherry-pick 6de4fbcf0d43b5d04c8ff46aed750719d7c06229 && cd ~/android/UR4/packages/apps/CMUpdater && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_CMUpdater cm-13.0 && git cherry-pick ecfd7788a14a87f48a64e4c884652db1d8411f1c && cd ~/android/UR4/packages/apps/Settings && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_Settings cm-13.0 && git cherry-pick 8f8e4da8270d6322380b125c3454bbd74275e306 && cd ~/android/UR4/packages/apps/AudioFX && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_AudioFX cm-13.0 && git cherry-pick c4b159da9c2b5a557b14b9e1d5999e5ed8cb32e8 && cd ~/android/UR4/packages/apps/BasicSmsReceiver && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_BasicSmsReceiver cm-13.0 && git cherry-pick 5799400aef8e24aa28b2e97b95feee1c18b763c8 && cd ~/android/UR4/packages/apps/Bluetooth && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_Bluetooth cm-13.0 && git cherry-pick c3863d95cd1d4ea34e8bc7fad6629b1901ead417 && cd ~/android/UR4/packages/apps/BluetoothExt && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_BluetoothExt cm-13.0 && git cherry-pick 3ca1b37007ad01c0049070bb471033004b463024 && cd ~/android/UR4/packages/apps/Browser && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_Browser cm-13.0 && git cherry-pick b98c0118f1d7b1a8d22f1407fe9e3193f189e8b1 && cd ~/android/UR4/packages/apps/Calendar && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_Calendar cm-13.0 && git cherry-pick 66a10853ea4dadfb714a0bfab666e33a305bfe59 && cd ~/android/UR4/packages/apps/Camera2 && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_Camera2 cm-13.0 && git cherry-pick 24ab2631e3f22ed4b1fdee4e73c786900c136d60 && cd ~/android/UR4/packages/apps/CarrierConfig && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_CarrierConfig cm-13.0 && git cherry-pick fb9cb77f8d5ba65850d0f306104b35a7ae00e8d0 && cd ~/android/UR4/packages/apps/CellBroadcastReceiver && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_CellBroadcastReceiver cm-13.0 && git cherry-pick fceb20942ab09cfa69a319358ab16999c9de9e47 && cd ~/android/UR4/packages/apps/CertInstaller && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_CertInstaller cm-13.0 && git cherry-pick 86c97afa4380fe5b5bd771bd850c3e1a27e43788 && cd ~/android/UR4/packages/apps/CMBugReport && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_CMBugReport cm-13.0 && git cherry-pick 30068d8aa91f5d404ff1f8d456eda34060ed871d && cd ~/android/UR4/packages/apps/CMFileManager && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_CMFileManager cm-13.0 && git cherry-pick f326c8d72f7be4c46c7c70fb9d6678d24a52728b && cd ~/android/UR4/packages/apps/CMWallpapers && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_CMWallpapers cm-13.0 && git cherry-pick 6b2a5f28f4d2dd34bc758917d187a226d6449337 && cd ~/android/UR4/packages/apps/Contacts && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_Contacts cm-13.0 && git cherry-pick b81111c76afe858549d41fe379cf75629052b889 && cd ~/android/UR4/packages/apps/ContactsCommon && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_ContactsCommon cm-13.0 && git cherry-pick 3ffb3c419ca60e999719b0cbf647c32593748166 && cd ~/android/UR4/packages/apps/DeskClock && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_DeskClock cm-13.0 && git cherry-pick afc5e64b85078c8b6d23b1f6447d51b82110baad && cd ~/android/UR4/packages/apps/Dialer && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_Dialer cm-13.0 && git cherry-pick a6d0e6248cd777562a15f2262ec2ae627c416655 && cd ~/android/UR4/packages/apps/Eleven && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_Eleven cm-13.0 && git cherry-pick 4218064f347d92c7147dd4f5787a72f1f4d510d0 && cd ~/android/UR4/packages/apps/Email && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_Email cm-13.0 && git cherry-pick bf6f079f9fc3c83c8a483f4f684f607cf0c8d568 && cd ~/android/UR4/packages/apps/ExactCalculator && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_ExactCalculator cm-13.0 && git cherry-pick 8c78fe40238d1304362a9129fe40d8cbdb39db44 && cd ~/android/UR4/packages/apps/Exchange && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_Exchange cm-13.0 && git cherry-pick c9fc783357390de292e65b85d3ed6f7b021a4055 && cd ~/android/UR4/packages/apps/FMRadio && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_FMRadio cm-13.0 && git cherry-pick ea202c7d6fdc6be85e3c3a1af8ea4b447f701b6c && cd ~/android/UR4/packages/apps/Gallery2 && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_Gallery2 cm-13.0 && git cherry-pick 163dbad7d3edb46c6a169d77f0069a8df5cfec93 && cd ~/android/UR4/packages/apps/HTMLViewer && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_HTMLViewer cm-13.0 && git cherry-pick 6bf012b36dc0c9bbf5653d42f6ecc6f7b5470b62 && cd ~/android/UR4/packages/apps/KeyChain && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_KeyChain cm-13.0 && git cherry-pick 6c2695ee3ec742d97877c21303a9b08c9560b72b && cd ~/android/UR4/packages/apps/LockClock && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_LockClock cm-13.0 && git cherry-pick 6964cd81a222c8a8e88614923a9c89077d02f1d7 && cd ~/android/UR4/packages/apps/ManagedProvisioning && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_ManagedProvisioning cm-13.0 && git cherry-pick 19edb54133d06e276e780667c9572adec179669f && cd ~/android/UR4/packages/apps/Messaging && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_Messaging cm-13.0 && git cherry-pick 013e71bdb31cbf6b63ab20d884cb0d33e0003588 && cd ~/android/UR4/packages/apps/Nfc && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_Nfc cm-13.0 && git cherry-pick f672ae5d39973aad767d28d3c1bb8508ad723e84 && cd ~/android/UR4/packages/apps/OneTimeInitializer && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_OneTimeInitializer cm-10.2 && git cherry-pick 2f09247fdfb80bb295adc109e1c1f7d8151c5f44 && cd ~/android/UR4/packages/apps/PackageInstaller && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_PackageInstaller cm-13.0 && git cherry-pick db4bdf4fa0663cae90af947c29bb1a3002bed4de && cd ~/android/UR4/packages/apps/PhoneCommon && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_PhoneCommon cm-13.0 && git cherry-pick f75b0e46cfefe4aa65b572fd3304b0dd4800480a && cd ~/android/UR4/packages/apps/Profiles && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_Profiles cm-13.0 && git cherry-pick 204858321d12456c60a8ca2530cab2a5b61c56dd && cd ~/android/UR4/packages/apps/Provision && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_Provision cm-13.0 && git cherry-pick ddfa959da0c2867f963545bed29c1bc7cd5da7ed && cd ~/android/UR4/packages/apps/Screencast && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_Screencast cm-13.0 && git cherry-pick 7af9e514109ea24a86f60155a422b227c021b889 && cd ~/android/UR4/packages/apps/SetupWizard && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_SetupWizard cm-13.0 && git cherry-pick 9e5f3478c999ea6c2183a86492121bed33edfc2e && cd ~/android/UR4/packages/apps/SoundRecorder && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_SoundRecorder cm-13.0 && git cherry-pick e13f206946b2f2b24cbdbdaccf65dec3e106699e && cd ~/android/UR4/packages/apps/SpeechRecorder && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_SpeechRecorder cm-13.0 && git cherry-pick 6f9ff9944259a3df77ab1df64cb9a80ba5010e4c && cd ~/android/UR4/packages/apps/Stk && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_Stk cm-13.0 && git cherry-pick d98ae2d1242f79da674d0f69ef5714a2908b7bf5 && cd ~/android/UR4/packages/apps/Tag && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_Tag cm-13.0 && git cherry-pick e3b0faa28bce471c67d22125a37cc6471b02e41a && cd ~/android/UR4/packages/apps/Terminal && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_Terminal cm-13.0 && git cherry-pick a14c0b5c1dd79013d69248081b0e2ce31785642b && cd ~/android/UR4/packages/apps/ThemeChooser && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_ThemeChooser cm-13.0 && git cherry-pick 2b9dca9bc2545a4f288d65325d9bd5236c6a8be8 && cd ~/android/UR4/packages/apps/Trebuchet && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_Trebuchet cm-13.0 && git cherry-pick 0d2e0f8b22829d13a045e9ae597425e004921217 && cd ~/android/UR4/packages/apps/TvSettings && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_TvSettings cm-13.0 && git cherry-pick e0c0ed968d5f70127c33b0d70928037e69749115 && cd ~/android/UR4/packages/apps/TvSettings && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_TvSettings cm-13.0 && git cherry-pick 24c2717be094bb734bd9be8bdfd79471b26c54c4 && cd ~/android/UR4/packages/apps/UnifiedEmail && git fetch https://github.com/LiquidSmokeX64/android_packages_apps_UnifiedEmail cm-13.0 && git cherry-pick a1a4b48d09db698e429b2e00564ce7b57c7c2452 && cd ~/android/UR4

Build ROM and/or Kernel NOW

cd ~/android/UR4 && make clean && export USE_CCACHE=1 && source build/envsetup.sh && breakfast bacon && croot && make bootimage

cd ~/android/UR4 && make clean && export USE_CCACHE=1 && source build/envsetup.sh && breakfast bacon && croot && brunch bacon

ENJOY.
