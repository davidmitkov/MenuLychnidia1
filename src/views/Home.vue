<template>
  <div>
    <div class="container pb-5">
      <div>
        <router-link
          :to="{ name: 'Products', params: { id: option.id } }"
          class="card mb-4 p-2 shadow"
          v-for="option in menu"
          :key="option.name"
        >
          <div class="row g-0">
            <div class="col-3 col-md-2 d-flex align-items-center">
              <div class="ratio ratio-1x1">
                <img
                  :src="option.img"
                  class="rounded-3 img-fluid"
                  style="width: 5rem; height: 5rem; object-fit: cover"
                  alt=""
                />
              </div>
            </div>
            <div class="col-8 d-flex align-items-center">
              <div class="card-body">
                <h5 class="card-title fw-bold">{{ option.name }}</h5>
              </div>
            </div>
          </div>
        </router-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Home",
  methods: {
    scrollToTop(option) {
      window.scrollTo(0, 0);
      if (option != null) this.selectedProducts = option.products;
      else this.selectedProducts = null;
    },
  },
  data() {
    return {
      selectedProducts: null,
      menu: [
        {
          img: require("../assets/images/juice.jpg"),
          name: "НЕГАЗИРАНИ ПИЈАЛОЦИ",
          id: 0,
        },
        {
          img: require("../assets/images/beer.jpeg"),
          name: "ПИВО",
          id: 1,
        },
        {
          img: require("../assets/images/wine.jpeg"),
          name: "ВИНАРИЈА",
          id: 2,
        },
        {
          img: require("../assets/images/coffee.jpg"),
          name: "КАФЕ И ЧАЈ",
          id: 3,
        },
        {
          img: require("../assets/images/alcochol.jpg"),
          name: "АЛКОХОЛНИ ПИЈАЛОЦИ",
          id: 4,
        },

        {
          img: require("../assets/images/salad.jpg"),
          name: "САЛАТИ",
          id: 5,
        },
        {
          img: require("../assets/images/foodboard.jpg"),
          name: "ДАСКИ",
          id: 6,
        },
        {
          img: require("../assets/images/breakfast.jpg"),
          name: "ПРИЛОЗИ И ДОРУЧЕК",
          id: 7,
        },
        {
          img: require("../assets/images/mincemeat.jpg"),
          name: "ЈАДЕЊА ОД МЕЛЕНО МЕСО",
          id: 8,
        },
        {
          img: require("../assets/images/vealmeat.jpg"),
          name: "ЈАДЕЊА ОД ТЕЛЕШКО МЕСО",
          Id: 9,
        },
        {
          img: require("../assets/images/porkmeat.jpg"),
          name: "ЈАДЕЊА ОД СВИНСКО МЕСО",
          Id: 10,
        },
        {
          img: require("../assets/images/chickenmeat.jpg"),
          name: "ЈАДЕЊА ОД ПИЛЕШКО МЕСО",
          Id: 11,
        },
        {
          img: require("../assets/images/tavafood.jpg"),
          name: "ЈАДЕЊА ВО ТАВА",
          Id: 12,
        },
        {
          img: require("../assets/images/burger.jpg"),
          name: "БУРГЕРИ",
          Id: 13,
        },
        {
          img: require("../assets/images/pasta.jpg"),
          name: "РИЖОТО И ПАСТА",
          Id: 14,
        },
        {
          img: require("../assets/images/speciality.jpg"),
          name: "ПРЕДЈАДЕЊА",
          id: 15,
        },
        {
          img: require("../assets/images/fish.jpg"),
          name: "РИБА",
          id: 16,
        },
        {
          img: require("../assets/images/dessert.jpg"),
          name: "ДЕСЕРТИ",
          id: 17,
        },
        {
          img: require("../assets/images/peppers.jpg"),
          name: "ДОДАТОЦИ",
          id: 18,
        },
        {
          img: require("../assets/images/cocktails.jpg"),
          name: "КОКТЕЛИ",
          id: 19,
        },
      ],
    };
  },
};
</script>

<style scoped>
.back {
  font-size: 1.2rem;
}
</style>
