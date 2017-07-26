# Que.js

## Que is a useful and elegant frontend framework.

摒弃浮华，回归真我。

脱去外衣以后，前端还剩下什么。

世界变化很快，加班越来越久。

学习技术有心无力？

没关系，你还有Que。


### Documentation

Coming soon.


### Examples

#### index.html
```html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Que.js</title>
</head>
<body>

<div id="que-app">
    <p>Que.js is better than {{framework}}.</p>
    <input type="text" q-model="framework" />
    <button q:click="randomFramework">RandomFramework</button>
</div>
```

</body>
</html>

#### index.js

```javascript
import Que from 'que'

const frameworks = ['backbone', 'angular', 'ember', 'react', 'vue']

const que = new Que({
  props: {
    framework: 'vue'
  },
  reducers: {
    randomFramework: function (e) {
      let framework = frameworks[parseInt(Math.random() * frameworks.length)]
      while (this.framework === framework) {
        framework = frameworks[parseInt(Math.random() * frameworks.length)]
      }
      this.framework = framework
    }
  }
})

que.render('#que-app')
```
