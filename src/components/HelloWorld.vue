
<template>
  <div
   v-bind="data.attrs"
   :class="data.staticClass"
   :style="data.staticStyle"
   v-on="listeners"
  >
    <slot/>
  </div>
</template>