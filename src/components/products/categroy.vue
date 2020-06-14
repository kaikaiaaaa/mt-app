<template>
  <div class="m-product-categroy">
      <dl class="classic">
          <dt>分类</dt>
          <dt>全部</dt>
          <dd v-for="(item) in classicList" :key="item.type">
              <m-select :name="item.title" :list="item.sub_list"></m-select>
          </dd>
      </dl>
      <dl class="classic">
          <dt>区域</dt>
          <dt>全部</dt>
          <dd v-for="(item) in areaList" :key="item.type">
              <m-select :name="item.title" :list="item.sub_list"></m-select>
          </dd>
      </dl>
  </div>
</template>

<script>
import MSelect from './selece.vue'
 export default {
    data(){
        return{
            classicList:[
                {
                    title:"美食",
                    type:"food",
                    sub_list:[
                        {
                            name:"日本菜",
                            id:"Japan"
                        },
                         {
                            name:"中国菜",
                            id:"China"
                        },
                    ]
                },
                  {
                    title:"酒店",
                    type:"hotel",
                    sub_list:[
                        {
                            name:"98酒店",
                            id:"aaa"
                        },
                         {
                            name:"维纳斯",
                            id:"wns"
                        },
                    ]
                },
            ],
            areaList:[
                {
                    title:"推荐商圈",
                    sub_list:[
                        {
                            name:"望京",
                            id:120000
                        },
                         {
                            name:"昌平",
                            id:1222
                        },
                    ]
                },
            ]
}
},
components:{
MSelect,
}

}
</script>

<style>

</style>