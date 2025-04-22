<template>
  <div class="counter-warp">
    <p>Vuex counter： {{ count }}</p>
    <p>
      <button @click="increment">+</button>
      <button @click="decrement">-</button>
    </p>
    <canvas id="testCanvas"></canvas>
    <a @click="goBack()" class="home">返回首页</a>
  </div>
</template>

<script>
// Use Vuex
import { mapState, mapActions } from 'vuex'
export default {
  computed: {
    ...mapState({
      count: state => state.counter.count
    })
  },
  mounted () {
    this.getProvince({
      testParams: '1'
    }).then(res => {
      console.log(res)
    })
    wx.cavasToTempFilePath({
      x: 0,
      y: 0,
      width: 100,
      height: 100,
      distWidth: 100 * 1,
      distHeight: 100 * 1,
      success: function (res) {
        console.log(res)
      }
    })
  },
  methods: {
    ...mapActions('counter', [
      'increment',
      'decrement',
      'getProvince'
    ]),
    goBack () {
      wx.navigateBack({
        url: '/pages/index/index'
      })
    }
  }
}

</script>
<style>
.counter-warp {
  text-align: center;
  margin-top: 100px;
}

.home {
  display: inline-block;
  margin: 100px auto;
  padding: 5px 10px;
  color: blue;
  border: 1px solid blue;
}
</style>
