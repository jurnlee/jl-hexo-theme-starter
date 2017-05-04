# jl-hexo-theme-starter
learning to custom my own Hexo theme step by step.

## step0 preparation 

1. 学习Hexo主题文件结构及其基本关系   
2. 学习Hexo主题配置及命令   
3. 学习EJS语法及其特点  

### 主题结构 
Hexo主题的结构大体如下：(ejs为例)  

```
./
├── _config.yml   
├── readme.md 
├── LICENSE
├── package.json (可选)
├── languages   
│   ├── default.yml  
│   └── xx.yml
├── layout          //主题的模板文件，默认支持Swig，安装插件支持ejs, Haml, Jade, Pug
│   ├── _partials
│   ├── archive.ejs
│   ├── category.ejs
│   ├── index.ejs
│   ├── layout.ejs  //名字固定，且为所有模板最外层，Swig的则为_layout.swig   
│   ├── page.ejs
│   ├── post.ejs
│   └── tag.ejs
├── source          //asset文件，自动忽略隐件与以下划线开头的文件；渲染生成或直接复制到public文件夹
│   ├── _data
│   ├── css
│   ├── fonts
│   ├── imgs
│   ├── js
│   └── vendor
└── scripts         //Hexo会自动加载该文件夹下所有的js文件
```
