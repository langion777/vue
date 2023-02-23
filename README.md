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
computed，复杂的计算属性，直接在html写显得冗余，如

```javascript
var vm = new Vue({
  el: '#example',
  data: {
    message: 'Hello'
  },
  computed: {
    // 计算属性的 getter
    reversedMessage: function () {
      // `this` 指向 vm 实例
      return this.message.split('').reverse().join('')
    }
  }
})
```

watch，监听器，变量名加function，改变之后直接变值，如果一个值由多个变量决定，最好用computed

v-渲染html中的元素，新加的，用值来表示，for，if即可

其中data数据可动态显示。即更改后，在页面上也自动更改。这样处理，即创建不同的vue类从而达成组件化的效果
当然也可以通过v-once让其不变

### 模板
何为模板？首先需要了解何为DOM。dom是指将html文档当成一棵树，有节点的树。

每个节点可绑定至vue

### 一些好用的细节
直接用javascript

```html
{{hash + ga}}//双大括号即将vue数据显示到html的语法，同时可以计算值，原始数据使用v-html来
```

### 生命周期

人有少年中年老年，vue的对象也有不同的状态，但跟人随时间进入不同的阶段有区别，vue在于用户操作改变

```
var app = new Vue({
    el: '#app',
    data: {
      message: ''
    },
    created: function() {
      // 在 created 钩子函数中获取数据
      this.message = 'Hello, Vue!';
    }
  });
```

如此即可获取数据，作为初始化显示在html文件里