# 一个基于typescript构建npm包的工程模板

[参考链接]([超链接地址](https://www.yuque.com/zcue/blog/lqd043) "NPM 发布 TS 包")

直接git clone仓库下来使用。
npm publish 构造
命令|操作|备注
--|:--:|--
prepare|npm run build|在打包和发布之前运行，适合build
prepublishOnly|npm test && npm run lint|在 prepare 之前，并且只有 npm publish 时才运行，这里应该执行测试和lint，保证我们不会发布不好的代码
preversion|npm run lint|在新建 tag 之前运行
version|npm run format && git add -A src|在改了 tag 之后，但 commit 之前
postversion|git push && git push --tags|在改了 tag 之后，commit 之后
