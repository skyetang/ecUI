<template>
  <transition name="page-fade">
    <div class="info-page">
      <div class="page-wrapper">
        <div class="page-header">
          <div class="header-item"><i class="gray icon-return" @click="close"></i></div>
          <div class="header-item">
            <slot name="title">
              {{title}}
          </slot>
          </div>
          <div class="header-item"><i class="gray icon-innerpage__close" @click="close"></i></div>
        </div>
        <div class="page-body">
          <div class="page-content">
            <slot></slot>
          </div>
        </div>
        <div class="page-footer">
          <slot name="footer">
            <ec-button>取消</ec-button>
            <ec-button>保存</ec-button>
          </slot>
        </div>
      </div>
    </div>
  </transition>
</template>

<script>
  export default {
    name: 'EcPage',
    props: {
      title: {
        type: String,
        default: '详情页'
      }
    },
    methods: {
      close() {
        this.$emit('close');
      }
    }
  };
</script>


