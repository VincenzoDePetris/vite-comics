<script>
export default {
  data() {
    return {};
  },
  methods: {},

  props: {
    cards: Array,
  },
};
</script>

<template>
  <div class="image-xl">
    <div>
      <span>CURRENT SERIES</span>
    </div>
  </div>
  <div class="dad">
    <div class="uncle">
      <div class="card" v-for="(card, index) in cards">
        <img :src="card.thumb" alt="" />
        <p>
          <a href="#">
            {{ card.series }}
          </a>
        </p>
      </div>
      <button>LOAD MORE</button>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.image-xl {
  height: 400px;
  background-image: url("/img/jumbotron.jpg");

  position: relative;
  div {
    width: 1400px;
    margin: auto;
    position: absolute;
    bottom: -5px;
    left: 15%;
    span {
      background-color: rgb(12, 124, 236);
      padding: 10px 15px;
      color: whitesmoke;
      font-size: 1.3rem;
    }
  }
}
.dad {
  background-color: rgb(36, 36, 36);
  color: whitesmoke;
  padding: 25px 0;
  .uncle {
    display: flex;
    align-items: flex-start;
    flex-wrap: wrap;
    justify-content: center;
    width: 1400px;
    margin: auto;
    .card {
      margin: 10px;
      width: 200px;
      height: 200px;
      a {
        text-decoration: none;
        color: whitesmoke;
      }
      img {
        width: 150px;
        height: 150px;
        max-width: 100%;
      }
    }
  }
}
button {
  background-color: rgb(12, 124, 236);
  color: whitesmoke;
  border: solid rgb(12, 124, 236) 2px;
  padding: 10px 20px;
  font-size: 1.2rem;
  &:hover {
    cursor: pointer;
  }
}
</style>
