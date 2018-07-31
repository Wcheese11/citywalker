<template>
    <div class="infoCard"@click="bindViewTap">
      <img :src=backimg alt="景点图片">
      <span>{{test}}</span>
    </div>
</template>

<script>
  export default {
    data () {
      return {
        test: '测试',
        backimg: 'http://img4.imgtn.bdimg.com/it/u=3836539368,3142492826&fm=27&gp=0.jpg'
      }
    },
    computed: {
      remain () {
        return 1
      }
    },
    props: ['text', 'imgSrc'],
    name: 'infoCard',
    methods: {
      bindViewTap () {
        const url = '../todolist/main'
        wx.navigateTo({ url })
      }
    }
  }
</script>

<style scoped>
.infoCard{
  -webkit-box-sizing: content-box;
  -moz-box-sizing: content-box;
  box-sizing: content-box;
  width: 193px;
  height: 100px;
  border: 2px solid rgba(0,150,255,0.91);
  -webkit-border-radius: 41px;
  border-radius: 41px;
  font: normal 14px/1 "Times New Roman", Times, serif;
  color: rgba(0,0,0,1);
  -o-text-overflow: ellipsis;
  text-overflow: ellipsis;
  -webkit-box-shadow: 0 0 1px 0 rgba(0,0,0,0.5) inset, 3px 3px 4px 0 rgba(0,0,0,0.4) , 5px 5px 8px 2px rgba(0,0,0,0.5) inset, 4px 4px 6px 1px rgba(0,0,0,0.5) inset, 3px 3px 4px 0 rgba(0,0,0,0.4) ;
  box-shadow: 0 0 1px 0 rgba(0,0,0,0.5) inset, 3px 3px 4px 0 rgba(0,0,0,0.4) , 5px 5px 8px 2px rgba(0,0,0,0.5) inset, 4px 4px 6px 1px rgba(0,0,0,0.5) inset, 3px 3px 4px 0 rgba(0,0,0,0.4) ;
  -webkit-transition: all 200ms cubic-bezier(0.42, 0, 0.58, 1) 10ms;
  -moz-transition: all 200ms cubic-bezier(0.42, 0, 0.58, 1) 10ms;
  -o-transition: all 200ms cubic-bezier(0.42, 0, 0.58, 1) 10ms;
  transition: all 200ms cubic-bezier(0.42, 0, 0.58, 1) 10ms;
  -webkit-transform: rotateX(8.021409131831525deg) rotateY(-34.95042550298022deg)   ;
  transform: rotateX(8.021409131831525deg) rotateY(-34.95042550298022deg)   ;
}
  .infoCard img{
    width: 200rpx;
    height: 100rpx;
  }

</style>
