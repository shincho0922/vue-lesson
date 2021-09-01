<template>
  <div>
    <h2>{{ title }}</h2>
    <slot name="head"></slot>
    <slot>default slot</slot>
    <slot name="foot"></slot>
  </div>
</template>

<script>
  export default {
    // Vueインスタンスが破棄される直前に実行されます。
    beforeDestroy() {
      console.log('beforeDestroy');
    },
    // Vueインスタンスが破棄された後に呼び出されます。
    destroyed() {
      console.log('destroyed');
    },
    props: {
      title: {
        type: String,
      }
    }
  }
</script>