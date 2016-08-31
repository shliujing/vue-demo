# README

Learn form: http://www.runoob.com/w3cnote/vue-js-quickstart.html

## 1

双向绑定
```
{{ message }}

new Vue({
        el:'#app',
        data: {
            message:'Hello World!'
        }
    });
```

## 2

同[1](#1)，实时变化
```
{{ message }}

new Vue({
  el: '#app',
  data: {
    message: '我会变动!'
  }
})

```

## 3

列表循环
```
<li v-for="todo in todos">
  {{ todo.text }}
</li>

or    {{ parentMessage }} - {{ $index }} - {{ item.message }}

new Vue({
  el: '#app',
  data: {
    todos: [
      { text: 'Learn JavaScript' },
      { text: 'Learn Vue.js' },
      { text: 'Build Something Awesome' }
    ]
  }
})
```


## 4

判断
```
<div v-if="Math.random() > 0.5">
  随机数大于 0.5
</div>
<div v-else>
  随机数不大于 0.5
</div>

new Vue({
  el: '#app'
})
```

## 5

过滤器，类似Linux的管道传输

```
{{message | reverse | uppercase}}

Vue.filter('reverse', function (value) {
    return value.split('').reverse().join('')
})
new Vue({
  el: '#app',
  data: {
      message:'www.iamlj.com'
  }
})
```