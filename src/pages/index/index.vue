<template>
  <div>
    <i-grid i-class="no-border">
    <i-grid-item i-class="no-border">
        <i-grid-icon>
            <image src="/static/images/1.png" />
        </i-grid-icon>
        <i-grid-label>经典文学</i-grid-label>
    </i-grid-item>
     <i-grid-item i-class="no-border">
        <i-grid-icon>
            <image src="/static/images/2.png"/>
        </i-grid-icon>
        <i-grid-label>推理悬疑</i-grid-label>
    </i-grid-item>
     <i-grid-item i-class="no-border">
        <i-grid-icon>
            <image src="/static/images/3.png" />
        </i-grid-icon>
        <i-grid-label>都市言情</i-grid-label>
    </i-grid-item>
     <i-grid-item i-class="no-border">
        <i-grid-icon>
            <image src="/static/images/4.png" />
        </i-grid-icon>
        <i-grid-label>外国著作</i-grid-label>
    </i-grid-item>
    </i-grid>
    <i-panel title="热门">
    <view style="padding: 15px;">PANEL 内容区域</view>
</i-panel>
  </div>
  </template>

<script>
export default {
  data () {
    return {
      
      }
  },


  methods: {
  
    },
 

  created () {
   
  }
}
</script>

<style scoped>
div >>> .no-border {
  border-width: 0pt;
}
div >>> .split {
  margin-bottom: 10pt;
}
</style>
