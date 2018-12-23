<template>
  <Menu mode="horizontal" :theme="theme1" active-name="1">
    <MenuItem name="4" v-for="(item,index) in Menus" :key="index">
      {{item.item}}
    </MenuItem>
  </Menu>
</template>
<script>
export default {
  data() {
    return {
      theme1: "light",
      url: '../../static/MenuItems.json',
      Menus:[]
    };
  },
  created(){
      this.MenuHandler()
  },
  methods: {
      MenuHandler() {
          this.$axios.get(this.url).then((res) => {
              console.log(res.data.MenuItems)
              this.Menus = res.data.MenuItems
          })
      }
  }
};
</script>
