<template>
  <div class="test">
        <div class="topbar">
          {{ headertitle }}
        <div class="xbutton"></div>
    </div>
    <Tab :tabContent="tabDatas"></Tab>
  </div>
</template>

<script>
import Tab from './Tab'

  export default {
    components: {
      Tab
    },
    data: function() {
      return {
        headertitle: 'Anfängerguide',
        tabDatas: [
          {id: 1, title: "test1", content:'<h1>test</h1>'},
          {id: 2, title: "test2", content:"irgendwas as2"},
          {id: 3, title: "test3", content:"irgendwas as3"},
        ]
      }
    }
  }
</script>

<style scoped>
.test{
  width: 100%;
  height: 100%;
}
 .topbar{
    width: 100%;
    height: 60px;
    background: rgb(0,145,255);
    background: linear-gradient(235deg, rgba(0,145,255,1) 0%, rgba(0,212,255,1) 100%);
    color: black;
    font-size: 20px;
    text-align: center;
    line-height: 60px;
    text-transform: uppercase;
    border-radius: 5px 5px 0px 0px;
    font-weight: 500;
    
  }
  .xbutton {
      width: 60px;
      height: 60px;
      position: absolute;
      top: 15vh;
      right: calc(20vw - 8px);
      border-radius: 0px 5px 0px 0px;
      background-color: rgba(0, 0, 0, 0.0);
      background-image: url('../assets/close.svg');
      background-size: 40%;
      background-repeat: no-repeat;
      background-position: center;
      color: white;
  }
  .xbutton:hover {
      cursor: pointer;
      background-color: rgba(0, 0, 0, 0.1);
  }
</style>