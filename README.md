# market
- 轮播图(vue-awesome-swiper)

'''

    <swiper-slide v-for="(page,index) in pages" :key="index">
        <div class="iconItem" v-for="(item,index) in page" :key="index">
            <a href="" :style="{backgroundImage:'url('+item.imgUrl+')'}">
              <h6>{{item.title}}</h6>
            </a>
        </div>
      </swiper-slide>
'''
- 懒加载

> A Vue.js project

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).
