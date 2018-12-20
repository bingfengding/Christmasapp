<template>
  <div id="home">
    <div class="modal" v-show="modalShow" @click="hideModal"></div>
    <div class="header"></div>
    <div class="main">
      <div class="numBox">
        <div class="numCen">
           <div class="num num1">
            {{numList.first}}
          </div>
          <div class="num num2">
            {{numList.sec}}
          </div>
          <div class="num num3">
            {{numList.thr}}
          </div>
          <div class="num num4">
            {{numList.four}}
          </div>
          <div class="num num5">
            {{numList.fifer}}
          </div>
          <div class="num num6">
            {{numList.six}}
          </div>
          <div class="num num7">
            {{numList.seven}}
          </div>
        </div>
       
      </div>
      <div class="mainBox">
        <div class="eggBox">
          <div class="egg" @click="knockEgg(index)" v-for="(item,index) in eggList" :key="index" :class="knockIndex == index ? 'knockMe' : ''">
            <img src="../image/egg.png" alt="">
          </div>
        </div>
        <div class="btnBox">
          <!-- <div class="residue itemBtn">您还有 <span>{{residue}}</span> 次抽奖机会</div>
          <div class="moreLucky itemBtn">获取更多抽奖机会</div> -->
        </div>
      </div>
      
    </div>
    <div class="gameBox">
      <div class="itemBox">
        <div class="gameItemBox vr">
          <div class="item" @click="openUrl('vr')">
            <div class="text">
              VR彩票
            </div>
          </div>
          <p class="itemText">高画质专业彩票平台</p>
        </div>
        <div class="gameItemBox sport">
        <div class="item" @click="openUrl('sport')">
          <div class="text">
            万博体育
          </div>
        </div>
        <p class="itemText">源自全球领先平台商，世界一流超高投注赔率</p>
        </div>
        <div class="gameItemBox eSports">
        <div class=" item" @click="openUrl('eSports')">
          <div class="text">
            万博电竞
          </div>
        </div>
        <p class="itemText">最好玩的电竞平台</p>
        </div>
        <div class="gameItemBox chess">
          <p class="itemText">专业棋牌游戏供应商</p>
        <div class=" item" @click="openUrl('chess')">
          <div class="text">
            万博棋牌
          </div>
        </div>
        </div>
      </div>
    </div>
    <div class="ruleBox">
      <div class="ruleCen">
         <div class="ruleTextBox">
           <div class="prompt" @click="showInfo">友情建议</div>
           <div class="ruleInfo" v-show="infoShow">
             请于2018年12月24日（00:00:00）准点后参与累计存款。基于网络环境的不稳定性，为保障您可以正常参与活动，您需在2019年1月1日（23:59:59）前完成存款结算，请合理安排，为第三方平台/银行到账预留充分时间，这意味着，2019年1月2日（00:00:00）后到账的存款将不予与累计。感谢您的支持，祝您游戏愉快！
           </div>
          <div class="ruleItem">
            <p class="ruleTitle">【砸蛋时间】</p>
            <p class="ruleText">会员在2018年12月24日00:00:00-2018年12月25日23:59:59和2019年1月1日00:00:00- 23:59:59，3天为砸蛋日期。</p>
          </div>
          <div class="ruleItem">
            <p class="ruleTitle">【砸蛋条件】</p>
            <p class="ruleText">会员在2018年12月24日-2019年1月1日，每累计存款达到2520元即可有一次砸蛋机会（可多次累计）。</p>
          </div>
          <div class="ruleItem">
            <p class="ruleTitle">【砸蛋领取方式】</p>
            <p class="ruleText">请符合活动会员在活动结束后48小时内，使用PC网页版、H5手机网页版、全站客户端(1.27版）和体育APP（1.2.7版）点击优惠页面【申请参与】加入活动：</p>
            <p class="ruleText">1.  提交主题：MXMN122018</p>
            <p class="ruleText">2.  提交内容：</p>
            <p class="ruleText">a)  活动字母（A/B/C）、活动代码（1/2/3/4/5）、符合活动注单号</p>
            <p class="ruleText">b)  奖励等级、任务完成日数</p>
            <p class="ruleText">c)  真实姓名、注册手机号码、奖品名称（若奖励为球衣需提供尺码M/L/XL）、详细邮寄地址信息（省→市→区（乡）→街道（村）→小区（组）→楼号→单元→门牌号）</p>
            <p class="ruleText">本活动遵循&lt;礼遇圣诞 乐惠元旦&gt;活动【温馨提示】</p>
            
          </div>
        </div>
      </div>
     
    </div>
    <div class="moreInfo">
      <div class="moreBox">
        <p class="cenTitle">【敬请期待】</p>
        <p class="title moreBold">亲爱的ManBetX万博会员，</p>
        <p class="title moreBold">您好!</p>
        <p class="moreText">圣诞袜里的心愿单都如期实现了吗？为感恩各位一直以来对ManBetX万博的信任与支持， ManBetX万博年末回馈盛典继续接力！特此献上“好礼不停，金蛋不止”回馈活动！双“蛋”来袭，圣诞过后更有元旦，精彩游戏、神秘大礼轮番登场，惊喜一整年！节日加冕好运不停，幸运锦鲤伴您每一次的满足感都得到升华，与ManBetX万博一起祈愿新年吧！</p>
        <p class="title moreBold">敬祝颂乐</p>
        <p class="last moreBold">ManBetX万博</p>

        <div class="moreBtnBox">
          <!-- <div class="btn">
            了解更多
          </div> -->
        </div>
      </div>
    </div>
  </div>
