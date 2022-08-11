<template>
  <div>
    <div class="external">
      <div style="display: flex;margin: 1rem 0.5rem 0 1rem;">
        <div class="inner">
          <div v-show="curId===0">
            <img src="../assets/ava.jpg" style="width: 120px;height: 120px;border-radius: 50%">
            <div style="margin: 5px 0">林凯琳</div>
            <div style="display: flex;flex-wrap: wrap;text-align:center">
              <div class="minbox" >毕业院校：广东技术师范大学</div>
              <div class="minbox">联系方式：13925614094</div>
              <div class="minbox"> 出生年月：1999/10</div>
              <div class="minbox">学历：本科</div>
              <div class="minbox">求职意向:web 前端开发</div>
            </div>
          </div>
          <div v-show="curId===1">
            <p>相关技能</p>
            <p>1、能够使用HTML和CSS编写静态页面</p>
            <p>2、了解并使用vue全家桶（vue-cli、vue-router、vuex、axios、搭配ui框架）</p>
            <p>3、了解并使用uniapp，微信小程序开发</p>
            <p>4、了解使用webpack打包工具和git版本管理工具</p>
            <p>5、能够使用工具画原型图</p>
            <p>6、能够实现前后端接口联调</p>
            <p>7、了解浏览器渲染机制和缓存原理</p>
          </div>
          <div v-show="curId===2">
            <div style="display: flex;justify-content: space-around">
              <p>2020.01-2021.08</p>
              <p>深圳市有华软件开发有限公司</p>
              <p>开发人员</p>
            </div>
            <div style="display: flex;justify-content:space-between">
              <div style="display: flex;justify-content: center;flex-wrap: wrap;width: 45%">
                <div class="detail"  @click="noteId=0" :class="{'not':noteId===0}">熟人地图小程序</div>
                <div class="detail" @click="noteId=1" :class="{'not':noteId===1}">九龄商城管理平台</div>
                <div class="detail" @click="noteId=2" :class="{'not':noteId===2}">真好拼城APP</div>
                <div class="detail"  @click="noteId=3" :class="{'not':noteId===3}">"金手约"盲人按摩辅助系统</div>
              </div>
              <div style="width: 55%;text-align: start">
                <div v-show="noteId===0">
                  <p>项目介绍：主要是关于地图人脉资源的社交小程序，用户可通过推荐人绑定形成多级的人脉关系在地图上区别标记，通过关系链的名片展示来获取交换资源信息。</p>
                  <p>主要任务：</p>
                  <ul>
                    <li>名片的创建存储展示</li>
                    <li>多级人脉关系绑定展示</li>
                    <li>地图分级人脉展示</li>
                    <li>个人动态、个人关注、个人粉丝</li>
                  </ul>
                  <p>主要技术：</p>
                  <p>uniapp+node+MongoDB</p>
                </div>
                <div v-show="noteId===1">
                  <p>项目介绍：一个商城平台的管理系统；包括总平台端、供应商端、商品端形成管理</p>
                  <p>主要任务：</p>
                  <ul>
                    <li>使用echart数据可视化工具实现平台数据的概览</li>
                    <li>实现平台的积分设置、人员角色设置、优惠券设置、消息管理前端页面</li>
                  </ul>
                  <p>主要技术：</p>
                  <p>vue+element-UI</p>
                </div>
                <div v-show="noteId===2">
                  <p>项目介绍：主要关于多级分销的商城APP，用户可以通过推荐人绑定的级别下单购买商品获得平台提供的佣金。</p>
                  <p>主要任务：</p>
                  <ul>
                    <li>实现商城首页、积分排行、产品分类、个人信息、订单管理、积分管理页面</li>
                    <li>实现分享绑定功能</li>
                    <li>实现后端提供的接口进行前后端的数据交互。</li>
                  </ul>
                  <p>主要技术：</p>
                  <p>uniapp+node+MongoDB</p>
                </div>
                <div v-show="noteId===3">
                  <p>项目介绍：主要是关于针对特殊人群开发的按摩店铺工人排班辅助系统APP</p>
                  <p>主要任务：</p>
                  <ul>
                    <li>参与前期原型图的绘制</li>
                    <li>参与后期的模块功能测试</li>
                  </ul>
                  <p>主要技术：</p>
                  <p>uniapp+node+MongoDB</p>
                </div>
              </div>
            </div>
          </div>
          <div v-show="curId===3" style="text-align: start">
            <p>自我评价：</p>
            <p>本人性格开朗、非常有耐心，拥有团队责任感，有着良好的自学能力,能够自学一些新型的技术以配合项目的开发，
              个人认为学习是永无止境的，遇到问题不可怕，要学会全方位多渠道的去寻找解决的办法，不断地去提升自己，能够接受加班。</p>
            <p>校园经历：</p>
            <p>1、院级团学部门部长，策划举办过多项活动</p>
            <p>2、KAB俱乐部副部长，组织开展过部门技术分享会</p>
            <p>3、志愿活动爱好者，参与过多项志愿活动</p>
            <p>证书：1+X web前端开发证书</p>
          </div>
        </div>
        <div style="display: flex;flex-direction: column;justify-content: space-evenly;align-items: center;">
          <div style="display: flex;justify-content: center;margin:30px 0;flex-wrap: wrap;width: 300px">
            <div class="btn3" @click="curId=0" :class="{'cur':curId===0}" style="background-color: #86e3ce">个人信息</div>
            <div class="btn3" @click="curId=1" :class="{'cur':curId===1}" style="background-color: #d0e6a5">自我评价</div>
            <div class="btn3" @click="curId=2" :class="{'cur':curId===2}" style="background-color: #d0e6a5">项目经历</div>
            <div class="btn3" @click="curId=3" :class="{'cur':curId===3}" style="background-color: #86e3ce">其他信息</div>
          </div>
          <div class="btn"></div>
        </div>


      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "homePage",
  data() {
    return {
      curId: 0,
      noteId:0
    }
  },
  methods: {}
}
</script>

<style scoped>
.external {
  border: 0.7rem solid #040000;
  width: 90%;
  height: 27.5rem;
  border-radius: 1.5rem;
  background-color: #ffdd94;
}

.inner {
  border: 0.7rem solid #040000;
  border-radius: 16px;
  height: 24rem;
  width: 90%;
  padding: 5px 10px
}


.btn {
  background: #ec6b46;
  border: 0.7rem solid #040000;
  border-radius: 50%;
  width: 4.1rem;
  height: 4.1rem
}


.btn3 {
  /*width: 200px;*/
  padding: 10px;

  margin: 10px;
  border-radius: 10px;
  height: 40px;
  line-height: 40px;
  border: 0.3rem solid #040000;
}

.minbox {
  width: 500px;
  background-color: #2c3e50;
  margin: 10px 20px 20px 20px;
  border-radius: 10px;
  color: #ffffff;
  padding: 15px 5px;
}
.detail{
  width: 200px;
  margin: 30px 10px 10px 10px;
  height: 100px;
  border-radius: 10px;
  line-height: 100px;
  background-color: #a9b8c7;
}
</style>
