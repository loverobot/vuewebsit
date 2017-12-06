<template>
   <div id="nav">
    <nav class="navbar navbar-inverse">
        <div class="container">
            <div class="navbar-header">
                <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#navbar" aria-expanded="false" aria-controls="navbar">
                      <span class="sr-only">{{disableRipple+title}}</span>
                      <span class="icon-bar"></span>
                      <span class="icon-bar"></span>
                      <span class="icon-bar"></span>
                </button>
                <a class="navbar-brand" href="#">IT-PLAYBOY</a>
            </div>
            <div id="navbar" class="collapse navbar-collapse">
                <ul class="nav navbar-nav">
                      <li 
                         v-for="(nav,index) in navs" 
                         :class="{active: index === num}"
                         @click="active(index)">
                          <a :href="nav.url">{{ nav.name }}</a>
                      </li>
                </ul>
            </div>
            <!--/.nav-collapse -->
        </div>
    </nav>
    
    </div>
</template>
<script>
export default {
  name:'nav',
  props:{
      someprop:{
          type:Number,
          default:2
      },
      title:String,
      disableRipple:String
  },
  data(){  //返回新的对象 防止模板多次引用 数据也被共用
      return{
        num:0,
        navs :[
            {name:'首页',url:'#/index'},
            {name:'关于我们',url:'#/detail'},
            {name:'联系我们',url:'#/about'},
        ]
      } 
  },
  methods:{
      active:function(i){
          this.num = i;
      }
  },
  computed:{
      
  }
}
</script>


