<script>
export default {
  data() {
    return {
      dcComics: [
        {
          title: "DC COMICS",
          links: [
            "charachters",
            "Comics",
            "Movies",
            "TV",
            "Games",
            "Videos",
            "News",
          ],
        },
        {
          title: "SHOP",
          links: ["Shop DC", "Shop DC Collectibles"],
        },
        {
          title: "DC",
          links: [
            "Terms Of Use",
            "Privacy policy (New)",
            "Ad Choices",
            "Advertising",
            "jobs",
            "subscriptions",
            "Talent Workshops",
            "CPSC Certificates",
            "Ratings",
            "Shop Help",
            "Contact Us",
          ],
        },
        {
          title: "SITES",
          links: [
            "DC",
            "MAD Magazine",
            "DC Kids",
            "DC Universe",
            "DC Power Visa",
          ],
        },
      ],
    };
  },
};
</script>

<template>
  <div class="bg-ph">
    <div class="dad">
      <div v-for="title in dcComics">
        <h3>{{ title.title }}</h3>
        <ul>
          <li v-for="link in title.links">
            <a href="#">{{ link }}</a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.bg-ph {
  height: 400px;
  background-image: url("/img/footer-bg.jpg");
}

.dad {
  width: 1400px;
  height: 400px;
  margin: auto;
  color: whitesmoke;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-content: flex-start;
  flex-wrap: wrap;
  div {
    margin: 20px;
  }
  ul {
    padding: 0;
  }
  li {
    list-style: none;
    a {
      text-decoration: none;
      color: rgb(159, 159, 159);
      &:hover {
        color: whitesmoke;
      }
    }
  }
}
</style>
