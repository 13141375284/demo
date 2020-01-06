<!--
 * @掘金: https://juejin.im/user/5c4ebc72e51d4511dc7306ce
 * @LastEditTime: 2019-11-13 10:43:09
 * @Description: 首页->限时抢购
 * @FilePath: /ddBuy/src/views/home/components/flash/FlashFood.vue
 -->
<template>
  <div>
    <div id="flashFood">
      <div class="titleWrapper">
        <div class="title">限时抢购</div>
        <van-count-down :time="time" class="countStyle" format="HH mm ss">
          <template v-slot="timeData">
            <span class="item">{{ timeData.hours }}</span>
            <span class="item">{{ timeData.minutes }}</span>
            <span class="item">{{ timeData.seconds }}</span>
          </template>
        </van-count-down>
        <!-- 更多按钮 -->
      </div>

      <!-- 限时抢购商品 遍历父组件传来的数据并传递给子组件-->
      <FlashFood :flash_sale_product_list="flash_sale_product_list" />
      <div class="flashItemwrapper">
        <ul class="itemWrapper" ref="ulWrapper">
          <li
            class="itemInCovers"
            v-for="(product,index) in flash_sale_product_list"
            :key="product.id"
            ref="productItem"
          >
            <img v-lazy="product.small_image" class="itemImage" />
            <span class="title">{{product.name}}</span>
            <div class="price">
              <p class="nowPrice">{{product.price | moneyFormat}}</p>
              <p class="originPrice">{{product.origin_price | moneyFormat}}</p>
              <div class="buyCar" @click="addToCart(product)">
                <svg viewBox="0 0 52 52" class="icon icon-60">
                  <defs>
                    <radialGradient
                      cx="27.0288363%"
                      cy="10.3693483%"
                      fx="27.0288363%"
                      fy="10.3693483%"
                      r="93.8427229%"
                      id="radialGradient-1"
                    >
                      <stop stop-color="#4ECA75" offset="0%" />
                      <stop stop-color="#39B460" offset="100%" />
                    </radialGradient>
                  </defs>
                  <g stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
                    <g transform="translate(-678.000000, -2742.000000)">
                      <g transform="translate(678.000000, 2742.000000)">
                        <rect
                          fill="url(#radialGradient-1)"
                          x="0"
                          y="0"
                          width="51.8699976"
                          height="51.8699976"
                          rx="25.9349988"
                        />
                        <path
                          fill="#FFFFFF"
                          d="M20.3666667,39 C19.1700497,39 18.2,38.0299503 18.2,36.8333333 C18.2,35.6367164 19.1700497,34.6666667 20.3666667,34.6666667 C21.5632836,34.6666667 22.5333333,35.6367164 22.5333333,36.8333333 C22.5333333,38.0299503 21.5632836,39 20.3666667,39 Z M33.3666667,38.1333333 C32.1700497,38.1333333 31.2,37.1632836 31.2,35.9666667 C31.2,34.7700497 32.1700497,33.8 33.3666667,33.8 C34.5632836,33.8 35.5333333,34.7700497 35.5333333,35.9666667 C35.5333333,37.1632836 34.5632836,38.1333333 33.3666667,38.1333333 Z"
                        />
                        <path
                          stroke="#FFFFFF"
                          stroke-width="2.6"
                          stroke-linecap="round"
                          d="M12.1333333,13.8666667 L13.6768756,13.8666667 C15.4621209,13.8666667 16.9554584,15.222463 17.1274221,16.9994069 L18.2224287,28.314386 C18.4068512,30.2200702 20.1012175,31.6154285 22.0069016,31.431006 C22.0111286,31.4305969 22.0153548,31.4301801 22.0195802,31.4297555 L33.2997819,30.296256 C34.7947282,30.1460352 36.0227397,29.0499108 36.3411182,27.581556 L37.8958814,20.4110205 C38.0987345,19.4754663 37.5047629,18.5526049 36.5692087,18.3497518 C36.3853963,18.3098964 36.1963225,18.3002236 36.0094025,18.3211126 L22.8968424,19.7864909"
                        />
                      </g>
                    </g>
                  </g>
                </svg>
              </div>
            </div>
          </li>
        </ul>
      </div>
    </div>
    <div id="flashFood">
      <div class="titleWrapper">
        <div class="title">美易购</div>
      </div>

      <!-- 限时抢购商品 遍历父组件传来的数据并传递给子组件-->
      <FlashFood :flash_sale_product_list="flash_sale_product_list" />
      <div class="flashItemwrapper">
        <ul class="itemWrapper" ref="ulWrapper">
          <li
            class="itemInCovers"
            v-for="(product,index) in flash_sale_product_list"
            :key="product.id"
            ref="productItem"
          >
            <img v-lazy="product.small_image" class="itemImage" />
            <span class="title">{{product.name}}</span>
            <div class="price">
              <p class="nowPrice">{{product.price | moneyFormat}}</p>
              <p class="originPrice">{{product.origin_price | moneyFormat}}</p>
              <div class="buyCar" @click="addToCart(product)">
                <svg viewBox="0 0 52 52" class="icon icon-60">
                  <defs>
                    <radialGradient
                     
                      cy="10.3693483%"
                       cx="27.0288363%"
                      fx="27.0288363%"
                      fy="10.3693483%"
                      r="93.8427229%"
                      id="radialGradient-1"
                    >
                      <stop stop-color="#4ECA75" offset="0%" />
                      <stop stop-color="#39B460" offset="100%" />
                    </radialGradient>
                  </defs>
                  <g stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
                    <g transform="translate(-678.000000, -2742.000000)">
                      <g transform="translate(678.000000, 2742.000000)">
                        <rect
                          fill="url(#radialGradient-1)"
                          x="0"
                          y="0"
                          width="51.8699976"
                          height="51.8699976"
                          rx="25.9349988"
                        />
                        <path
                          fill="#FFFFFF"
                          d="M20.3666667,39 C19.1700497,39 18.2,38.0299503 18.2,36.8333333 C18.2,35.6367164 19.1700497,34.6666667 20.3666667,34.6666667 C21.5632836,34.6666667 22.5333333,35.6367164 22.5333333,36.8333333 C22.5333333,38.0299503 21.5632836,39 20.3666667,39 Z M33.3666667,38.1333333 C32.1700497,38.1333333 31.2,37.1632836 31.2,35.9666667 C31.2,34.7700497 32.1700497,33.8 33.3666667,33.8 C34.5632836,33.8 35.5333333,34.7700497 35.5333333,35.9666667 C35.5333333,37.1632836 34.5632836,38.1333333 33.3666667,38.1333333 Z"
                        />
                        <path
                          stroke="#FFFFFF"
                          stroke-width="2.6"
                          stroke-linecap="round"
                          d="M12.1333333,13.8666667 L13.6768756,13.8666667 C15.4621209,13.8666667 16.9554584,15.222463 17.1274221,16.9994069 L18.2224287,28.314386 C18.4068512,30.2200702 20.1012175,31.6154285 22.0069016,31.431006 C22.0111286,31.4305969 22.0153548,31.4301801 22.0195802,31.4297555 L33.2997819,30.296256 C34.7947282,30.1460352 36.0227397,29.0499108 36.3411182,27.581556 L37.8958814,20.4110205 C38.0987345,19.4754663 37.5047629,18.5526049 36.5692087,18.3497518 C36.3853963,18.3098964 36.1963225,18.3002236 36.0094025,18.3211126 L22.8968424,19.7864909"
                        />
                      </g>
                    </g>
                  </g>
                </svg>
              </div>
            </div>
          </li>
        </ul>
      </div>
    </div>
    <div id="flashFood">
      <div class="titleWrapper">
        <div class="title">白菜价</div>
      
        <!-- 更多按钮 -->
      </div>

      <!-- 限时抢购商品 遍历父组件传来的数据并传递给子组件-->
      <FlashFood :flash_sale_product_list="flash_sale_product_list" />
      <div class="flashItemwrapper">
        <ul class="itemWrapper" ref="ulWrapper">
          <li
            class="itemInCovers"
            v-for="(product,index) in flash_sale_product_list"
            :key="product.id"
            ref="productItem"
          >
            <img v-lazy="product.small_image" class="itemImage" />
            <span class="title">{{product.name}}</span>
            <div class="price">
              <p class="nowPrice">{{product.price | moneyFormat}}</p>
              <p class="originPrice">{{product.origin_price | moneyFormat}}</p>
              <div class="buyCar" @click="addToCart(product)">
                <svg viewBox="0 0 52 52" class="icon icon-60">
                  <defs>
                    <radialGradient
                      cx="27.0288363%"
                      cy="10.3693483%"
                      fx="27.0288363%"
                      fy="10.3693483%"
                      r="93.8427229%"
                      id="radialGradient-1"
                    >
                      <stop stop-color="#4ECA75" offset="0%" />
                      <stop stop-color="#39B460" offset="100%" />
                    </radialGradient>
                  </defs>
                  <g stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
                    <g transform="translate(-678.000000, -2742.000000)">
                      <g transform="translate(678.000000, 2742.000000)">
                        <rect
                          fill="url(#radialGradient-1)"
                          x="0"
                          y="0"
                          width="51.8699976"
                          height="51.8699976"
                          rx="25.9349988"
                        />
                        <path
                          fill="#FFFFFF"
                          d="M20.3666667,39 C19.1700497,39 18.2,38.0299503 18.2,36.8333333 C18.2,35.6367164 19.1700497,34.6666667 20.3666667,34.6666667 C21.5632836,34.6666667 22.5333333,35.6367164 22.5333333,36.8333333 C22.5333333,38.0299503 21.5632836,39 20.3666667,39 Z M33.3666667,38.1333333 C32.1700497,38.1333333 31.2,37.1632836 31.2,35.9666667 C31.2,34.7700497 32.1700497,33.8 33.3666667,33.8 C34.5632836,33.8 35.5333333,34.7700497 35.5333333,35.9666667 C35.5333333,37.1632836 34.5632836,38.1333333 33.3666667,38.1333333 Z"
                        />
                        <path
                          stroke="#FFFFFF"
                          stroke-width="2.6"
                          stroke-linecap="round"
                          d="M12.1333333,13.8666667 L13.6768756,13.8666667 C15.4621209,13.8666667 16.9554584,15.222463 17.1274221,16.9994069 L18.2224287,28.314386 C18.4068512,30.2200702 20.1012175,31.6154285 22.0069016,31.431006 C22.0111286,31.4305969 22.0153548,31.4301801 22.0195802,31.4297555 L33.2997819,30.296256 C34.7947282,30.1460352 36.0227397,29.0499108 36.3411182,27.581556 L37.8958814,20.4110205 C38.0987345,19.4754663 37.5047629,18.5526049 36.5692087,18.3497518 C36.3853963,18.3098964 36.1963225,18.3002236 36.0094025,18.3211126 L22.8968424,19.7864909"
                        />
                      </g>
                    </g>
                  </g>
                </svg>
              </div>
            </div>
          </li>
        </ul>
      </div>
    </div>
    <div id="flashFood">
      <div class="titleWrapper">
        <div class="title">降价抢购</div>
      
        <!-- 更多按钮 -->
      </div>

      <!-- 限时抢购商品 遍历父组件传来的数据并传递给子组件-->
      <FlashFood :flash_sale_product_list="flash_sale_product_list" />
      <div class="flashItemwrapper">
        <ul class="itemWrapper" ref="ulWrapper">
          <li
            class="itemInCovers"
            v-for="(product,index) in flash_sale_product_list"
            :key="product.id"
            ref="productItem"
          >
            <img v-lazy="product.small_image" class="itemImage" />
            <span class="title">{{product.name}}</span>
            <div class="price">
              <p class="nowPrice">{{product.price | moneyFormat}}</p>
              <p class="originPrice">{{product.origin_price | moneyFormat}}</p>
              <div class="buyCar" @click="addToCart(product)">
                <svg viewBox="0 0 52 52" class="icon icon-60">
                  <defs>
                    <radialGradient
                      cx="27.0288363%"
                      cy="10.3693483%"
                      fx="27.0288363%"
                      fy="10.3693483%"
                      r="93.8427229%"
                      id="radialGradient-1"
                    >
                      <stop stop-color="#4ECA75" offset="0%" />
                      <stop stop-color="#39B460" offset="100%" />
                    </radialGradient>
                  </defs>
                  <g stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
                    <g transform="translate(-678.000000, -2742.000000)">
                      <g transform="translate(678.000000, 2742.000000)">
                        <rect
                          fill="url(#radialGradient-1)"
                          x="0"
                          y="0"
                          width="51.8699976"
                          height="51.8699976"
                          rx="25.9349988"
                        />
                        <path
                          fill="#FFFFFF"
                          d="M20.3666667,39 C19.1700497,39 18.2,38.0299503 18.2,36.8333333 C18.2,35.6367164 19.1700497,34.6666667 20.3666667,34.6666667 C21.5632836,34.6666667 22.5333333,35.6367164 22.5333333,36.8333333 C22.5333333,38.0299503 21.5632836,39 20.3666667,39 Z M33.3666667,38.1333333 C32.1700497,38.1333333 31.2,37.1632836 31.2,35.9666667 C31.2,34.7700497 32.1700497,33.8 33.3666667,33.8 C34.5632836,33.8 35.5333333,34.7700497 35.5333333,35.9666667 C35.5333333,37.1632836 34.5632836,38.1333333 33.3666667,38.1333333 Z"
                        />
                        <path
                          stroke="#FFFFFF"
                          stroke-width="2.6"
                          stroke-linecap="round"
                          d="M12.1333333,13.8666667 L13.6768756,13.8666667 C15.4621209,13.8666667 16.9554584,15.222463 17.1274221,16.9994069 L18.2224287,28.314386 C18.4068512,30.2200702 20.1012175,31.6154285 22.0069016,31.431006 C22.0111286,31.4305969 22.0153548,31.4301801 22.0195802,31.4297555 L33.2997819,30.296256 C34.7947282,30.1460352 36.0227397,29.0499108 36.3411182,27.581556 L37.8958814,20.4110205 C38.0987345,19.4754663 37.5047629,18.5526049 36.5692087,18.3497518 C36.3853963,18.3098964 36.1963225,18.3002236 36.0094025,18.3211126 L22.8968424,19.7864909"
                        />
                      </g>
                    </g>
                  </g>
                </svg>
              </div>
            </div>
          </li>
        </ul>
      </div>
    </div>
    <div class="images-my">
      <img class="card" src="~@/images/home/tu.png" ></img>
    </div>
  </div>  
