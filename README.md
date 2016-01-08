# just_read  
[Visual Studioでデバッグ時にOpenCVのMat等の画像を表示できるプラグインが便利 ](http://whoopsidaisies.hatenablog.com/entry/2014/11/28/175637)  
[逆引きUNIXコマンド/topコマンドの出力をファイルに保存したい ](http://linux.just4fun.biz/%E9%80%86%E5%BC%95%E3%81%8DUNIX%E3%82%B3%E3%83%9E%E3%83%B3%E3%83%89/top%E3%82%B3%E3%83%9E%E3%83%B3%E3%83%89%E3%81%AE%E5%87%BA%E5%8A%9B%E3%82%92%E3%83%95%E3%82%A1%E3%82%A4%E3%83%AB%E3%81%AB%E4%BF%9D%E5%AD%98%E3%81%97%E3%81%9F%E3%81%84.html)  
[Taiwan Visa](http://web.roc-taiwan.org/jp/post/435.html)  
[description-configure-pkg](http://www.mike.org.cn/articles/description-configure-pkg-config-pkg_config_path-of-the-relations-between/)  

http://whoopsidaisies.hatenablog.com/entry/2013/12/07/135810#DescriptorMatcher

---------------------------------------------------------------------------------------------
#OpenCV-3.1.0 Install

    Ubuntu15.10 x64  Opencv3.1  
    
    apt-get update  
    apt-get upgrade  
    apt-get install libqt4-dev libopencv-dev build-essential cmake git libgtk2.0-dev pkg-config python-dev python-numpy libdc1394-22 libdc1394-22-dev libjpeg-dev libpng12-dev libtiff5-dev libjasper-dev libavcodec-dev libavformat-dev libswscale-dev libxine2-dev libgstreamer0.10-dev libgstreamer-plugins-base0.10-dev libv4l-dev libtbb-dev  libfaac-dev libmp3lame-dev libopencore-amrnb-dev libopencore-amrwb-dev libtheora-dev libvorbis-dev libxvidcore-dev x264 v4l-utils unzip   
    下载opencv3.1  wget https://github.com/Itseez/opencv/archive/3.1.0.zip
    下载完了 放在 /usr/local  
    用 unzip 解压刚才下载文件
    进入opencv-3.1.0  
    创建build
    进入 build 
    接下来 就开始干
    cmake -D CMAKE_BUILD_TYPE=RELEASE -D CMAKE_INSTALL_PREFIX=/usr/local -D WITH_TBB=ON -D WITH_V4L=ON -D WITH_QT=ON -D WITH_OPENGL=ON ..
    make -j $(nproc)
    make  install 
    /bin/bash -c 'echo "/usr/local/lib" > /etc/ld.so.conf.d/opencv.conf'
     ldconfig(这一步很重要)
    pkg-config --modversion opencv
    pkg-config --cflags opencv
