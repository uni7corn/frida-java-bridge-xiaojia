### 修改了frida的javahook

其实本质上frida会更加稳定，但是我们的也是基本没什么问题的，本质上就是修改的ArtMethod。

提供两个分支，一个hook了GetOatQuickMethod的，这个会更加稳定，但是hook了libart，一个没有hook这个的，无痕但是在特殊情况下不是很稳定。但是不代表用不了，无痕的这个函数如果hook出现了问题，你可以换一个函数去hook也许有几率会修复这个问题。

编译：

```
npm run build
```

得到_agent.js



监控：

```
npm run watch
```

动态更新，这个_agent.js文件也动态更新



切换直接替换lib/android.js里面的代码就可以



此为frida-java-bridge原始6.3.6版本