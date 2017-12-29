<template>
  <div>
    <h1 class="logo">codejs Api Test</h1>
    <ul class="list">
      <li v-for="item in lists" v-text="item.title"></li>
    </ul>
  </div>
</template>
<script>
  export default {
    data () {
      return {
        lists: []
      }
    },
    created () {
      this.get_data()
    },
    methods: {
      get_data: function(params) {
        var v = this
        if(!params) params = {}
        //我们这里用全局绑定的$api方法来获取数据，方便吧
        v.$api.get('topics', params, function(r){
          v.lists = r.data
        })
      },
    },
  }
</script>
<style>

</style>
