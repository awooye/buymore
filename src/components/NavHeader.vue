<template>
  <div class="header">
    <div class="nav-topbar">
      <div class="container">
        <div class="top-menu">
          <div class="top-menu-left">
            <span>欢迎来到丝芙兰</span>
            <a href="javascript:;">请登录</a>
            <i class="line-split"></i>
            <a href="javascript:;">免费注册</a>
            <a href="javascript:;">手机验证码登录</a>
          </div>

          <el-carousel direction="vertical" :autoplay="true">
            <el-carousel-item v-for="item in topList" :key="item">
              <h3 class="medium">{{ item.title }}</h3>
            </el-carousel-item>
          </el-carousel>
          <div class="top-menu-right">
            <span class="top-m-r menu-r1">
              <span class="my-sephora"></span>
              <a href="javascript:;">我的丝芙兰</a>
              <span class="arrow-down"></span>
              <ul class="my-sephora-hover top-angle">
                <li>
                  <a href="javasctipt:;">我的订单</a>
                </li>
              </ul>
            </span>
            <span class="top-m-r">
              <span class="vip-club"></span>
              <a href="javascript:;">会员俱乐部</a>
            </span>
            <span class="top-m-r">
              <span class="mobile-sephora"></span>
              <a href="javascript:;">手机丝芙兰
                <img class="mobile-erweima" src="/imgs/downQR2.png" alt="">
              </a>
            </span>
            <a class="help" href="javascript:;">帮助中心</a>
          </div>
        </div>
      </div>
    </div>
    <div class="search">
      <div class="container">
        <div class="search-info">
          <div class="search-logo-box">
            <a class="search-logo" href="javascript:;">
              <img src="/imgs/sep_top_Logo.png" alt="" />
            </a>
          </div>
          <div class="search-box">
            <div class="search-up">
              <div class="search-input">
                <input type="text" :placeholder="psdPlaceholder" />
              </div>
              <a class="search-button" href="javascript:;">搜索</a>
            </div>
            <div class="search-down">
              <a href="javascript:;">周末秒杀</a>
              <a href="javascript:;">新年星品大集结</a>
              <a href="javascript:;">面膜补水成吨屯</a>
              <a href="javascript:;">美力度假不花状</a>
              <a href="javascript:;">小众香氛新浪潮</a>
              <a href="javascript:;">小众尖货盘点</a>
            </div>
          </div>
          <a class="shop-car" href="javascript:;">
            <em class="shopping-bag"></em>
            购物袋
            <span class="shopping-num">0</span>
            件
          </a>
        </div>
      </div>
    </div>
    <div class="navigation">
      <div class="container">
        <div class="navigation-info">
          <div class="nav-menu">
            <a href="javascript:;">全部商品类目</a>
          </div>
          <div class="nav-link">
            <ul>
              <li><a href="javascript:;">畅销榜单</a></li>
              <li><a href="javascript:;">独家发售</a></li>
              <li><a href="javascript:;">礼物套装</a></li>
              <li><a href="javascript:;">全部品牌</a></li>
              <li><a href="javascript:;">预约中心</a></li>
            </ul>
          </div>
          <div class="nav-img">
            <div class="nav-img-box">
            <img src="/imgs/navigation_shopping.png" alt="">

            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "nav-header",
  component: {},
  data() {
    return {
      autoplay: "",
      psdPlaceholder: "红出新势力",
      topList: [
        {
          title: "丝芙兰正品承诺",
        },
        {
          title: "常见问题",
        },
      ],
      
    };
  },
};
</script>
<style lang="scss">
@import "./../assets/scss/base.scss";
@import "./../assets/scss/mixin.scss";
.header {
  .nav-topbar {
    width: 100%;
    background-color: #000;
    .top-menu {
      @include flex();
      width: 100%;
      height: 30px;
      background-color: #000;
      .top-menu-left {
        // width: 420px;
        span {
          color: #fff;
          margin: 0 22px 0 12px;
        }
        a {
          color: #fff;
          margin: 0 12px;
          &:hover {
            color: #f00;
          }
        }
        .my-sephora-a {
          &:hover {
            .my-sephora-hover {
              display: block;
            }
          }
        }
        .line-split {
          border-left: 1px solid #ccc;
          display: inline-block;
          vertical-align: sub;
          font-weight: 400;
          height: 16px;
          font-style: normal;
        }
      }
      .el-carousel {
        margin-left: -105px;
        .el-carousel__container {
          height: 30px;
          width: 230px;
          color: #fff;
          .el-carousel__item {
            h3 {
              line-height: 30px;
              font-size: 12px;
              color: #fff;
            }
          }
        }
        .el-carousel__indicators {
          display: none;
        }
      }
      .top-menu-right {
        position: relative;
        .menu-r1 {
          &:hover {
            .arrow-down {
              background-position: -3px -12px;
            }
            .my-sephora-hover {
              display: block;
            }
          }
        }
        .top-m-r {
          margin-left: 22px;
          .my-sephora {
            @include bgImg(12px, 12px, "/imgs/my-sephora.png");
            margin-right: 6px;
            margin-top: -2px;
          }
          a {
            color: #fff;
            &:hover {
              color: #f00;
            }
          }
          .arrow-down {
            content: "";
            background-image: url("./../../public/imgs/top_angle_w.png");
            width: 9px;
            height: 4px;
            display: inline-block;
            margin-left: 5px;
            margin-bottom: 3px;
            background-position: -3px -16px;
          }
          .top-angle {
            content: "";
            background-image: url("/imgs/top_angle_w.png");
          }
          .my-sephora-hover {
            position: absolute;
            display: none;
            top: 17px;
            left: 23px;
            padding-top: 7px;
            background-repeat: no-repeat;
            border-bottom: 1px solid #c8c8c8;
            z-index: 99;
            li {
              display: block;
              padding: 5px 10px;
              width: 88px;
              height: 30px;
              border-right: 1px solid #c8c8c8;
              border-left: 1px solid #c8c8c8;
              background-color: #fff;
              a {
                display: block;
                color: #000;
                text-align: center;
                &:hover {
                  color: #f00;
                }
              }
            }
          }
        }
      }
      .top-m-r {
        .vip-club {
          @include bgImg(12px, 12px, "/imgs/vip-club.png");
          margin-right: 6px;
          margin-top: -2px;
        }
      }
      .top-m-r {
        .mobile-sephora {
          @include bgImg(7px, 12px, "/imgs/mobile-sephora.png");
          margin-right: 6px;
          margin-top: -2px;
         
        }
         a{
           position: relative;
           &:hover{
             .mobile-erweima{
               display: block;
             }
           }
            .mobile-erweima{
              display: none;
              position: absolute;
              z-index: 29;
              top: 14px;
              left: -263px;

            }
          }
      }
      .help {
        color: #fff;
        margin-left: 22px;
        &:hover {
          color: #f00;
        }
      }
    }
  }
  .search {
    background-color: #fff;
    .container {
      .search-info {
        @include flex(flex-start);
        height: 84px;
        padding-top: 24px;
        align-items: start;
        .search-logo-box {
          width: 320px;
          height: 36px;
          .search-logo {
            display: block;
            width: 240px;
            height: 32px;
            margin: 2px 0;
            img {
              width: 100%;
              height: 100%;
            }
          }
        }
        .search-box {
          width: 650px;
          height: 60px;
          @include flex();
          flex-wrap: wrap;
          .search-up {
            @include flex();
            width: 630px;
            .search-input {
              width: 540px;
              height: 34px;
              border: 1px solid #c8c8c8;
              background-color: #fff;
              input {
                width: 100%;
                height: 100%;
                line-height: 34px;
                padding-left: 20px;
                font-size: 12px;
                outline: 0;
                border: 0;
              }
            }
            .search-button {
              display: inline-block;
              background-color: #000;
              width: 90px;
              height: 34px;
              border: 1px solid #000;
              border-left: 0;
              border-right: 0;
              color: #fff;
              font-size: 16px;
              text-align: center;
              line-height: 34px;
            }
          }
          .search-down {
            z-index: 1;
            a {
              font-size: 12px;
              color: #acacac;
              padding: 0 4px;
              &:hover{
                color:#f00;
              }
            }
          }
        }
        .shop-car {
          display: inline-block;
          margin-left: 32px;
          color: #000;
          width: 188px;
          height: 36px;
          line-height: 34px;
          border: 1px solid #ddd;
          background-color: #fff;
          text-align: center;
          font-size: 16px;
          z-index: 10;
          .shopping-bag {
            @include bgImg(18px, 26px, "/imgs/shopping_bag.png");
            margin-left: 10px;
            margin-right: 10px;
          }
          .shopping-num {
            color: #f00;
          }
        }
      }
    }
  }
  .navigation{
    .container{
      .navigation-info{
        background-color: #fff;
        @include flex();
        height: 36px;
        .nav-menu{
          @include bgImg(240px,36px,"/imgs/classified.png");
          a{
            margin-left:15px;
            font-size: 16px;
            color: #fff;
            line-height: 36px;
          }
        }
        .nav-link{
          ul{
            @include flex(flex-start);
            width: 760px;
            height: 42px;
            padding-left: 40px;
            li{
              margin-right: 40px;
              
              a{
                font-size: 16px;
                color: #000;
                &:hover{
                color: #f00;
              }
              }
            }
          }

        }
        .nav-img{
          // width: 209px;
          // height: 36px;
          cursor: pointer;
          z-index: 9;
        }
      }
    }
  }
}
</style>
