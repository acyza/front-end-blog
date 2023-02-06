# 创建uniapp+vue3+vite+typescript项目并在vscode中开发

以下的`{{dir}}`换成自己项目文件夹名称

##### 注：`{{dir}}`只是文件夹名称，不是项目名称

## 第一步：
```
npx degit dcloudio/uni-preset-vue#vite-ts {{dir}}
```

[官方文档](https://uniapp.dcloud.net.cn/quickstart-cli.html#%E5%88%9B%E5%BB%BAuni-app)

## 第二步：
```
cd {{dir}}
```
## 第三步：
npm install

我这报了个依赖解析错误
![error](../%E6%88%AA%E5%9B%BE/%E4%BE%9D%E8%B5%96%E8%A7%A3%E6%9E%90%E9%94%99%E8%AF%AF.png)
解决方法，找到项目文件夹中的package.json用文本编辑器打开，删除"vite":"4.0.4"这行，因为依赖树中已经存在vite，这里似乎不需要再引入vite。

## 第四步：

第三步完成且无报错后
```
npm run dev:h5
```
稍等片刻后会显示几个链接：打开`Local:`后面的链接如果可以正常访问说明安装成功了

## 第五步
打开vscode

文件>打开文件夹>选择项目文件夹

完成以上步骤就可以在vscode中愉快的编写代码了。