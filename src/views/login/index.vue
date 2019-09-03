<template>
  <div class="login-back">
    <div class="boat">
      <div class="wrap">
        <div class="main">
          <div class="boat-top-layer">
            <div class="top">
              <div class="pole"></div>
              <div class="help"><span></span></div>
            </div>
            <div class="bottom"></div>
          </div>
          <div class="boat-mid-layer">
            <div class="top"></div>
            <div class="bottom"></div>
          </div>
          <div class="boat-bot-layer">
            <div class="top"></div>
            <div class="bottom"></div>
          </div>
        </div>
      </div>
      <div class="water">
        <div class="drops clearfix drops-1">
          <span class="drop drop-a"></span>
          <span class="drop drop-b"></span>
          <span class="drop drop-c"></span>
          <span class="drop drop-d"></span>
          <span class="drop drop-e"></span>
          <span class="drop drop-f"></span>
          <span class="drop drop-g"></span>
          <span class="drop drop-h"></span>
        </div>
        <div class="drops clearfix drops-2">
          <span class="drop drop-a"></span>
          <span class="drop drop-b"></span>
          <span class="drop drop-c"></span>
          <span class="drop drop-d"></span>
          <span class="drop drop-e"></span>
          <span class="drop drop-f"></span>
          <span class="drop drop-g"></span>
          <span class="drop drop-h"></span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "login"
  }
</script>

