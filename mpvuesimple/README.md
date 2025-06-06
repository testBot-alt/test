
## 基本用法
``` bash
$ npm install
$ npm run dev
```

# 目录结构
```
|____build              webpack打包的环境代码
|____config             webpack打包的配置文件
|____node_modules       项目运行依赖的npm包
|____src                项目代码文件夹
 |__components          自定义公用组件
 |__pages               页面组件
 |__plugins             vue插件
   |__index.js          vue插件的注册，包含接口请求及工具utils
   |__utils             工具类及共用方法
 |__router              小程序的page.json的配置
  |__flyio          
   |__apiUrl            接口请求地址管理
   |__config            接口请求配置管理
   |__interceptors.js   接口请求拦截器
   |__request           接口请求封装（包括loading及toast，接口的定制化配置及默认配置)
  |__modules            store的管理文件
  |__index.js           实现store对modules文件下的自动注册
 |__store               vuex状态管理
 |__App.vue             小程序的App页面
 |__main.js             小程序插App入口的配置
 |__template.js         小程序插页面入口的配置
 |__app.json            小程序app.json的配置
|____static             静态资源文件夹
|____.babelrc           es6语法转换配置文件
|____.editorconfig      编辑器配置
|____.eslintignore      eslint的忽略配置
|____.eslintrc.js       eslint配置
|____.gitignore         git push忽略配置
|____.postcssrc.js      postcss插件的配置文件
|____index.html         SPA的index页面
|____package.json       npm包配置文件
|____README.md          readme文档

```

# 踩坑攻略
1.使用'cover-view'标签在视频播放时保持显示，最外层一定要使用fixed定位
2.使用'cover-view'标签内嵌入'button'按钮, 'button'内一定要再嵌入一个'cover-view'或者'cover-image'
3.在vue页面中使用'button'按钮时，最好加上nf-get-form-id组件，该组件会遇到插槽数据渲染问题，具体参照URL_ADDRESS3.在vue页面中使用'button'按钮时，最好加上nf-get-form-id组件，该组件会遇到插槽数据渲染问题，具体参照https://github.com/Meituan-Dianping/mpvue/issues/427
4.使用'cover-view'标签内嵌入'button'按钮, 'button'内一定要再嵌入一个'cover-view'或者'cover-image'
