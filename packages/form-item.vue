<template>
  <div class="jay-form-item">
    <label :style="labelStyle" class="jay-form-item_label">{{label}}</label>
    <div class="jay-form-item_content">
      <slot></slot>
    </div>
  </div>
</template>
<script>
export default {
  name: 'oneFormItem',
  props: {
    label: {
      type: String,
      default: ''
    }
  },
  inject: ['Form'],
  computed: {
    labelStyle () {
      return {
        width: this.Form.labelWidth
      }
    }
  }
}
</script>

<style lang="scss" scoped>
  .jay-form-item{
    margin-bottom: 25px;
    .jay-form-item_label{
      text-align: right;
      vertical-align: middle;
      float: left;
      font-size: 14px;
      color: #606266;
      line-height: 40px;
      padding: 0 12px 0 0;
      box-sizing: border-box;
    }
    .jay-form-item_content{
      line-height: 40px;
      position: relative;
      font-size: 14px;
      overflow: hidde;
    }
  }
</style>
