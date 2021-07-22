<template>
  <div>
  <h2>Rating & Reviews</h2>
  <div class="comments__wrapper wt-offset-top-24">
    <div v-for="item in common" :key="item.id" class="float:left;" @mouseenter="enter(index)" @mouseleave="leave()">
      <p class="width:100px;float:left">{{item.userId}}</p>
    </div>
  </div>
  <div>
    <el-button round  class="MoreButtomClass" type="">show more</el-button>
  </div>
  

  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      common:[
        {
          review:"test",
          date:"2020-07-22",
          userImage:"",
          rating:"4",
          userId:"test1",
          id:1,
          replies:[
            {
               id:"1",
               userId:"test2",
               reply:"testReply"
            },
            {

            }
          ]
        },
        
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.MoreButtomClass{
  font-family: system-ui,-apple-system,BlinkMacSystemFont,Segoe UI,Roboto,Oxygen,Ubuntu,Cantarell,Droid Sans,Helvetica Neue,Arial,sans-serif;
  font-size: 15px;
  font-weight: 400;
  text-align: center;
  white-space: nowrap;
  background: transparent;
  transition: color var(--wt-transition-xfast,.1s),background-color var(--wt-transition-xfast,.1s),border-color var(--wt-transition-xfast,.1s);
  }
.comments__wrapper {
    margin-left: -20px;
    margin-right: -20px;
}
.wt-offset-top-24 {
    margin-top: 24px;
    margin-top: calc(var(--wt-offset-top-unit, 24px)*1);
}
.comment {
    padding: 6px 10px 8px 18px;
    border-radius: 8px;
}
</style>
