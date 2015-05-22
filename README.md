# repo

用来解决国内用户被 GFW 墙掉无法导致的repo init 失败问题
使用方法：

    repo init --repo-url git://github.com/yun-percy/repo.git -u git://github.com/CyanogenMod/android.git -b cm-12.0 --no-repo-verify
    
方法来自 百度rom团队。向他们致敬

# repo sync 被墙

现在各个repo都开始将公共的代码直接指向了google的源，来避免每次都需要去同步google的源代码，但是，这就苦了我们这些墙内人的码农了，简直卧槽了得。

其实只需要将 .repo/manifests里面的

        <remote name="aosp"

下面fetch的内容改为面的地址即可

           fetch="git://Android.git.linaro.org/" />
