# Vue组件多项目使用的解决方案(一个vue menu组件的demo)
在开发vue项目的时候，我们会创建许多组件，当前项目可以随意引用，但是如果有其他的项目或者其他人想要用这些组件的时候，就像npm下载包一样那样方便。那么我们可以做成npm包在git上进行统一管理([因为npm install可以安装git项目](https://docs.npmjs.com/cli/install) )。
## 解决方案

### 说明： 将vue组件开发成一个包，然后提交到git上进行统一管理。


## 包文件结构

src  
  * index.vue

index.js

package.json

README.md


## 步骤：
1. 在git上新建一个仓库，然后写好仓库名，各种必填的信息（例如项目名称为 vue-test）

2. 在本地使用git clone 项目

3. 进入项目文件夹，然后 npm init初始配置文件，然后可以一直回车

4. 将组件放入src文件夹中。

5. 新建index.js，然后 引入组件，并且输出模块名(变量名)

```
import Menu from './src/index.vue'
export default Menu
```
因为在开发项目中一般都模块化开发，通过import或者require来引入js，所以这里需要使用export输出变量名或者模块名。关于js模块化加载介绍参考[js模块化加载介绍](https://github.com/liunian/webpack-doc/blob/master/motivation.md)
 
6. 使用git将项目提交到远程仓库

## 下载组件

### npm install git+repo-url

## 使用组件

和平常的用法一样

```
import componentName from 'packName'
.......
component：{
    componentName
}
.......
```
