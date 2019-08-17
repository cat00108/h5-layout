<template>
  <div id="page">
    <div id="hd">
      <div class="head">
        head
      </div>
    </div>
    <div id="bd">
      <p>1</p>
      <p>2</p>
      <p>3</p>
      <p>4</p>
      <p>5</p>
      <p>6</p>
      <p>7</p>
      <p>8</p>
      <p>9</p>
      <p>10</p>
      <p>11</p>
      <p>12</p>
      <p>13</p>
      <p>14</p>
      <p>15</p>
      <p>16</p>
    </div>
    <div id="ft">
      <div class="foot">
        foot
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="stylus" scoped>
@import '../assets/style/mixin.styl'
  $gray=rgba(22, 24, 35, 0.2)
  $red=#fe2c55
  .l-flex-certer-middle {
    display: flex;
    justify-content: center;
    align-items: center;
  }
  // 1PX
  .l-border-bottom {
    border-bottom: 1PX solid $gray;
  }
  #page {
    display: flex;
    flex-direction: column;
    position: relative;
    height: 100vh;
    overflow: hidden;
  }
  .head {
    // iphonex 适配
    adapterIphoneXTop();
    box-sizing: content-box;
    height: 100px;
    background-color: #000;
    color: #fff;
    @extend .l-flex-certer-middle;
    @extend .l-border-bottom;
  }
  .foot {
    // iphonex 适配
    adapterIphoneXBottom();
    box-sizing: content-box;
    height: 100px;
    background-color: $red;
    border-top: 1PX solid $gray;
    @extend .l-flex-certer-middle;
  }
  #bd {
    flex-grow: 1;
    overflow-y: auto;
    -webkit-overflow-scrolling: touch;

  }
</style>
