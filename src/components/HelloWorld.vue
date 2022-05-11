<template>
 <div>
  <div class="nav">
    <div class="logo">
            <img src="../assets/logo.png" alt="">
    </div>
      <div class="ul">
          <ul>
              <li :class="{actived:active}" @click="x" ref="index">首页</li>
              <li>AI诊断</li>
              <li>在线课程</li>
              <li>教学动态</li>
              <li>科研展示</li>
          </ul>
          <div class="line" ref="line"></div>
      </div>
   <div class="login">
       <img src="../assets/ico_search.png" alt="" style="width: 24px;">
      <span>登录/注册</span>
   </div>
  </div>
  <div class="body">
      <div class="lunBo">
          <div class="block">
        <el-carousel height="400px" >
            <el-carousel-item v-for="(item,index) in items" :key="index" >
                <img :src="item.url">
            </el-carousel-item>
        </el-carousel>
    </div>
          <div><ul>
              <li>在线授课</li>
              <li>AI快速诊断</li>
              <li>记录检查</li>
              <li>精准解答疑问</li>
          </ul> </div>
</div>
      <div class="action">
              <div class="blueColor">
                  最新活动
              </div>
              <div>
                  <div class="img-wrapper" >
                      <div class="block" style="flex-basis: 27%;margin-right: 50px">
                          <el-carousel trigger="click" height="300px" >
                              <el-carousel-item v-for="(item,index) in actions" :key="index">
                                  <img :src="item.url">
                              </el-carousel-item>
                          </el-carousel>
                      </div>
                      <div><img src="../assets/index_06.jpg" alt="" width="920px" height="300px"></div>
                  </div>
              </div>
      </div>
      <div class="Popular">
          <ul>
              <li>课题播放</li>
              <li>问题解答</li>
              <li>注册用户</li>
              <li>名师团队</li>
          </ul>
      </div>
      <div style="position: relative">
          <div class="AI-message" >AI智能诊断技术</div>
          <div>
              <img src="../assets/AI.jpg" alt="">
          </div>
      </div>
  </div>
  <div class="footer">
      <div class="wrapper ">
          <div class="message">
              <img src="../assets/ai_04.png" alt="" style="position: absolute;height:200px ">
              <ul>
                  <li class="tag">联系我们</li>
                  <li>公司地址</li>
                  <li>联系电话</li>
                  <li>公司邮箱</li>
                  <li>业务部</li>
              </ul>
              <ul>
                  <li class="tag">快捷导航</li>
                  <li>首页</li>
                  <li>AI诊断</li>
                  <li>在线课程</li>
                  <li>教学动态</li>
                  <li>科研成果</li></ul>

              <ul>
                  <li class="tag">友情链接</li>
                  <li>慕课网</li>
                  <li>国家知识库</li>
                  <li>百度网</li>
                  <li>中国大学MOOC</li>
              </ul>
          </div>
          <div class="message-2">
              <el-button type="primary" round style="background: rgb(52, 158, 235);margin-bottom:20px;">在线留言</el-button>
              <div class="Erwei">
                  <div>
                      <img src="../assets/ai_50.jpg" alt="">
                  </div>

                  <div>
                      <img src="../assets/ai_50.jpg" alt="">
                  </div>
              </div>
          </div>
      </div>
      <div class="footer-msg">
          版权所有
      </div>
  </div>
   </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data(){
    return{
      active:true,
      items: [
        {url: require("../assets/lunBo1/ai_32.jpg")},
        {url: require("../assets/lunBo1/ai_34.jpg")},
        ],
      imges:[
        {url: require("../assets/teacher/index_08.png")},
        {url: require("../assets/teacher/index_09.png")},
        {url: require("../assets/teacher/index_10.png")},
        {url: require("../assets/teacher/index_19.png")},
      ],
      actions:[
        {url: require("../assets/ai_04.png")},
        {url: require("../assets/ai_04.png")},
        {url: require("../assets/ai_04.png")},
      ]
    }
    },
  }


</script>

<style scoped lang="scss">
    $blue:rgb(52, 158, 235);
    .blueColor{
        color: $blue;
        font-size: 20px;
        padding: 10px;
        font-weight: bold;
        margin: 10px auto;
    }
.actived{
        color: $blue
    }
.nav{
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    align-items: center;
    position: relative;
    >.logo{

        display: flex;
        flex-direction: row;

    }
    > .ul{
        position: relative;
        padding: 20px;
        > ul {
            display: flex;

            > li {
                padding: 0 10px;
                font-size: 14px;
                margin: 0 20px;

                &:hover {
                    color: $blue;
                    cursor: pointer;
                }
            }
        }
        > .line{
            width: 48px;
            position: absolute;
            bottom: 0;
            margin-left: 20px;
            border:1px solid rgb(52, 158, 235);
        }
    }

    >.login{
        position: absolute;
        right: 30px;
        display: flex;
        align-items: center;
        justify-content: center;

        >span{
            font-size: 14px;
            line-height:24px;

        }
    }
}
.body{
    >.lunBo{
        *> ul{
            display: flex;
            margin: 0 auto;
            justify-content: space-around;
            padding: 30px 150px;
            >li{
                &:hover{
                    color:$blue;
                    cursor: pointer;
                }
            }
        }
    }
    >.action{
        background: rgb(247,247,247);
        *>.img-wrapper{
            display: flex;
            flex-direction: row;
            padding: 10px ;
            justify-content: right;

        }
    }
    >.Popular{
        display: flex;
        flex-direction: column;
        >ul{
            display: flex;
            justify-content: space-around;
            padding: 30px 150px;
            >li{
                &:hover{
                    color: $blue;
                    cursor: pointer;
                }
            }
        }
    }
    *>.AI-message{
        position: absolute;
        color: white;
        left: 20%;
        top: 20%;
        font-size: 26px;
        font-weight: bold;
    }
}
.footer{
    height: 30%;
    >.wrapper{
        display: flex;
        padding: 50px;
        justify-content: space-around;
        >.message{
            display: flex;
            position: relative;
            >ul{
                margin: 0 20px;
                color: grey;
                >.tag{
                    font-size: 20px;
                    color: black;
                    margin-bottom:20px;
                    font-weight: bold;
                }
            }
        }
        >.message-2{
            >.Erwei{
                display: flex;
                *>img{
                    margin: 0 10px;
                    width: 100px;
                }
            }
        }

    }
    >.footer-msg{
        background: $blue;
        font-size: 10px;
        padding: 10px;
        color: white;
        margin: 10px auto 50px;
    }
}

.el-carousel__item h3 {
    color: #475669;
    font-size: 14px;
    opacity: 0.75;
    line-height: 150px;
    margin: 0;
}
.el-carousel__item:nth-child(2n) {
    background-color: #99a9bf;
}
.el-carousel__item:nth-child(2n+1) {
    background-color: #d3dce6;
}
.el-carousel__item h3 {
        color: #475669;
        font-size: 14px;
        opacity: 0.75;
        line-height: 200px;
        margin: 0;
    }
.el-carousel__item:nth-child(2n) {
        background-color: #99a9bf;
    }
.el-carousel__item:nth-child(2n+1) {
        background-color: #d3dce6;
    }
</style>
