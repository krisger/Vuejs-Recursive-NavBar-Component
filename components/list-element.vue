<template>
  <li :key="id">
    <a v-if="link" :href="link">{{name}}</a>
    <span v-else-if="!link" :href="link">{{name}}</span>
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