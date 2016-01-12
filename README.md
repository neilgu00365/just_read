# just_read  
[Visual Studioでデバッグ時にOpenCVのMat等の画像を表示できるプラグインが便利 ](http://whoopsidaisies.hatenablog.com/entry/2014/11/28/175637)  
[逆引きUNIXコマンド/topコマンドの出力をファイルに保存したい ](http://linux.just4fun.biz/%E9%80%86%E5%BC%95%E3%81%8DUNIX%E3%82%B3%E3%83%9E%E3%83%B3%E3%83%89/top%E3%82%B3%E3%83%9E%E3%83%B3%E3%83%89%E3%81%AE%E5%87%BA%E5%8A%9B%E3%82%92%E3%83%95%E3%82%A1%E3%82%A4%E3%83%AB%E3%81%AB%E4%BF%9D%E5%AD%98%E3%81%97%E3%81%9F%E3%81%84.html)  
[Taiwan Visa](http://web.roc-taiwan.org/jp/post/435.html)  
[description-configure-pkg](http://www.mike.org.cn/articles/description-configure-pkg-config-pkg_config_path-of-the-relations-between/)  

[OpenCVで画像の特徴抽出・マッチングを行う](http://whoopsidaisies.hatenablog.com/entry/2013/12/07/135810#DescriptorMatcher)  
[OpenCV3.0.0-alphaの特徴抽出・マッチングまとめ](http://whoopsidaisies.hatenablog.com/entry/2014/08/20/200215)  
[OpenCV 3.1.0-dev Document](http://docs.opencv.org/master/pages.html#gsc.tab=0)  
[About Ransac](http://ramsrigoutham.com/tag/ransac/)  
[Common Interfaces of Descriptor Matchers](http://docs.opencv.org/2.4/modules/features2d/doc/common_interfaces_of_descriptor_matchers.html#descriptormatcher-create)  
[画像局所特徴量と特定物体認識 - SIFTと最近のアプローチ -](http://www.vision.cs.chubu.ac.jp/cvtutorial/PDF/02SIFTandMore.pdf)  
[AKAZE and ORB planar tracking](http://docs.opencv.org/master/dc/d16/tutorial_akaze_tracking.html#gsc.tab=0)  
[Panorama – Image Stitching in OpenCV](http://ramsrigoutham.com/tag/ransac/)  
[Features2D + Homography to find a known object](http://docs.opencv.org/2.4/doc/tutorials/features2d/feature_homography/feature_homography.html)  
[ORBを用いて特徴点のマッチングを行う(ORB説明)](http://homepage3.nifty.com/ishidate/opencv_11/opencv_11.htm)  
[OpenCV中feature2D学习——ORB和BruteForceMatcher ](http://blog.csdn.net/holybin/article/details/48776949)  
[OpenCV中feature2D学习——FAST特征点检测与SIFT/SURF/BRIEF特征提取与匹配 ](http://blog.csdn.net/holybin/article/details/44778747) [二枚のカメラ画像から基礎行列を求めるのは難しい](http://homepage3.nifty.com/ishidate/opencv_19/opencv_19.htm)  
[A Study on an Obstacles Detection System Employing a Car-mounted Camera(Camera ego-estimation)](https://ds.lib.kyutech.ac.jp/dspace/bitstream/10228/5313/1/D-231_kou_k_371.pdf)  
[BundlerによるStructure from MotionでKAZE局所特徴量を使ってみた](http://daily.belltail.jp/?p=1387)  
[A-KAZE github](https://github.com/pablofdezalc/akaze)  
[ORB使ってみた(ORBと比較&code)](http://pukulab.blog.fc2.com/blog-entry-41.html)  
[ORBでホモグラフィー行列推定](http://pukulab.blog.fc2.com/blog-entry-59.html)　　
[カメラキャリブレーションと3次元再構成](http://opencv.jp/opencv-2svn/cpp/camera_calibration_and_3d_reconstruction.html#cv-findhomography)  
[Camera Calibration and 3D Reconstruction](http://docs.opencv.org/2.4/modules/calib3d/doc/camera_calibration_and_3d_reconstruction.html?highlight=findhomography)  
[]()






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
