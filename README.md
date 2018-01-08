# firstnuxt

> 学习nuxt

## Build Setup

``` bash
# install dependencies
$ npm install # Or yarn install

# serve with hot reload at localhost:3000
$ npm run dev

# build for production and launch server
$ npm run build
$ npm start

# generate static project
$ npm run generate
```

For detailed explanation on how things work, checkout the [Nuxt.js docs](https://github.com/nuxt/nuxt.js).



# nuxt 为使用vue作为服务器渲染框架的解决方案

## 使用nuxt的动机

-   解决spa单页面应用的首页加载较慢的问题
-   解决动态页面的seo问题,利于爬虫的爬取数据
-   使用vuejs框架,前后端统一框架,便于维护


## 优点: 

- 1.基于node,少配置,开箱即用,对于前端开发者,学习曲线平缓
- 2.基于vue,使用api简单,前端页面也是基于vue,方便前后端处理沟通,一套页面两端都可以用
- 3.支持自动动态路由,动态传参数,无需人工配置路由(以文件名的方式,_id表示传递参数为:id,支持_newsId/newsdetail这类动态二级路由)


根据文件名字及文件路径自动生成路由格式如下:

文件tree
```bash

    --pages         
        --info
            --_id.vue
            --infolist.vue    
        --news
            --_newsId.vue
            --newslist.vue
        --user
            --_id.vue
        index.vue    

```


自动生成的路由
```bash
     routes: [
		{
			path: "/",
			component: _2e7fbb5a,
			name: "index"
		},
		{
			path: "/info/infolist",
			component: _68e7f8c9,
			name: "info-infolist"
		},
		{
			path: "/news/newslist",
			component: _40462b53,
			name: "news-newslist"
		},
		{
			path: "/user/:id?",
			component: _5b85c7d0,
			name: "user-id"
		},
		{
			path: "/news/:userId?",
			component: _0f9852f3,
			name: "news-userId"
		},
		{
			path: "/info/:id?",
			component: _821cc366,
			name: "info-id"
		}
    ],


```










