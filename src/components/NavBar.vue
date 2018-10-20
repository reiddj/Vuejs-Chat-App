<template lang="html">
  <div class="navbar">
    <svg xmlns="http://www.w3.org/2000/svg" class="cross" xmlns:xlink="http://www.w3.org/1999/xlink" style="isolation:isolate" viewBox="-32 116 18 18" width="18" height="18"><switch><g><path d=" M -20.882 122.882 L -20.882 118.118 C -20.882 116.949 -21.831 116 -23 116 L -23 116 C -24.169 116 -25.118 116.949 -25.118 118.118 L -25.118 122.882 L -29.882 122.882 C -31.051 122.882 -32 123.831 -32 125 L -32 125 C -32 126.169 -31.051 127.118 -29.882 127.118 L -25.118 127.118 L -25.118 131.882 C -25.118 133.051 -24.169 134 -23 134 L -23 134 C -21.831 134 -20.882 133.051 -20.882 131.882 L -20.882 127.118 L -16.118 127.118 C -14.949 127.118 -14 126.169 -14 125 L -14 125 C -14 123.831 -14.949 122.882 -16.118 122.882 L -20.882 122.882 Z " fill-rule="evenodd" id="Compound Shape" fill="#882795"/></g><foreignObject requiredExtensions="http://ns.gravit.io/"> xlink:href="#BaIRjyBCfsPsQxBRCDtZA2xZC0GJlNiD"/></foreignObject></switch></svg>
    <div class="profile-circ"></div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="sass">
  .navbar
    position: relative
    display: flex
    align-items: center
    //background: black
    height: 60px
    width: 100vw

  .cross
    position: relative
    left: 20px

  .profile-circ
    position: absolute
    right: 20px
    width: 30px
    height: 30px
    background-color: #882795
    border-radius: 50%
</style>
