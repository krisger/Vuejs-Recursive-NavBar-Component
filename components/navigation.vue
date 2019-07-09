<template>
  <ul :class="'level-' + level">
    <ListElement
      v-for="item in list"
      v-bind:key="item"
      v-bind:name="item.name"
      v-bind:link="item.href"
      v-bind:id="item.id"
    >
      <NavBar
        v-if="typeof(item.childItems) != 'undefined'"
        :list="item.childItems"
        :level="item.level + 1"
      ></NavBar>
    </ListElement>
  </ul>
</template>

<script>
import ListElement from "./list-element.vue";
export default {
  name: "NavBar",
  components: {
    ListElement
  },
  props: {
    list: {
      type: Array
    },
    level: {
      type: Number,
      default: 0
    }
  },
  data: function() {
    return {};
  }
};
</script>
// Could be moved anywhere
// Currently minimaly styled only few levels.
<style scoped>
ul {
  list-style-type: none;
  padding: 0;
  text-align: left;
}

ul.level-0 {
  background-color: cornflowerblue;
  color: white;
}

ul.level-0 > li {
  display: inline-block;
  position: relative;
  margin-right: 15px;
  padding: 0px 15px;
}

ul.level-0 > li > a {
  padding: 15px 0px;
}

ul.level-1 > li:hover > ul,
ul.level-0 > li:hover > ul {
  display: block;
}

ul.level-1,
ul.level-2 {
  position: absolute;
  display: none;
  left: 0;
  top: 18px;
  background-color: royalblue;
}

ul.level-2 {
  left: 100%;
  top: 0;
}

ul.level-1 > li {
  padding: 5px 15px;
}

ul.level-2 > li {
  position: relative;
}

ul li a {
  color: red;
}
ul li span {
  color: black;
}
</style>