<script>
export default {
  data() {
    return {
      commerce: [
        {
          text: "DIGITAL COMICS",
          img: "/public/img/buy-comics-digital-comics.png",
        },
        {
          text: "DC MERCHANDISE",
          img: "/public/img/buy-comics-merchandise.png",
        },
        {
          text: "SUBSCRIPTION",
          img: "/public/img/buy-comics-shop-locator.png",
        },
        {
          text: "COMIC SHOP LOCATOR",
          img: "/public/img/buy-comics-subscriptions.png",
        },
        {
          text: "DC POWER VISA",
          img: "/public/img/buy-dc-power-visa.svg",
        },
      ],
    };
  },
  methods: {},
};
</script>

<template>
  <div class="dad">
    <div class="dc-merch">
      <div v-for="links in commerce" class="mini-merch">
        <div class="img-mini">
          <a href="#">
            <img :src="links.img" alt="" />
          </a>
        </div>
        <div>
          <a href="#">
            {{ links.text }}
          </a>
        </div>
      </div>
    </div>
    <div class="references"></div>
    <div class="social"></div>
  </div>
</template>

<style lang="scss" scoped>
.dad {
  div {
    width: 1400px;
    margin: auto;
  }
  background-color: rgb(12, 124, 236);
}
.dc-merch {
  &:hover {
    cursor: pointer;
  }
  display: flex;

  color: whitesmoke;
  a {
    text-decoration: none;
    color: whitesmoke;
  }
}

.mini-merch {
  display: flex;
  justify-content: center;
  align-items: center;

  div {
    width: 50%;
  }
  .img-mini {
    width: 50%;
    margin: 20px;
  }
}
</style>
