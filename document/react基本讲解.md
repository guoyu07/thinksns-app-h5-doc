# 用es6语法创建一个component
其实很简单，
app.js
```jsx
import React, {Component} from 'react';

class App extends Component {
  constructor(props) {
    super(props);
    // TODO...
    // 本函数非必要，相当于构造方法，这里列举下，在实际中，可以忽略这个函数
  }

  // 整个包中必须存在的函数
  render() {
    return (
      <div>
        todo...
      </div>
    );
  }

}

export default App;
```
这样，就完成了一个最简单的react包文件

现在，我们看看怎么用

index.js
```jsx
import React from 'react';
import ReactDOM from 'react-dom';
import App from './app.js';

ReactDOM.render(
    <App />,
    document.getElementById('app')
);
```
你一定好奇，这个`document.getElementById('app')`哪里来的，我们看看基础的html吧
```html
<!DOCTYPE html>
<html>
  <head>
    <title>react</title>
  </head>
  <body>
    <div id='app'></div>
    <script type="text/javascript" src="app.js"></script>
  </body>
</html>
```
在html中的app.js是编译后的文件，并非jsx文件哈。

这就是最基本的react＋es6语法，所有的控制器都是基于这个语法的基础上而写出来的component，然后将这些组件嵌套在一起，组成一个完整的前端app。
