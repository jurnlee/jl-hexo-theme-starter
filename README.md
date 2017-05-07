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
│   ├── layout.ejs  //名字固定，且为所有模板最外层，其余模板可选，Swig的则为layout.swig   
│   ├── page.ejs
│   ├── post.ejs
│   └── tag.ejs
├── source          //自动忽略隐藏文件与以下划线开头的文件除了(_data,_post)；其余则渲染生成或直接复制到public发布目录
│   ├── _data
│   ├── css
│   ├── fonts
│   ├── imgs
│   ├── js
│   └── vendor
└── scripts         //Hexo会自动加载该文件夹下所有的js格式的Hexo插件
```
### 需要插件
```
    "hexo-generator-archive": "^0.1.4",
    "hexo-generator-category": "^0.1.3",
    "hexo-generator-index": "^0.2.0",
    "hexo-generator-restful": "^0.2.0",
    "hexo-generator-tag": "^0.2.0",
    "hexo-renderer-ejs": "^0.3.0",
    "hexo-renderer-less": "^0.2.0",
    "hexo-renderer-marked": "^0.2.10",
```