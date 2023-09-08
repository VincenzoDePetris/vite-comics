<script>
export default {
  data() {
    return {
      counter: 1,
      links: [
        {
          name: "CHARACTERS",
          status: false,
        },
        {
          name: "COMICS",
          status: true,
        },
        {
          name: "MOVIES",
          status: false,
        },
        {
          name: "TV",
          status: false,
        },
        {
          name: "GAMES",
          status: false,
        },
        {
          name: "COLLECTIBLES",
          status: false,
        },
        {
          name: "VIDEOS",
          status: false,
        },
        {
          name: "FANS",
          status: false,
        },
        {
          name: "NEWS",
          status: false,
        },
        {
          name: "SHOP",
          status: false,
        },
      ],
    };
  },
  methods: {
    activeClass(index) {
      this.counter = index;
    },
  },
};
</script>

<template>
  <div class="dad">
    <div><img src="/public/img/dc-logo.png" alt="" /></div>
    <div>
      <ul>
        <li
          v-for="(link, index) in links"
          :class="index == counter ? 'active' : ''"
          @click="activeClass(index)"
        >
          <a href="#">
            {{ link.name }}
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.dad {
  height: 100px;
  img {
    width: 75px;
  }
}
div {
  display: flex;
  align-items: center;
  justify-content: space-around;
}
ul {
  display: flex;
  &:hover {
    cursor: pointer;
  }
  li {
    height: 100px;
    display: flex;
    align-items: center;
    justify-content: center;
    list-style: none;
    margin: 0 10px;
    a {
      text-decoration: none;
      color: black;
    }
  }
}
.active {
  border-bottom: solid 5px rgb(12, 124, 236);
  a {
    color: rgb(12, 124, 236);
  }
}
</style>
