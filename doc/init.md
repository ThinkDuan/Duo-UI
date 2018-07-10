## 初始化目录
1. 把src目录改变为examples目录,原src目录，改成 examples 用作示例展示
2. 新增 packages 用于写存放组件,
3. 我们需要再把我们webpack配置文件稍作一下调整，首先是把原先的编译指向src的目录改成examples
4. 为了 npm run build 能正常编译 packages 我们也需要为 babel-loader 再增加一个编译目录：
{
   test: /\.js$/,
   loader: 'babel-loader',
   include: [resolve('examples'), resolve('test'), resolve('packages')]
}
```
|--- build
|--- config
|--- doc // 主要是编写组件过程的记录
|--- exampls // 展示示例
|
```