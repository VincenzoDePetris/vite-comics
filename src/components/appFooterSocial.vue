<script>
export default {
  data() {
    return {
      social: [
        "/public/img/footer-facebook.png",
        "/public/img/footer-periscope.png",
        "/public/img/footer-pinterest.png",
        "/public/img/footer-twitter.png",
        "/public/img/footer-youtube.png",
      ],
    };
  },
};
</script>

<template>
  <div class="main">
    <div class="dad">
      <div>
        <Button>SIGN-UP NOW!</Button>
      </div>
      <div>
        <div class="follow">
          <a href="#">FOLLOW US</a>
        </div>
        <div v-for="image in social">
          <a href="#">
            <img :src="image" alt="" />
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.main {
  background-color: rgb(57, 57, 57);
  height: 100px;
}

.dad {
  width: 1400px;
  margin: auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  div {
    display: flex;
    align-items: center;
    margin: 10px;
  }
  .follow {
    a {
      text-decoration: none;
      color: rgb(12, 124, 236);
      font-size: 1.2rem;
    }
  }
  button {
    background-color: rgba(0, 0, 0, 0);
    color: whitesmoke;
    border: solid rgb(12, 124, 236) 2px;
    padding: 10px 20px;
    font-size: 1.2rem;
    &:hover {
      cursor: pointer;
    }
  }
}
</style>