</template>
<script>

export default {
  data(){
    return {
      infoShow:false,
      modalShow:false,
      knockIndex:null,
      delayKnock :false,
      residue:0,
      numList:{
        first:"0000",
        sec:"0000",
        thr:"0000",
        four:"0000",
        fifer:"0000",
        six:"0000",
        seven:"0000"
      },
      eggList:[
        {
          id:1
        },
        {
          id:2
          },
        {
          id:3
          },
        {
          id:4
        },

      ],
    }
  },
  methods:{
    knockEgg(index){
      if(this.delayKnock) {

      } else {
        this.delayKnock = true
        this.knockIndex = index
        let timer = setTimeout(() => {
          this.knockIndex = null
          this.delayKnock = false
          alert("活动暂未开始")
        }, 500);
      }
     
      
    },
    showInfo(){
      this.modalShow = true
      this.infoShow = true
    },
    hideModal(){
      this.modalShow = false
      this.infoShow = false
    },
    openUrl(value){
      // switch (value) {
      //   case "vr":
      //     window.top.open("http://cn.man984.com/lottery/keno")
      //     break;
      //   case "chess":
      //     window.top.open("http://cn.91manbet.net/liveCasino/cardgame")
      //     break;
      //   case "sport":
      //     window.top.open("http://cn.91manbet.net/sports/msports")
      //     break;
      //   case "eSports":
      //     window.top.open("http://cn.91manbet.net/game/index")
      //     break;
      //   default:
      //     break;
      // }
    }
  },
  components: {

  }
}
</script>
<style lang="stylus" scoped>
#home {
  font-size 0.3rem
  color #555555
  position relative
  .modal {
    position absolute
    left 0
    right 0
    bottom 0
    top 0
    background-color rgba(0,0,0,0.8)
    z-index 100
  }
  .header {
    height 19.17rem
    background url("../image/header_bg.png") no-repeat top center/100% 100%
  }
  .main {
    height 19.22rem
    background url("../image/main_bg.png") no-repeat top center/100% 100%
    padding-bottom 1rem
    display flex
    flex-wrap wrap
    align-items flex-end
    position relative
    .numBox {
      .num {
        position absolute
        width 2.6rem
        height 0.6rem
        background url("../image/num_box.png") no-repeat center center/100% 100%
        line-height 0.6rem
        font-size 0.56rem
        color #fff
        letter-spacing 0.36rem
        padding 0 0.08rem
        transform scale(0.5) translate(-50%,-50%)
      }
      .num1 {
        left 6.53rem
        top 1.76rem
      }
      .num2 {
        left 3.1rem
        top 1.76rem
      }
      .num3 {
        left 8.2rem
        top 3.35rem
      }
      .num4 {
        left 1.46rem
        top 3.34rem
      }
      .num5 {
        left 5.63rem
        top 9.74rem
      }
      .num6 {
        left 8.74rem
        top 9.28rem
      }
      .num7 {
        left 2.36rem
        top 9.23rem
      }
    }
    .mainBox {
      width 100%
      display flex
      justify-content center
      flex-wrap wrap
    }
    .eggBox {
      width 100%
      display flex
      justify-content center
      padding-bottom 2.3rem
      .egg {
        width 2.28rem
        height 3.44rem
        margin-right 0.2rem
        img {
          width 100%
          height 100%
        }
      }
      @keyframes shaking {
        0% {
          transform rotateZ(0)
        }
        25% {
          transform rotateZ(-10deg)
        }
        50% {
          transform rotateZ(0)
        }
        75% {
          transform rotateZ(10deg)
        }
        100% {
          transform rotateZ(0)
        }
      }
      .knockMe {
        transform-origin center bottom
        animation shaking 0.5s linear 1
      }
      .egg:last-of-type {
        margin-right 0
      }
    }
    .btnBox {
      width 100%
      height 1.19rem
      display flex
      justify-content center
      .residue {
        margin-right 0.4rem
        span {
          color #bd2c22
        }
      }
      .itemBtn {

        width 4.19rem
        height 1.19rem
        padding-top 0.1rem
        text-align center
        line-height 1.19rem
        font-size 0.36rem
        background url("../image/main_btn.png") no-repeat top center/100% 100%
        color #ffffff
      }
    }
  }
  .gameBox {
    height 19.23rem
    background url("../image/game_bg.png") no-repeat top center/100% 100%
    position relative
    .itemBox {
      .gameItemBox {
        
        box-sizing content-box
        position absolute
        .itemText {
          padding 0.16rem 0
          font-size 0.24rem
        }
        .item {
          border 0.06rem solid #ffffff
          display flex
          align-items flex-end
          .text {
            font-size 0.32rem
            background-color rgba(255,255,255,0.7)
            line-height 0.8rem
            height 0.8rem
            width 100%
            text-align center
          }
        }
      }
      .vr {
        top 2.8rem
        left 1.8rem
        .item {
          width 3.46rem
          height 5.05rem
          background-image url("../image/game1.png")
          background-size 100% 100%
        }
      }
      .sport {
        top 8.65rem
        left 4.5rem
        .item {
          width 5.36rem
          height 7.5rem
          background-image url("../image/game2.png")
          background-size 100% 100%
        }
        .itemText {
          width 5.36rem
        }
      }
      .eSports {
        top 3.8rem
        left 5.16rem
        .itemText {
          text-align right
        }
        .item {
          width 4.77rem
          height 3.36rem
          background-image url("../image/game4.png")
          background-size 100% 100%
        }
      }
      .chess {
        left 0.8rem
        top 12rem
        .itemText {
          text-align right
        }
        .item {
          width 3.07rem
          height 3.07rem
          background-image url("../image/game3.png")
          background-size 100% 100%
        }
      }
    }
  }
  .ruleBox {
    height 19.23rem
    background url("../image/rule_bg.png") no-repeat top center/100% 100%
    display flex
    justify-content center
    padding-top 4.4rem
    .ruleTextBox {
      width 9.7rem
      min-height 12.4rem
      background-color #ffffff
      padding 0.8rem 0.8rem 0.2rem 0.6rem
      position relative
      .ruleInfo {
        position absolute
        width 9.7rem
        padding 0.4rem
        background-color #ffffff
        z-index 200
        left 0
        top 1rem
      }
      .prompt {
        position absolute
        right 0.8rem
        top 0.4rem
        font-size 0.4rem
        color #fdd883
      }
      .ruleItem {
        padding-bottom 0.6rem
        .ruleTitle {
          font-weight 600
          vertical-align middle
          padding-bottom 0.2rem
          &::before {
            content ""
            background-image url("../image/rule_icon.png")
            vertical-align middle
            display inline-block
            background-size 0.32rem 0.31rem
            width 0.32rem 
            height 0.31rem
          }
        }
        .ruleText {
          padding-left 0.44rem
          text-align justify
        }
      }
    }
  }
  .moreInfo {
    height 19.21rem
    background url("../image/more_bg.png") no-repeat top center/100% 100%
    display flex
    justify-content center
    padding-top 4rem
    .moreBox {
      width 7rem
      min-height 9rem
      .title {
      }
      .last {
        text-align right
        padding-bottom 0.7rem
        padding-top 0.2rem
      }
      .moreBold {
        font-size 0.36rem
        font-weight 600
      }
      .cenBlod {
        text-align center
        line-height 0.6rem
      }
      .cenTitle {
        text-align center
        font-size 0.36rem
        font-weight 600
        padding-bottom 0.4rem
      }
      .moreText {
        line-height 0.5rem
        padding-top 0.2rem
        padding-bottom 0.4rem
        font-size 0.26rem
        
      }
      .moreBtnBox {
        padding-top 1rem
        font-size 0.36rem
        display flex
        justify-content center
        .btn {
          padding-top 0.1rem
          width 3.46rem
          height 1.19rem
          line-height 1.19rem
          text-align center
          background url("../image/more_btn.png") no-repeat center center/100% 100%
          color #ffffff
        }
      }
    }
  }
}
</style>

