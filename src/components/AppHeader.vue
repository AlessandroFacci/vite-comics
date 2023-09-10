<script>
export default {
  data() {
    return {
      links: [
        {
          text: "CHARACTERS",
          url: "#",
          current: false,
        },
        {
          text: "COMICS",
          url: "#",
          current: true,
        },
        {
          text: "MOVIES",
          url: "#",
          current: false,
        },
        {
          text: "TV",
          url: "#",
          current: false,
        },
        {
          text: "GAMES",
          url: "#",
          current: false,
        },
        {
          text: "COLLECTIBLES",
          url: "#",
          current: false,
        },
        {
          text: "VIDEOS",
          url: "#",
          current: false,
        },
        {
          text: "FANS",
          url: "#",
          current: false,
        },
        {
          text: "NEWS",
          url: "#",
          current: false,
        },
        {
          text: "SHOP",
          url: "#",
          current: false,
        },
      ],
    };
  },
};
</script>

<template>
  <header>
    <div>
      <img src="../../public/img/dc-logo.png" alt="dc-logo" />
    </div>
    <div>
      <ul>
        <li v-for="link in links">
          <a :href="link.url" :class="link.current ? 'current' : ''">
            {{ link.text }}</a
          >
        </li>
      </ul>
    </div>
  </header>
</template>

<style lang="scss" scoped>
header {
  padding: 1rem 0;
  display: flex;
  justify-content: space-around;
  ul {
    list-style-type: none;
    padding: 0;
    display: flex;
    li {
      padding: 0 1rem;
      a {
        text-decoration: none;
        color: black;
      }
    }
  }
}

li .current {
  border-bottom: 4px solid blue;
}
</style>
