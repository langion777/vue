## 自带的命令

### Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

## 搭建一个vue
在命令行输入 vue create yourname
注意package.json文件
出问题可npm audit fix --force
npm为node管理包，audit为审计，即自动更新

### vue思想
谈vue的前提要明白vue是一个前端框架，为了解决如何前后端交互即数据、以及前端显示效率问题

核心在于一个vue类，里面含有：
data，可用数组、字符串内容，为一个数组
methods，即点击按钮后返回的函数，在里面更改vue类中data数据即可显示在页面上

v-渲染html中的元素，新加的，用值来表示，for，if即可