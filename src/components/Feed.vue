<template lang="html">
  <div class="feed">
    <div class="timeline">
      <!-- card-feed holds all the cards -->
      <div id="card-feed">
        <div class="header-feed">
          <h1 class="header">Feed</h1>
        </div>
        <!-- Dynaimc cards will be gerneated here -->
      </div>
    </div>
  </div>
</template>

<script>
export default {
}
</script>

<style lang="sass">
  // feed holds the timeline
  .feed
    position: absolute
    width: 100vw
    height: auto
    //background: red
    margin-top: 30px
    margin-bottom: 40px
    padding-bottom: 40px
    .timeline
      height: 100vh
      width: 100vw
      //background: yellow

  #card-feed
    //background: blue
    display: flex
    flex-direction: column
    align-items: flex-start
    height: auto
    padding-bottom: 90px
    width: 100%


  // Header-feed holds the header 'feed'
  .header-feed
    align-self: flex-start
    color: white

  .header-feed .header
    margin-left: 15px
    font-family: sans-serif 'Roboto'
    //font-size:

  #card
    position: relative
    background: #393636
    width: 90vw
    max-height: auto
    height: auto
    min-height: 70px
    margin: 8px
    margin-left: 15px
    border-radius: 12px
    box-shadow: 2px 8px 30px 3px #2E2E2E

  #name
    position: absolute
    width: 40px
    left: 48.5px
    top: 15px
    font-family: sans-serif 'Roboto'
    font-size: 10.5px
    color: white

  #profile-pic
    position: relative
    top: 10px
    left: 14px
    background: #1C1B1B
    height: 28px
    width: 28px
    border-radius: 50%

  #time
    position: absolute
    font-size: 9.3px
    color: #BBBBBB
    right: 20px
    top: 15px
    //background: red
    display: inline-block

  #content-box
    position: relative
    top: 8px
    left: 48.5px
    width: 71%
    height: auto
    //background-color: #2F2D2D
    border-radius: 8px
    min-width: 65%
    margin-bottom: 16px
    color: white
    word-wrap: break-word

  #content-box p
    font-size: 12.1px
    color: white

  @media(min-width: 600px){}
</style>
