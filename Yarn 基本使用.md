## Yarn 基本使用 ##

### 开始一个新项目 ###
    yarn init

### 添加依赖关系 ###

    yarn add [package]
    yarn add [package]@[version]
    yarn add [package]@[tag]

### 将依赖关系添加到不同类别的依赖项 ###

> 添加到devDependencies，peerDependencies和optionalDependencies分别为：

    yarn add [package] --dev
    yarn add [package] --peer 
    yarn add [package] --optional

### 升级依赖项 ###

    yarn upgrade [package]
    yarn upgrade [package]@[version]
    yarn upgrade [package]@[tag]

### 删除依赖项 ###

    yarn remove [package]

### 安装项目的所有依赖项 ###

    yarn
	||
    yarn install

### 运行一个定义的包脚本 ###

你可以在你的package.json文件中定义scripts。

    {
	    "name": "my-package",
	    "scripts": {
		    "build": "node index.js",
		    "test": "jest"
		 }
    }

    yarn run [script] [<args>]
