<template>
  <div class="wrapperInner">
      <div class="tabs">
        <button @click="selectTab(tabitem.id)"
                v-for="tabitem in tabContent" :key="tabitem.id"
                class="btnTabs">
                {{ tabitem.title }}
        </button>
      </div>
      <div v-for="tabitem in tabContent"
           v-if="currentTab == tabitem.id" class="contents" v-html="tabitem.content"
           >
          
      </div>

  </div>
</template>

<script>
  export default {
    props: {
      tabContent: Array,
    },
    data: function() {
      return {
        currentTab: 1
      }
    },
    methods: {
      selectTab(selectedTab){
        this.currentTab = selectedTab
      }
    }
  }
</script>

<style scoped>
.wrapperInner{
    width: calc(100% - 10px);
    margin: 5px;
    height: calc(100% - 10px);
}
.tabs{
    width: 20%;
    height: calc(100% - 60px);
    float: left;
    background: rgba(0, 0, 0, 0.75);
    border-radius: 5px 0px 0px 5px;
}
button{
    border: 0px;
    width: 100%;
    height: 50px;
    border-bottom: 1px solid;
    border-image-source: linear-gradient(-2deg, rgba(36,161,253,1) 0%, rgba(0,255,205,1) 100%);
    border-image-slice: 1;
    background: rgba(0, 0, 0, 0.1);
    color: white;
    text-align: left;
    font-size: 15px;
    line-height: 50px;
    float: left;
    padding-left: 15px;
}
button:focus{
    background: rgba(0, 0, 0, 0.75);
    outline: 0px;
    color: rgba(0,255,205,1);
}
button:hover{
    cursor: pointer;
    background: rgba(0, 0, 0, 0.75);
    color: rgba(0,255,205,1);
}
.contents{  
    background: rgba(0, 0, 0, 0.75);
    overflow: scroll;
    width: calc(80% - 25px);
    height: calc(100% - 80px);
    float: left;
    margin-left: 5px;
    padding: 10px;
    color: white;
    border-radius: 0px 5px 5px 0px;
}
::-webkit-scrollbar {
  width: 0px;
}
</style>