<style scoped type="text/scss" lang="scss">
  *, :after, :before {
    box-sizing: border-box
  }
  .pull-left {
    float: left
  }
  .pull-right {
    float: right
  }
  .clearfix:after, .clearfix:before {
    content: '';
    display: table
  }
  .clearfix:after {
    clear: both;
    display: block
  }
  .login-back {
    width: 100%;
    height: 100%;
    background: #8ab7a0;
  }
  .boat {
    bottom: 20%;
    left: 50%;
    position: absolute;
    margin-left: -105px;
  }
  .boat .wrap {
    margin: auto;
    width: 210px;
    height: 150px;
    overflow: hidden;
    position: relative;
    padding: 50px 0 0 25px;
  }
  .boat {
    .main {
      bottom: -3px;
      position: relative;
      -webkit-animation: boat-start 1s infinite;
      animation: boat-start 1s infinite;
    }
    .boat-top-layer {
      .top {
        left: 70px;
        width: 55px;
        height: 30px;
        position: relative;
        border: 2px solid #fff;
        &:before {
          top: 50%;
          left: -2px;
          height: 2px;
          width: inherit;
          margin-top: -1px;
        }
        &:after {
          top: -30px;
          width: 2px;
          right: -2px;
          height: 35px;
        }
        .pole {
          width: 2px;
          left: -2px;
          z-index: 1;
          height: 50px;
          bottom: -8px;
          background: #fff;
          position: absolute;
          &:before {
            top: -5px;
            left: 50%;
            width: 15px;
            height: 8px;
            border-radius: 4px;
            margin-left: -7.5px;
          }
          &:after {
            bottom: 0;
            left: 30px;
            width: 2px;
            height: 35px;
          }
        }
        .help {
          z-index: 1;
          width: 30px;
          height: 30px;
          margin-top: -2px;
          margin-left: -1px;
          position: relative;
          border-radius: 50%;
          border: 8px solid #f04850;
          &:before {
            height: 2px;
            width: inherit;
            margin-top: -1px;
            margin-left: -15px;
          }
          &:after {
            width: 2px;
            height: inherit;
            margin-top: -15px;
            margin-left: -1px;
          }
          span {
            top: -2px;
            width: 14px;
            height: 14px;
            overflow: hidden;
            border-radius: 50%;
            position: relative;
            display: inline-block;
            &:before {
              width: 2px;
              height: inherit;
              margin-top: -7px;
              margin-left: -1px;
            }
            &:after {
              height: 2px;
              width: inherit;
              margin-top: -1px;
              margin-left: -7px;
            }
          }
        }
      }
      .bottom {
        left: 55px;
        height: 5px;
        width: 75px;
        position: relative;
        background: #688b77;
        border-radius: 5px 3px 0 0;
        &:before {
          left: 8px;
          top: -30px;
          width: 5px;
          height: 35px;
          -webkit-transform: skewX(-25deg);
          transform: skewX(-25deg);
        }
        &:after {
          bottom: 0;
          left: 30px;
          width: 2px;
          height: 85px;
        }
      }
    }
    .boat-mid-layer {
      .top {
        left: 60px;
        width: 70px;
        height: 20px;
        position: relative;
        background: #222e28;
        border-top: 5px solid #fff;
        border-right: 5px solid #fff;
        &:before {
          top: -5px;
          left: -10px;
          width: 18px;
          height: inherit;
          background: inherit;
          border-top: inherit;
          border-right: inherit;
          border-left: 5px solid #fff;
          -webkit-transform: skewX(-25deg);
          transform: skewX(-25deg);
        }
        &:after {
          top: -5px;
          width: 5px;
          height: 5px;
          right: -10px;
          background: #fff;
          border-radius: 0 3px 3px 0;
        }
      }
      .bottom {
        left: 25px;
        width: 105px;
        height: 12px;
        background: #fff;
        position: relative;
        &:before {
          left: -5px;
          width: 10px;
          height: inherit;
          background: inherit;
          border-radius: 3px 0 0 0;
          -webkit-transform: skewX(-25deg);
          transform: skewX(-25deg);
        }
        &:after {
          top: 3px;
          right: 5px;
          height: 5px;
          width: 20px;
          background: #d0e2d7;
        }
      }
    }
    .boat-bot-layer {
      .top {
        left: -10px;
        height: 5px;
        width: 180px;
        position: relative;
        background: #688b77;
        border-radius: 5px 5px 0 0;
        &:before {
          left: 10px;
        }
        &:after {
          right: 25px;
        }
      }
      .bottom {
        width: 180px;
        height: 25px;
        position: relative;
        border-radius: 2px;
        background: #222e28;
        &:before {
          left: -15px;
          width: 25px;
          height: 25px;
          background: inherit;
          border-radius: inherit;
          -webkit-transform: skewX(25deg);
          transform: skewX(25deg);
        }
        &:after {
          top: -13px;
          left: 28px;
          width: 5px;
          height: 5px;
          border-radius: 50%;
          background: inherit;
        }
      }
    }
    .water {
      bottom: 0;
      left: 150px;
      position: absolute;
      .drops {
        width: 300px;
        height: 22px;
        position: relative;
      }
      .drop {
        left: 0;
        bottom: 0;
        background: #fff;
        position: absolute;
        &.drop-a {
          width: 10px;
        }
        &.drop-c {
          left: 37px;
          width: 32px;
          height: 7px;
          border-radius: 6px 6px 0 0;
          &:before {
            left: 0;
            top: -5px;
          }
          &:after {
            top: -8px;
            right: 5px;
            width: 4px;
            height: 4px;
          }
        }
        &.drop-d {
          left: 68px;
          width: 25px;
          height: 10px;
          border-radius: 10px 10px 0 0;
          &:before {
            top: -8px;
            left: 8px;
          }
          &:after {
            top: -2px;
            right: -8px;
          }
        }
        &.drop-e {
          left: 93px;
        }
        &.drop-f {
          width: 50px;
          left: 115px;
          height: 4px;
        }
        &.drop-g {
          left: auto;
          right: 75px;
          width: 40px;
          height: 2.5px;
          &:before {
            top: -5px;
            left: -5px;
          }
          &:after {
            left: 100%;
            width: 12px;
            height: inherit;
          }
        }
        &.drop-h {
          left: auto;
          right: 25px;
          height: 2px;
          width: 25px;
          &:before {
            left: 30px;
            width: 10px;
          }
          &:after {
            left: 45px;
            width: 4px;
          }
        }
      }
      .drops-2 {
        bottom: 0;
        left: 30px;
        position: absolute;
        .drop {
          &.drop-a {
            width: 15px;
            border-radius: 5px 5px 0 0;
          }
          &.drop-b {
            height: 10px;
            border-radius: 10px 10px 0 0;
          }
          &.drop-c {
            &:before {
              left: 10px;
              top: -10px;
            }
            &:after {
              top: -12px;
              right: -25px;
            }
          }
          &.drop-d {
            height: 8px;
            &:before {
              top: -15px;
              left: 35px;
            }
            &:after {
              top: -8px;
              right: -55px;
            }
          }
          &.drop-g {
            &:before {
              right: 0;
              top: -10px;
              left: auto;
            }
          }
          &.drop-h {
            bottom: 0;
            width: 10px;
            left: auto;
            height: 5px;
            right: 45px;
            border-radius: 5px 5px 0 0;
          }
        }
      }
    }
  }
  .boat .boat-top-layer .top:before,
  .boat .boat-top-layer .top:after,
  .boat .boat-top-layer .top .pole:before,
  .boat .boat-top-layer .top .pole:after,
  .boat .boat-top-layer .top .help:before,
  .boat .boat-top-layer .top .help:after,
  .boat .boat-top-layer .top .help span:before,
  .boat .boat-top-layer .top .help span:after,
  .boat .boat-top-layer .bottom:before,
  .boat .boat-top-layer .bottom:after,
  .boat .boat-mid-layer .top:before,
  .boat .boat-mid-layer .top:after,
  .boat .boat-mid-layer .bottom:before,
  .boat .boat-mid-layer .bottom:after,
  .boat .boat-bot-layer .top:before,
  .boat .boat-bot-layer .top:after,
  .boat .boat-bot-layer .bottom:before,
  .boat .boat-bot-layer .bottom:after,
  .boat .water .drop:before,
  .boat .water .drop:after {
    content: '';
    position: absolute;
  }
  /* top - top */
  .boat .boat-top-layer .top:before,
  .boat .boat-top-layer .top:after {
    background: #fff;
  }
  .boat .boat-top-layer .top .pole:before,
  .boat .boat-top-layer .top .pole:after {
    position: absolute;
    background: inherit;
  }
  .boat .boat-top-layer .top .help:before,
  .boat .boat-top-layer .top .help:after {
    top: 50%;
    left: 50%;
    position: absolute;
    background: rgba(0, 0, 0, .3);
  }
  .boat .boat-top-layer .top .help span:before,
  .boat .boat-top-layer .top .help span:after {
    top: 50%;
    left: 50%;
    z-index: 1;
    background: #fff;
    position: absolute;
  }
  /* top - bottom */
  .boat .boat-top-layer .bottom:before,
  .boat .boat-top-layer .bottom:after {
    background: #fff;
  }
  /* middle - top */
  /* middle - bottom */
  /* bottom - top */
  .boat .boat-bot-layer .top:before,
  .boat .boat-bot-layer .top:after {
    width: 5px;
    height: 5px;
    bottom: 100%;
    background: #222e28;
    border-radius: 2px 2px 0 0;
  }
  /* bottom - bottom */
  .boat .water .drop:before,
  .boat .water .drop:after {
    background: inherit;
    border-radius: inherit;
  }
  .boat .water .drop.drop-a,
  .boat .water .drop.drop-b,
  .boat .water .drop.drop-e,
  .boat .water .drop.drop-f,
  .boat .water .drop.drop-g {
    height: 5px;
    border-radius: 3px 3px 0 0;
  }
  .boat .water .drop.drop-b,
  .boat .water .drop.drop-e,
  .boat .water .drop.drop-f,
  .boat .water .drop.drop-g {
    left: 15px;
    width: 22px;
  }
  .boat .water .drop.drop-c:before,
  .boat .water .drop.drop-c:after,
  .boat .water .drop.drop-d:before,
  .boat .water .drop.drop-d:after,
  .boat .water .drop.drop-g:before {
    width: 2px;
    height: 2px;
    border-radius: 50%;
  }
  .boat .water .drop.drop-h:before,
  .boat .water .drop.drop-h:after {
    height: inherit;
  }
  .boat .water .drops-2 .drop.drop-h:before,
  .boat .water .drops-2 .drop.drop-h:after {
    display: none;
  }
  .drops-1 {
    -webkit-animation: blink .8s linear infinite;
    animation: blink .8s linear infinite;
  }
  .drops-2 {
    -webkit-animation: blink 1.6s linear infinite;
    animation: blink 1.6s linear infinite;
  }
  @keyframes boat-start {
    0% {
      transform: none;
    }
    50% {
      transform: translateY(4px);
    }
    100% {
      transform: none;
    }
  }
  @keyframes blink {
    25% {
      visibility: hidden;
    }
    50% {
      visibility: hidden;
    }
    100% {
      visibility: visible;
    }
  }
</style>