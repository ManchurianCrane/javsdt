# JAV-Scraper-and-Rename-local-files
收集jav元数据，并规范本地文件（夹）的格式。  
python3.7  使用pyinstaller打包成exe。
[exe下载：](https://github-production-release-asset-2e65be.s3.amazonaws.com/199952692/67614c00-1071-11ea-8c3a-a1e536c53052?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAIWNJYAX4CSVEH53A%2F20191126%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20191126T092836Z&X-Amz-Expires=300&X-Amz-Signature=9cc87b4a529b5ddc8b19bc5c883a55055b7e70c219c5594233658baf0cb9d89a&X-Amz-SignedHeaders=host&actor_id=44168897&response-content-disposition=attachment%3B%20filename%3DV1.9.7.JAV.For.Emby.Kodi.Jellyfin.zip&response-content-type=application%2Foctet-stream)

工作流程：  
1、用户选择文件夹，遍历路径下的所有文件。  
2、文件是jav，取车牌号，到javXXX网站搜索影片找到对应网页。  
3、获取网页源码找出“标题”“导演”“发行日期”等信息和DVD封面url。  
4、重命名影片文件。  
5、保存信息写入nfo。  
6、下载封面url作fanart.jpg，裁剪右半边作poster.jpg。  
7、重命名文件夹。  

目标效果：  
![image](https://github.com/junerain123/Collect-Info-and-Fanart-for-JAV-/blob/master/images/1.png)  
![image](https://github.com/junerain123/Collect-Info-and-Fanart-for-JAV-/blob/master/images/2.png)  
![image](https://github.com/junerain123/Collect-Info-and-Fanart-for-JAV-/blob/master/images/3.png)  

以下为ini中的用户设置：  

[收集nfo]  
是否收集nfo？ = 是  
是否跳过已存在nfo的文件夹？ = 否  

[重命名影片]  
是否重命名影片？ = 是  
重命名影片的格式 = 车牌  
  
[修改文件夹]  
是否重命名或创建独立文件夹？ = 否  
新文件夹的格式 = 【+全部女优+】+车牌  

[获取两张jpg]  
是否获取fanart.jpg和poster.jpg？ = 是  

[kodi专用]  
是否收集女优头像 = 否  

[emby服务端]  
网址 = http://localhost:8096/  
api id = 12345678  

[其他设置]  
javlibrary网址 = http://www.x39n.com/cn/  
javbus网址 = https://www.buscdn.work/  
素人车牌(若有新车牌请自行添加) = MIUM、NTK、ARA、GANA、LUXU、DCV、MAAN、HOI、NAMA、SWEET、SIRO、SCUTE、CUTE、SQB  
扫描文件类型 = mp4、mkv、avi、wmv、iso、rmvb、m2ts  

[百度翻译API]  
是否需要日语简介？ = 是  
是否翻译为中文？ = 是  
app id = 20190723000320508  
密钥 = KLstKvVtFnfusg_ArQ8L  

[百度人体检测]  
是否需要准确定位人脸的poster？ = 否  
appid =   
api key =   
secret key =   
  
