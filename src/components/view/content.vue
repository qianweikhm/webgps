<template>
  <div class="content">
    <div class="ellipsis recommend-item" v-for="(item,index) in recommend" :key="index">
      <a :href="item.url" target="_blank" >
        <img :src='item.url+"/favicon.ico"' > {{item.web}}
      </a>
    </div>
  </div>
</template>

<script>
export default {
    data() {
        return {
            recommend:[{
                "url": "https://www.baidu.com",
                "web": "百度"
            },{
                "url": "https://github.com/",
                "web": "GitHub"
            },]
        }
    }
};
</script>

<style scoped>
.content {
  position: relative;
  width: 95%;
  margin-left: auto;
  margin-right: auto;
  min-height: 167px;
  margin-top: 20px;
  margin-bottom: 20px;
  padding: 15px;
  border: 1px solid #ddd;
  background: #fff;
}
.ellipsis {
    white-space: nowrap;
    text-overflow: ellipsis;
    overflow: hidden;
    float: left;
}
.recommend-item a {
    padding: 10px;
}
.recommend-item a:hover {
    background: #ebf3ff;
}
img {
    height: 1.3em;
    margin-top: -3px;
    margin-right: 5px;
    vertical-align: middle;
}
a {
    display: block;
    padding: 10px;
    text-decoration: none;
    overflow: hidden;
    color: #2c3e50;
}
</style>
