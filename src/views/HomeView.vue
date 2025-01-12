<template>
  <div class="wrap">
    <main>
      <section class="title">
        <div class="img-wrap">
          <div class="words-beauty">
            <img src="../assets/img/titleBeauty.png" alt="title-beauty">
          </div>
          <div class="words-one">
            <img src="../assets/img/titleOne.png" alt="title-one">
          </div>
        </div>
      </section>
      <section class="intro">
        <h1 ref="target" class="text-light move">
          <p class="slogan">BEAUTY ONE</p>
          <p class="slogan">MAKES YOU BE THE BEAUTIFUL ONE</p>
          <p class="content">—— 讓我們與您一起尋找凍齡的秘密 ——</p>
        </h1>
      </section>
      <section class="information">
        <div ref="target2" class="inner move">
          <h2 class="flash-title">快閃店資訊</h2>
          <div class="messege">
            <p>
              活動地點 : 雲林縣斗六市民生路27號
            </p><br>
            <p>
              活動時間 : 2025年1月10日(星期五)11:00至2025年1月22日(星期三)
            </p>
          </div>
          <div class="discount">
            <p class="activity text-light">
              優惠活動
            </p>
            <p>
              活動期間打卡即享100元折扣，一人僅限一次。
            </p>
          </div>
        </div>
      </section>
      <section class="goods">
        <div ref="target3" class="inner move">
          <h2 class="flash-title text-light">快閃店商品</h2>
          <div class="item-box">
            <div class="card">
              <img src="../assets/img/goods/fragrance.jpg" class="card-img-top" alt="fragrance">
              <div class="card-body">
                <h5 class="card-title">白茶香氛</h5>
                <p class="card-text">NT$400</p>
              </div>
            </div>
            <div class="card">
              <div class="new"></div>
              <div class="new-item">新品</div>
              <img src="../assets/img/goods/shampoo.jpg" class="card-img-top" alt="shampoo">
              <div class="card-body">
                <h5 class="card-title">溫和洗髮精</h5>
                <p class="card-text">NT$330</p>
              </div>
            </div>
            <div class="card">
              <div class="new"></div>
              <div class="new-item">新品</div>
              <img src="../assets/img/goods/oil.jpg" class="card-img-top" alt="oil">
              <div class="card-body">
                <h5 class="card-title">火山泥精華</h5>
                <p class="card-text">NT$620</p>
              </div>
            </div>
          </div>
          <div class="item-box">
            <div class="card">
              <img src="../assets/img/goods/essense.jpg" class="card-img-top" alt="essense">
              <div class="card-body">
                <h5 class="card-title">黑豆茶精油</h5>
                <p class="card-text">NT$550</p>
              </div>
            </div>
            <div class="card">
              <img src="../assets/img/goods/lotion.jpg" class="card-img-top" alt="lotion">
              <div class="card-body">
                <h5 class="card-title">保濕乳液組</h5>
                <p class="card-text">NT$699</p>
              </div>
            </div>
            <div class="card">
              <img src="../assets/img/goods/lip.jpg" class="card-img-top" alt="lip">
              <div class="card-body">
                <h5 class="card-title">玫瑰油唇膜</h5>
                <p class="card-text">NT$220</p>
              </div>
            </div>
          </div>
          <div class="item-box">
            <div class="card">
              <div class="new"></div>
              <div class="new-item">新品</div>
              <img src="../assets/img/goods/white.jpg" class="card-img-top" alt="set">
              <div class="card-body">
                <h5 class="card-title">滋養洗護系列</h5>
                <p class="card-text">NT$999</p>
              </div>
            </div>
            <div class="card">
              <img src="../assets/img/goods/black.jpg" class="card-img-top" alt="set">
              <div class="card-body">
                <h5 class="card-title">控油洗護系列</h5>
                <p class="card-text">NT$999</p>
              </div>
            </div>
            <div class="card">
              <img src="../assets/img/goods/body.jpg" class="card-img-top" alt="bodylotion">
              <div class="card-body">
                <h5 class="card-title">美白身體乳</h5>
                <p class="card-text">NT$310</p>
              </div>
            </div>
          </div>
        </div>
      </section>
    </main>
    <footer class="footer">
      <div class="copyright">
        <p>2024 &copy; By BEAUTY ONE All Rights Reserved &emsp;</p>
        <p>個人練習作品 &nbsp; 非商業用途</p>
      </div>
    </footer>
  </div>
</template>

<script>

export default {
  data () {
    return {
      isFadedIn: false
    }
  },
  mounted () {
    window.addEventListener('scroll', this.scrolling)
  },
  methods: {
    scrolling () {
      const targets = [this.$refs.target, this.$refs.target2, this.$refs.target3]
      targets.forEach(target => {
        const targetPos = target.getBoundingClientRect().top
        const scrollPos = window.scrollY
        const targetHeight = target.offsetHeight
        const windowHeight = window.innerHeight
        const isFadedIn = target.classList.contains('fade-in')
        if (!isFadedIn && targetPos + targetHeight >= scrollPos && targetPos <= windowHeight * 0.6) {
          target.classList.add('fade-in')
          this.isFadedIn = true
        }
      })
    }
  }
}
</script>
