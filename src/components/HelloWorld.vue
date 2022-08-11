<template>
  <div class="contain">
    <div class="content" style="color:#fff">
      <p >我叫林凯琳</p>
      <p >毕业于广东技术大学</p>
      <p >软件工程专业</p>
      <p >是今年的应届毕业生</p>
      <p >当前状态</p>
      <p >正在真诚的找工作中</p>
      <p >这是我的简历</p>
      <p @click="more()"><img style="width: 50px;height:50px" src="../assets/down.png"></p>
    </div>
    <div style="color:#ffffff;display:flex;flex-wrap: wrap;justify-content: center" v-if="type">
      <a class="info" href="#target1">个人信息</a>
      <a class="info" href="#target2">自我评价</a>
      <a class="info" href="#target3">项目信息</a>
      <a class="info" href="#target4">其他信息</a>
    </div>
  <div id="target1">
    <p>个人信息</p>
    <p>姓名：林凯琳</p>
    <p>出生年月：1999.10</p>
    <p>联系方式：13925614094</p>
    <p>学历：本科</p>
  </div>
    <div id="target2">
      <p>个人信息</p>
      <p>姓名：林凯琳</p>
      <p>出生年月：1999.10</p>
      <p>联系方式：13925614094</p>
      <p>学历：本科</p>
    </div>
    <div id="target3">
      <p>个人信息</p>
      <p>姓名：林凯琳</p>
      <p>出生年月：1999.10</p>
      <p>联系方式：13925614094</p>
      <p>学历：本科</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      type: false,
      mes: "999"
    }
  },
  methods: {
    more() {
      this.type = !this.type
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.contain{
  color: #ffffff;
}
.content {
  animation: ani ease-out 0s infinite normal;
}

/*@keyframes ani {*/
/*  0% {*/
/*    opacity: 0;*/
/*  }*/
/*  100% {*/
/*    opacity: 1;*/
/*  }*/
/*}*/


@keyframes ani {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}

@keyframes arrow {
  100% {
    opacity: 1;
    transform: translate(0, 10px)
  }
}

@keyframes info {
  0%{
    opacity: 0;
  }
  50%{
    opacity: 0.5;
  }
  100% {
    opacity: 1;
    transform: translate(0, 5px)
  }
}

.content p:nth-child(1) {
  animation: ani 0.2s both;
}

.content p:nth-child(2) {
  animation: ani 0.6s 1s both;
}

.content p:nth-child(3) {
  animation: ani 0.6s 2s both;
}

.content p:nth-child(4) {
  animation: ani 0.6s 3s both;
}

.content p:nth-child(5) {
  animation: ani 0.6s 4s both;
}

.content p:nth-child(6) {
  animation: ani 0.2s 5s both;
}

.content p:nth-child(7) {
  animation: ani 0.2s 6s both;
}

.content p:nth-child(8) {
  animation: arrow 1.2s 6.5s infinite ease-in-out;
}

.info {
  animation: info 1.2s ease-in-out forwards ;
}

.contain {
  background-color: #183c47;
}
.info {
  display: inline-block;
  line-height: 100px;
  width: 100px;
  height: 100px;
  margin:10px 20px;
  border-radius: 50%;
  background: radial-gradient(circle at 50% 120%, #81e8f6, #76deef 10%, #055194 80%, #062745 100%);
}
.info:before {
  content: "";
  border-radius: 50%;
  background: radial-gradient(circle at 50% 0px, #ffffff, rgba(255, 255, 255, 0) 58%);
  -webkit-filter: blur(5px);
  z-index: 2;
}

.info .shadow {
  width: 100%;
  height: 100%;
  background: radial-gradient(circle at 50% 50%, rgba(0, 0, 0, 0.4), rgba(0, 0, 0, 0.1) 40%, rgba(0, 0, 0, 0) 50%);
  -webkit-transform: rotateX(90deg) translateZ(-150px);
  -moz-transform: rotateX(90deg) translateZ(-150px);
  -ms-transform: rotateX(90deg) translateZ(-150px);
  -o-transform: rotateX(90deg) translateZ(-150px);
  transform: rotateX(90deg) translateZ(-150px);
  z-index: -1;
}

</style>