</template>

<script type="text/javascript">
// 引入第三方组件
import FlashFood from "./FlashFood";
import BScroll from "better-scroll";
import { Toast } from "vant";
// 引入中央事件总线
import { mapMutations } from "vuex";
import { ADD_TO_CART } from "./../../../../config/pubsub_type.js";
export default {
  props: {
    flash_sale_product_list: Array
  },
  data() {
    return { time: 30 * 60 * 1000 * 100 };
  },
  mounted() {
    this.$nextTick(() => {
      let contentWrapperWidth = 0;
      let el = this.$refs.productItem;
      for (let i = 0; i < el.length; i++) {
        contentWrapperWidth += el[i].clientWidth;
      }
      // 给ul设置值
      this.$refs.ulWrapper.style.width = contentWrapperWidth + "px";
      if (!this.scroll) {
        // 名字一定要唯一 和父组件独立
        this.scroll = new BScroll(".flashItemwrapper", {
          probeType: 2,
          startX: 0,
          click: true,
          scrollX: true,
          scrollY: false,
          eventPassthrough: "vertical"
        });
      } else {
        this.scroll.refresh();
      }
    });
  },
  components: {},
  methods: {
    moreClick() {
      Toast({
        duration: 800
      });
    },
    // 添加到购物车
    ...mapMutations({
      addToCart: "ADD_TO_CART"
    })
  }
};
</script>
<style lang="less" scoped>
.titleWrapper{
  width: 100%;
  display: flex;
}
#flashFood {
  width: 42.5%;
  display:inline-block;
  margin: 0.4rem 0rem 0.4rem 0.4rem;
  padding: 0.5rem 0.5rem 0.5rem 0.5rem;
  background-color: white;
  border-radius: 5px;
  .flashItemwrapper {
    width: 100%;
    display: flex;
    overflow: hidden;
    .itemWrapper {
      display: flex;
      justify-content: flex-start;
    }
    .itemInCovers {
      // 设置子li的宽度

      flex: 0 0 8rem;
      align-items: center;
      padding-right: 1rem;
      .itemImage {
        width: 100%;
        // 等比缩小图片来适应元素的尺寸
        background-size: contain;
        background-image: url("../../../../images/placeholderImg/product-img-load.png");
      }
      .title {
        padding: 0.2rem;
        display: inline-block;
        font-size: 0.6258rem;
        height: 1rem;
        line-height: 1rem;
        font-size: 0.625rem;
        word-break: break-all;
        display: -webkit-box;
        overflow: hidden;
        text-overflow: ellipsis;
        -webkit-line-clamp: 2;
        -webkit-box-orient: vertical;
      }
      .price {
        position: relative;
        padding-left: 0.2rem;
        .nowPrice {
          color: #f37078;
          font-size: 0.928rem;
        }
        .originPrice {
          font-size: 0.6875rem;
          color: #999999;
          text-decoration: line-through;
        }
        .buyCar {
          position: absolute;
          right: 0.6rem;
          top: 0.1rem;
          width: 1.5rem;
          height: 1.5rem;
        }
      }
    }
  }
}
.title {
  display: inline-block;
  height: 1.3125rem;
  line-height: 1.3125rem;
  vertical-align: middle;
  font-size: 1.1rem;
  float: left;
}
.item {
  display: inline-block;
  width: 20px;
  height: 20px;
  margin-left: 0.2rem;
  margin-top: 0.18rem;
  color: #fff;
  font-size: 10px;
  border-radius: 5px;
  text-align: center;
  background-color: black;
}
.countStyle {
  float: right;
}

.more {
  color: #3cb963;
  float: right;
  font-size: 0.8rem;
}
.images-my{
  width: 100%;
}
.images-my img{
  width: 96%;
  margin: 0rem 0.4rem;
}
</style>
