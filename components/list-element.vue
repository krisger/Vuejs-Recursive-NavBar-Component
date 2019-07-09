<template>
  <li :key="id">
    <a v-if="link" :href="link">{{name}}</a>
    <span v-else-if="!link" :href="link">{{name}}</span>
    <slot></slot>
  </li>
</template>

<script>
export default {
  name: "ListElement",
  props: {
    name: String,
    link: String,
    id: Number
  }
};
</script>