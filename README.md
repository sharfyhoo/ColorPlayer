## ColorPlayer
一款基于NodeJs的命令行在线音乐播放器，目前支持网易云音乐的播放。

## 软件界面
- 榜单列表                       
![榜单列表](https://raw.githubusercontent.com/arrowing/ColorPlayer/master/interfaces/top_list.png "榜单列表")

- 歌曲列表                      
![歌曲列表](https://raw.githubusercontent.com/arrowing/ColorPlayer/master/interfaces/music_list.png "歌曲列表")

## 使用须知
下载代码后，在其根目录下执行npm link，将会创建一个cPlayer命令，然后就可以启动该播放软件了。
> **cPlayer**

## 全局变量与驱动问题

请确保您已安装SoX音频工具，下载地址是：http://sox.sourceforge.net/        
安装完SoX后，将其目录放置PATH中。

## 驱动设置：

Windows：（先再全局环境里添加，然后在cmd下输入set AUDIODRIVER=waveaudio即可。）                
set AUDIODRIVER=waveaudio

其他：（从上到下依次设置，无效再用下一个，我没测试过）
- set AUDIODRIVER=oss
- set AUDIODEV=/dev/dsp2
- set AUDIODEV=hw:0

#### 注意事项（限于windows环境）
Windows下还需要将SoX目录下的sox.exe拷贝到play.exe与rec.exe
- copy sox.exe soxi.exe
- copy sox.exe play.exe
- copy sox.exe rec.exe

然后还需要下载2个dll，名字分别为libmp3lame-0.dll和libmad-0.dll，这样子才可以播放音乐。               
由于微软版权关系，SoX没直接提供这2个dll文件，需要自行用VS编译，不过可以在网络上下载得到。
