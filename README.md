git clone https://github.com/xiaowubangbangbang/vue-core-video-player.git

cd vue-core-video-player 
//导入依赖
npm install 
//运行
npm run serve
//打包
npm run build 

打包之后可以丢进nginx运行,将打包好的dist内容替换nginx目录下html内容,配置监听,启动nginx

修改/html/static/data.js可以动态修改数据
本地视频源放在/html/static/vedio下
新增一个视频
{
  id: '视频id',
  title: '标题',
  author: '作者',
  date: '日期',
  decs: "描述",
  link: '地址',
  cover: '缩略图',
  cover2: '缩略图',
  cover3: '缩略图',
  source: [
    {
     src: '360P的视频源',
     resolution: 360,
   }, {
     src: '720P的视频源',
     resolution: 720,
   }, {
     src: '1080P的视频源',
     resolution: 1080
   }
 ],
  duration: '视频时长'
}

//如果不需要多个清晰度 将source:[]替换成source:'视频源'




本项目是基于 https://github.com/core-player/vue-core-video-player-examples 更改 
源代码:https://github.com/core-player/vue-core-video-player-examples

