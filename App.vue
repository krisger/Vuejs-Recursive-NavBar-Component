<template>
  <div id="app">
    <NavBar :list="navigationItems"></NavBar>
  </div>
</template>

<script>
import NavBar from "./components/navigation.vue";

export default {
  name: "App",
  components: {
    NavBar
  },
  data: function() {
    return {
      navigationItems: [
        {
          name: "one",
          id: 1,
          level: 0,
          href: "/one",
          childItems: [
            {
              name: "onefirstchild",
              id: 10,
              href: "/onefirstchild",
              level: 1,
              childItems: [{ name: "onefirstsubchild", level: 2 }]
            },
            {
              name: "onesecondchild",
              id: 11,
              href: "/onesecondchild",
              level: 1
            }
          ]
        },
        {
          name: "two",
          level: 0,
          id: 2,
          href: "/two"
        }
      ]
    };
  }
};
</script>