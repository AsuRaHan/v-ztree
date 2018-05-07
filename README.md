# v-ztree

A simple tree for Vue2, support single or multiple(check) select tree, and support server side data

## Install

``` bash
npm i v-ztree --save
```

Include plugin in your `main.js` file.

```js
import Vue from 'vue';
import vZtree from 'v-ztree';

Vue.use(vZtree);
```

## Deploy on you component

template code

```html
<template>
    <v-tree @selected="selected"
                :data="data"
                :data-format="dataFormat"
                :expand-all="false"></v-tree>
</template>
```

script code
```js
export default {
    name: 'myComponent',
    data(){
        return {
            //local json data
            data: [{id:11, pId:1, name:"node1"},{id:11, pId:1, name:"node1"},{...}],
            //server side data
            //data: 'http://xxx.com/load'
        }
    },
    methods:{
        //receive selected tree node info
        selected(nodes){
            console.log(nodes);//{id:1,pId:0,name:'aaa',...}
        }
    }
};
```
