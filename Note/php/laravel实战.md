# laravel实战 #
>
 1.使用composer创建laravel项目
>
 - `composer global require "laravel/installer"`
>
 - `laravel new blog`
>
 2.安装node.js，使用前端包管理 npm
>
*注意：在运行npm时请科学上网或者切换国内某宝镜像，否则会导致安装失败*
>
运行`npm install`，修改`package.json`如下：
>
	{
	  "private": true,
	  "scripts": {
	    "dev": "npm run development",
	    "development": "cross-env NODE_ENV=development node_modules/webpack/bin/webpack.js --progress --hide-modules --config=node_modules/laravel-mix/setup/webpack.config.js",
	    "watch": "cross-env NODE_ENV=development node_modules/webpack/bin/webpack.js --watch --progress --hide-modules --config=node_modules/laravel-mix/setup/webpack.config.js",
	    "watch-poll": "npm run watch -- --watch-poll",
	    "hot": "cross-env NODE_ENV=development node_modules/webpack-dev-server/bin/webpack-dev-server.js --inline --hot --config=node_modules/laravel-mix/setup/webpack.config.js",
	    "prod": "npm run production",
	    "production": "cross-env NODE_ENV=production node_modules/webpack/bin/webpack.js --progress --hide-modules --config=node_modules/laravel-mix/setup/webpack.config.js"
	  },
	  "devDependencies": {
	    "axios": "^0.16.2",
	    //    "bootstrap-sass": "^3.3.7",
	    "cross-env": "^5.0.1",
	    "jquery": "^3.1.1",
	    "laravel-mix": "^1.0",
	    "lodash": "^4.17.4",
	    "vue": "^2.1.10"
	  }
	}

>
3.运行`npm install buma`