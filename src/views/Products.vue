<template>
  <div>
    <div class="container pb-5">
      <router-link
        :to="{ name: 'Home' }"
        class="mb-4 back btn btn-warning shadow border-radius-14px fw-bold px-3"
      >
        &lt; Назад кон менито
      </router-link>
      <div>
        <div
          class="card mb-4 p-4 shadow"
          v-for="(product, i) in products[this.$route.params.id]"
          :key="i"
        >
          <div
            class="d-flex flex-row align-items-center justify-content-between"
          >
            <div class="d-flex flex-column">
              <div class="fw-bold">
                {{ product.name }}
              </div>
              <div class="fst-italic ingredients">
                {{ product.ingredients }}
              </div>
            </div>
            <div class="fw-bold fst-italic text-nowrap">
              {{ product.price }} ден.
            </div>
          </div>
        </div>
      </div>
      <router-link
        :to="{ name: 'Home' }"
        class="back mb-2 btn btn-warning shadow border-radius-14px fw-bold px-3"
      >
        &lt; Назад кон менито
      </router-link>
    </div>
  </div>
</template>

<script>
export default {
  name: "Products",
  data() {
    return {
      products: [
        // НЕГАЗИРАНИ ПИЈАЛОЦИ/SOFT DRINKS
        [
          {
            name: "Вода (голема)/Water 0.75",
            price: "120",
            ingredients: "Безалкохолни пијалоци",
          },
          {
            name: "Вода (мала)/Water 0.25",
            price: "80",
            ingredients: "Безалкохолни пијалоци",
          },
          {
            name: "Пепси",
            price: "120",
            ingredients: "Безалкохолни пијалоци",
          },
          {
            name: "Пепси Макс",
            price: "120",
            ingredients: "Безалкохолни пијалоци",
          },
          {
            name: "Газоза/Gazoza",
            price: "100",
            ingredients: "Безалкохолни пијалоци",
          },
          {
            name: "Леден Чај/Ice Tea",
            price: "120",
            ingredients: "Безалкохолни пијалоци",
          },
          {
            name: "7уп",
            price: "120",
            ingredients: "Безалкохолни пијалоци",
          },
          {
            name: "Негазирани сокови/Juice",
            price: "140",
            ingredients: "Безалкохолни пијалоци",
          },
          {
            name: "Цеден Лимон/Fresh Lemon Juice",
            price: "90",
            ingredients: "Безалкохолни пијалоци",
          },
          {
            name: "Цеден портокал/Fresh Orange Juice",
            price: "180",
            ingredients: "Безалкохолни пијалоци",
          },
          {
            name: "Mirinda/Mirinda",
            price: "120",
            ingredients: "Безалкохолни пијалоци",
          },
          {
            name: "Домашна лимонада со вкус/Homemade lemonade",
            price: "160",
            ingredients: "Безалкохолни пијалоци",
          },
          {
            name: "Овошна сода",
            price: "140",
            ingredients: "Безалкохолни пијалоци"
          }
        ],
        // ПИВО
        [
          {
            name: "Крали Марко 0.5",
            price: "140",
            ingredients: "Пиво",
          },
          {
            name: "Златен Даб 0.33",
            price: "130",
            ingredients: "Пиво",
          },
          {
            name: "Златен Даб Драфт 0.33",
            price: "140",
            ingredients: "Пиво",
          },
          {
            name: "Златен Даб Драфт 0.5",
            price: "170",
            ingredients: "Пиво",
          },
          {
            name: "Fox Pale ale draft 0.5",
            price: "240",
            ingredients: "Пиво",
          },
          {
            name: "Veda White ipa draft 0.5",
            price: "260",
            ingredients: "Пиво",
          },
          {
            name: "Corona",
            price: "250",
            ingredients: "Пиво",
          },
          {
            name: "Kalesh-Black ipa 0.33",
            price: "250",
           ingredients: "Пиво",
        
          },
          {
            name: "Tuborg 0.33",
            price: "170",
            ingredients: "Пиво",

          },
          {
            name: "Tuborg Draft 0.4",
            price: "220",
            ingredients: "Пиво",
          },
          {
            name: "Carlsberg 0.33",
            price: "190",
            ingredients: "Пиво",
          },
          {
            name: "Holsten 0.5",
            price: "260",
            ingredients: "Пиво",

          },
          {
            name: "Kozel 0.5",
            price: "220",
            ingredients: "Пиво",
          },
          {
            name: "Franziskaner 0.5",
            price: "280",
            ingredients: "Пиво",
          },
        ],
        // ВИНАРИЈА
        [
          {
            name: "Synthesis cuvee barrique(dry)",
            price: "1900",
            ingredients: "Винарија",
          },
          {
            name: "Dionis vranec barrique(dry)",
            price: "2200",
            ingredients: "Винарија",
          },
          {
            name: "Hermes vranec(dry)",
            price: "1300",
            ingredients: "Винарија",
          },
          {
            name: "Hermes cabernet sauvignon(dry)",
            price: "1300",
            ingredients: "Винарија",
          },
          {
            name: "Amfora vranec(semi-dry)",
            price: "900",
            ingredients: "Винарија",
          },
          {
            name: "Chardonnay barrique fermented(dry)",
            price: "2400",
            ingredients: "Винарија",
          },
          {
            name: "Muscat temjanika(semi-dry)",
            price: "1350",
            ingredients: "Винарија",
          },
          {
            name: "Elegija chardonnay(dry)",
            price: "1300",
            ingredients: "Винарија",
          },
          {
            name: "Elegija traminer(dry)",
            price: "1300",
            ingredients: "Винарија",
          },
          {
            name: "Elegija zupljanka(dry)",
            price: "1300",
            ingredients: "Винарија",
          },
          {
            name: "Amphora cuvee(semi-dry)",
            price: "900",
            ingredients: "Винарија",
          },
          {
            name: "Temjanika(dry)",
            price: "1400",
            ingredients: "Винарија",
          },
          {
            name: "Chardonnay(dry)",
            price: "1400",
            ingredients: "Винарија",
          },
          {
            name: "Sauvignon blanc(dry)",
            price: "1400",
            ingredients: "Винарија",
          },
          {
            name: "Amfora Rose(dry)",
            price: "900",
            ingredients: "Винарија",
          },
          {
            name: "Elegija syrah(dry)",
            price: "1200",
            ingredients: "Винарија",
          },
          {
            name: "Muscat rolinger(dry)",
            price: "1250",
            ingredients: "Винарија",
          },
          {
            name: "Muscat rolinger red(semi-dry)",
            price: "1250",
            ingredients: "Винарија",
          },
        ],
        // КАФЕ И ЧАЈ/COFFEE AND TEA
        [
          {
            name: "Чај/Tea",
            price: "80",
            ingredients: "Топли напитоци",
          },
          {
            name: "Еспресо/Espresso",
            price: "90",
            ingredients: "Топли напитоци",
          },
          {
            name: "Макијато/Macchiato",
            price: "100",
            ingredients: "Топли напитоци",
          },
          {
            name: "Големо Макијато",
            price: "110",
            ingredients: "Топли напитоци",
          },
          {
            name: "Latte macchiato",
            price: "160",
            ingredients: "Топли напитоци",
          },
          {
            name: "Нес кафе",
            price: "140",
            ingredients: "Топли напитоци",
          },
          {
            name: "Капучино",
            price: "120",
            ingredients: "Топли напитоци",
          
          },
          {
            name: "Ладно макијато",
            price: "110",
            ingredients: "Топли напитоци",

          },
          {
            name: "Ирско кафе",
            price: "260",
            ingredients: "Топли напитоци",
          },
          {
            name: "Американо",
            price: "120",
            ingredients: "Топли напитоци",
          },
          {
            name: "Македонско кафе",
            price: "90",
            ingredients: "Топли напитоци",
          },
        ],
        // АЛКОХОЛНИ ПИЈАЛОЦИ
        [
          {
            name: "Лозова Жолта",
            price: "120",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Лозова бела",
            price: "120",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Мастика",
            price: "120",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Ракија Азбука",
            price: "130",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Гордион амбер ракија",
            price: "160",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Бадел Вилијамс ракија",
            price: "170",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Џин бадел",
            price: "120",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Смидџин",
            price: "250",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Џин беефеатер",
            price: "170",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Џин Гордонс",
            price: "190",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Џин пинк Гордонс",
            price: "180",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Џин Бомбај",
            price: "240",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Водка бадел",
            price: "120",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Бејлис",
            price: "180",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Фенејс",
            price: "150",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Крушковац пеар ликер",
            price: "140",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Текила",
            price: "130",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Амарето",
            price: "150",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Корлат Шливовица",
            price: "220",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Корлат мараска",
            price: "220",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Шот",
            price: "100",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Смирноф",
            price: "160",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Џек Даниелс",
            price: "280",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Џемјсон",
            price: "180",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Џејмсон Блек",
            price: "290",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Џони Ред",
            price: "160",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Џони Блек",
            price: "260",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "4 Рози",
            price: "200",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Вилијам Пеел",
            price: "150",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Рум Морган",
            price: "160",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Јегермајстер",
            price: "210",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Пелинковац бадел",
            price: "120",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Пелинковац антик",
            price: "170",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Коњак бадел",
            price: "120",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Коњак бадел блек",
            price: "160",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Рум бадел",
            price: "120",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Шток 84",
            price: "150",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Текила олмека",
            price: "170",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Аперол",
            price: "160",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Корлат лоза",
            price: "220",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Кампари",
            price: "160",
            ingredients: "Алкохолни пијалоци",
          },
        ],
        // САЛАТИ
        [
          {
            name: "Шопска Салата",
            price: "220",
            ingredients: "Домати, краставица , кромид , сирење",
          },
          {
            name: "Егејска салата",
            price: "220",
            ingredients: "Домати, краставица, кромид кругови, сирење на коцки, оригано",
          },
          {
            name: "Ракија салата",
            price: "170",
            ingredients: "Зелка, краставица, маслинки",
          },
          {
            name: "Македонска салата",
            price: "200",
            ingredients: "Домати, кромид, печени пиперки",
          },
          {
            name: "Мешана салата",
            price: "190",
            ingredients: "Цвекло, морков, краставица, домат, зелка",
          },
          
      
          {
            name: "Цезар салата",
            price: "250",
            ingredients: 
            "Марула, пилешко, кубети, домати, пармезан, прелив",
          },
          {
            name: "Туна салата",
            price: "260",
            ingredients: "Марула, туна, пченка, кромид, маслинки",
          },
          
          {
            name: "Салата од морски плодови",
            price: "360",
            ingredients:
              "Марула, морски плодови, авокадо, краставица, домати, прелив со сенф и лимон",
          },
        
        ],

        // ДАСКИ
        [
          {
            name: "МЕШАНА ДАСКА (4 ЛИЦА)",
            price: "1350",
            ingredients: "5 ќебапи, плескавица 100г, пилешки стек 100г, сланина 100г, колбас, пилешки увијач, пилешки прсти 150г, поховани зденки, сирење на скара 150г, помфрит, сос",
          },
          {
            name: "ВИНСКА ДАСКА",
            price: "1650",
            ingredients: "Горгонзола, чаден кашкавал, домашно кравјо сирење, овчо сирење, кашкавал, биено сирење, сланина, мортадела, пршута",
          },
          {
            name: "МАКЕДОНСКА МЕЗЕ ДАСКА",
            price: "890",
            ingredients: "Ајвар, лутеница, макало, тиквици на скара, домашно сирење 200г, леб на скара",
          },
          
        ],

        // ПРИЛОЗИ И ДОРУЧЕК
        [
          {
            name: "Авокадо Тортиља",
            price: "250",
            ingredients: "2 јајца, тортиља, намаз од авокадо, домат, павлака",
          },
          {
            name: "Охридска кајгана",
            price: "240",
            ingredients: "3 јајца, домати, печени пиперки, сирење",
          },
          {
            name: "Јајца на око со сланина",
            price: "230",
            ingredients: "3 јајца, 100г сланина, леб",
          },
          {
            name: "Утринска кеседиља",
            price: "260",
            ingredients: "Тортиља, кашвакал, чедар, 1 јаце на око, сланина, домат",
          },
          {
            name: "Доручек Лихнидија",
            price: "360",
            ingredients: "Пржени лепчиња со јајце, кашкавал, сланина, колбас, домашно кравјо сирење, ајвар",
          },
          {
            name: "Омлет",
            price: "250",
            ingredients: "Ваша комбинација по избор",
          },
          {
            name: "Јајца на око со шунка",
            price: "220",
            ingredients: "3 јајца, 100г шунка, леб",
          },
          {
            name: "Чоко тост",
            price: "190",
            ingredients: "Путер од кикиритки, нутела, мед, сезонско овошје",
          },
          {
            name: "Рибна чорба",
            price: "240",
            ingredients: "Прилози и доручек",
          },
          {
            name: "Телешка чорба",
            price: "230",
            ingredients: "Прилози и доручек",
          },
          
        ],

        // Јадења од мелено месо
        [
          {
            name: "Плескавица 250г.",
            price: "280",
            ingredients: "Јадења од мелено месо",
          },
          {
            name: "Шарска плескавица 350г.",
            price: "320",
            ingredients: "Мелено месо 250г, кашкавал 100г",
          },
          {
            name: "Ќебапи со кајмак",
            price: "360",
            ingredients: "Јадења од мелено месо",
          },
          {
            name: "Ќофте во доматен сос",
            price: "340",
            ingredients: "Мелено месо 250г, пелати сос, пармнезан, босилек",
          },
          {
            name: "Плескавица 1кг со сос од кашкавал",
            price: "950",
            ingredients: "Јадења од мелено месо",
          },
          {
            name: "Полнета плескавица",
            price: "380",
            ingredients: "Мелено месо 300г, кашкавал, зденка, печурки, шунка",
          },
          {
            name: "Ќебапи",
            price: "320",
            ingredients: "Јадења од мелено месо",
          },
          {
            name: "Лихнидија плескавица 500г",
            price: "390",
            ingredients: "Мелено месо 300г, сланина 100г, кајмак, јајце",
          },
          
        ],
        //ЈАДЕЊА ОД ТЕЛЕШКО МЕСО
        [
          {
            name: "Бифтек на путер и рузмарин 250г",
            price: "1150",
            ingredients: "Јадења од телешко месо",
          },
          {
            name: "Бифтек со јајце 250г",
            price: "1220",
            ingredients: "Јадења од телешко месо",
          },
          {
            name: "Телешка тава 250г",
            price: "850",
            ingredients: "Телешко месо 200г, кромид, домат, пиперка",
          },
          {
            name: "Бифтек во сос од бибер во зрна 250г",
            price: "1250",
            ingredients: "Јадења од телешко месо",
          },
        ],
        //ЈАДЕЊА ОД СВИНСКО МЕСО
        [
          {
            name: "Свинско филе со кашкавал и печурки 200г",
            price: "390",
            ingredients: "Јадења од свинско месо",
          },
          {
            name: "Каре во скара сос и сусам 200г",
            price: "350",
            ingredients: "Јадења од свинско месо",

          },
          {
            name: "Вешалица 200г",
            price: "370",
            ingredients: "Јадења од свинско месо",
          },
          {
            name: "Домашен колбас 250г",
            price: "330",
            ingredients: "Јадења од свинско месо",

          },
          {
            name: "Ребро 300г",
            price: "380",
            ingredients: "Јадења од свинско месо",

          },
          {
            name: "Коленица 1кг",
            price: "990",
            ingredients: "Јадења од свинско месо",
          },
          {
            name: "Сланина 200г",
            price: "340",
            ingredients: "Јадења од свинско месо",

          },
        ],
        //ЈАДЕЊА ОД ПИЛЕШКО МЕСО
        [
        {
            name: "Пилешко Лихнидија",
            price: "360",
            ingredients: "Пилешко филе 200г, сланина, маслиново масло, пармезан, путер, сушен домат, оригано, мајчина душица, гарнир",
          },
          {
            name: "Пилешки стек на скара 200г",
            price: "260",
            ingredients: "Јадења од пилешко месо",

          },
          {
            name: "Крцкав пилешки стек 250г",
            price: "280",
            ingredients: "Јадења од пилешко месо",
          },
          {
            name: "Пилешки стек на азсики начин 250г",
            price: "290",
            ingredients: "Тиквици, печурки, кромид, бело вино, кари",

          },
          {
            name: "Пилешки копанчиња во скара сос 500г",
            price: "280",
            ingredients: "Јадења од пилешко месо",

          },
          {
            name: "Пилешки прсти 300г",
            price: "320",
            ingredients: "Јадења од пилешко месо",
          },
          
        ],
        //ЈАДЕЊА ВО ТАВА
        [
        {
            name: "Селско месо",
            price: "440",
            ingredients: "Свинско месо, пилешко месо, кашкавал, печурки, кромид, лук, пиперка, домат",
          },
          {
            name: "Тава Лихнидија",
            price: "480",
            ingredients: "Свинско месо, пилешко месо, сланина, домат, пиперка, кромид, лук, буковка, печурки, чаден кашкавал",

          },
          {
            name: "Тавче гравче",
            price: "250",
            ingredients: "Јадења во тава",
          },
          {
            name: "Тавче гравче со плескавица/колбас",
            price: "320",
            ingredients: "Јадења во тава",

          },
          {
            name: "Печурки со сланина и кашкавал",
            price: "370",
            ingredients: "Јадења во тава",

          },
         
        ],
        //БУРГЕРИ
        [
        {
            name: "Хамбургер",
            price: "240",
            ingredients: "150г мелено месо, марула, зелка, краставица, кромид, помфрит",
          },
          {
            name: "Чикенбургер",
            price: "260",
            ingredients: "150г пилешко месо, марула, зелка, краставица, помфрит",

          },
          {
            name: "Чаден бургер",
            price: "320",
            ingredients: "150г мелено месо, чаден кашкавал, сланина, марула, зелка, краставица, кромид, бургер сос",
          },
          {
            name: "Блу Чикенбургер",
            price: "310",
            ingredients: "150г пилешко месо, горгонзола сос, марула, зелка, краставица, помфрит, сос",

          },
          
        ],
        //Рижото и паста
        [
        {
            name: "Рижото со врган",
            price: "420",
            ingredients: "Ориз, врган, лук и кромид, бело вино, млеко, путер, пармезан",
          },
          {
            name: "Шпагети карбонара",
            price: "380",
            ingredients: "Шпагети, сланина, пармезан, жолчка од јајце, бибер",

          },
          {
            name: "Рижото со горгонзола",
            price: "390",
            ingredients: "Ориз, путер, маслиново масло, бело вино, горгонзола",
          },
          {
            name: "Рижото со морски плодови",
            price: "490",
            ingredients: "Ориз, школки, ракчиња, лук и кромид, маслиново масло, бело вино, копар",

          }, 
          {
            name: "Тортелини со горгонзола и фстаци",
            price: "370",
            ingredients: "Ориз, пустер, маслиново масло, бело вино, горгонзола",
          },
          {
            name: "Шпагети со морски плодови",
            price: "460",
            ingredients: "Школки, ракчиња, кромид, лук, маслиново масло, магданос, копер, бело вино, домат",

          }, 
        ],

        // ПРЕДЈАДЕЊА
        [
          {
            name: "Брускети со домат,моцарела и песто",
            price: "220",
            ingredients:
              "Предјадења",
          },
          {
            name: "Сирење на скара 200г",
            price: "240",
            ingredients: "Предјадења",
          },
          {
            name: "Печурки на путер 250г",
            price: "240",
            ingredients: "Предјадења",
          },
          {
            name: "Чипс од сланина 200г",
            price: "290",
            ingredients: "Предјадења",
          },
          {
            name: "Полнета пиперка со кајмак",
            price: "170",
            ingredients: "Пиперка, кајмак, јајце, кашкавал",
          },
          {
            name: "Лепчиња со лук",
            price: "170",
            ingredients: "Предјадења",
          },
          {
            name: "Лепиња со кајмак",
            price: "140",
            ingredients:
              "Предјадења",
          },
          {
            name: "Тиквици на скара 200г",
            price: "180",
            ingredients:
              "Предјадења",
          },
          {
            name: "Макало од лук",
            price: "140",
            ingredients: "Предјадења",
          },
          {
            name: "Ајвар",
            price: "140",
            ingredients: "Предјадења",
          },
          {
            name: "Биено сирење со сланина 150г",
            price: "280",
            ingredients: "Предјадења",
          },
          {
            name: "Домашно кравјо сирење 200г",
            price: "250",
            ingredients: "Предјадења",
          },
          {
            name: "Полнети печурки",
            price: "260",
            ingredients: "Печурки, кашкавал, свински врат",
          },
          {
            name: "Топено сирење 300г",
            price: "270",
            ingredients:
              "Фета сирење, доматен сос, павлака, сланина, кашкавал",
          },
          {
            name: "Похован кашкавал 100г",
            price: "170",
            ingredients:
              "Предјадења",
          },
          {
            name: "Поховани зденки 150г",
            price: "180",
            ingredients: "Предјадења",
          },
          {
            name: "Похован кромид 200г",
            price: "240",
            ingredients: "Предјадења",
          },
          {
            name: "Лутеница",
            price: "140",
            ingredients: "Предјадења",
          },
        ],
        // РИБА
        [
          {
            name: "Пастрмка 1кг.",
            price: "1200",
            ingredients: "Риба",
          },
          {
            name: "Пастрмка на охридски начин 1кг.",
            price: "1600",
            ingredients: "Риба",
          },
          {
            name: "Лосос во сос од бело вино 1кг.",
            price: "1350",
            ingredients: "Риба",
          },
          {
            name: "Кременадли од крап 1кг.",
            price: "1400",
            ingredients: "Риба",
          },
          {
            name: "Печен крап со зеленчук 1кг. по нарачка",
            price: "1550",
            ingredients: "Риба",
          },
          {
            name: "Белвица 1кг.",
            price: "2400",
            ingredients: "Риба",
          },
        ],
        // ДЕСЕРТИ
        [
          {
            name: "Палачинка со нутела,плазма и банана",
            price: "180",
            ingredients: "Десерти",
          },
          {
            name: "Чоколаден мус",
            price: "160",
            ingredients: "Десерти",
          },
          {
            name: "Овошна салата со сезонско овошје",
            price: "220",
            ingredients: "Десерти",
          },
          {
            name: "Баклава",
            price: "170",
            ingredients: "Десерти",
          },
          
        ],
        //ДОДАТОЦИ
        [
          {
            name: "Пиперка парче",
            price: "50",
            ingredients: "Додатоци",
          },
          {
            name: "Лута пиперка парче",
            price: "50",
            ingredients: "Додатоци",
          },
          {
            name: "Нафора со сирење",
            price: "150",
            ingredients: "Додатоци",
          },
          {
            name: "Маслинки 100г",
            price: "80",
            ingredients: "Додатоци",
          },
          {
            name: "Лепиња",
            price: "50",
            ingredients: "Додатоци",
          },
          {
            name: "Јајце",
            price: "30",
            ingredients: "Додатоци",
          },
          {
            name: "Помфрит 100г",
            price: "70",
            ingredients: "Додатоци",

          
          },
          {
            name: "Сос",
            price: "40",
            ingredients: "Додатоци",
          },
        ],
        //КОКТЕЛИ
        [
        {
            name: "Margarita",
            price: "300",
            ingredients: "Текила, трипл сек, сок од лимон",
          },
          {
            name: "Tequila sunrise",
            price: "270",
            ingredients: "Текила, гранадин, сок од портокал",
          },
          {
            name: "Cuba libre",
            price: "290",
            ingredients: "Рум, кока кола, свежа лимета",
          },
          {
            name: "Mojito",
            price: "320",
            ingredients: "Бел рум, кафеав шеќер, нане, лед, сода",
          },
          {
            name: "Sex on the beach",
            price: "300",
            ingredients: "Вотка, арчерс, сок од брусница, портокал",
          },
          {
            name: "Mai Tai",
            price: "350",
            ingredients: "Бел рум, црн рум, сок од лимета, портокал",
          },
          {
            name: "Cosmopolitan",
            price: "320",
            ingredients: "Вотка, трипл сек, сок од лимета, брусница",
          },
          {
            name: "Hurricane",
            price: "390",
            ingredients: "Бел и темен рум, сок од маракуја и лимета, гренадин, шеќерен сируп ",
          },
          {
            name: "Long Island Iced Tea",
            price: "380",
            ingredients: "Бел рум, вотка, џин, текила, сок од лимон, кока кола, шеќерен сируп",
          },
          {
            name: "AMF",
            price: "370",
            ingredients: "Вотка, бел рум, текила, џин, син курасао, лимон, шеќерен сируп",
          },
          {
            name: "Pinacolada",
            price: "350",
            ingredients: "Бел рум, кокосов крем и рум, сок од ананас",
          },
          {
            name: "Gin Fizz",
            price: "260",
            ingredients: "Џин, сок од лимон, шеќерен сируп, сода",
          },
          {
            name: "Blue Lagoon",
            price: "320",
            ingredients: "Вотка, син курасао, 7уп",
          },
          {
            name: "Bahama Mama",
            price: "350",
            ingredients: "Бел рум, малибу, вишнова ракија, сок од портокал и лимон, шеќерен сируп",
          },
          {
            name: "Aperol Spritz",
            price: "300",
            ingredients: "Аперол, просеко, сода",
          },
          {
            name: "Blue Hawaii",
            price: "340",
            ingredients: "Бел рум, вотка, син курасао, сок од ананас и лимон, шеќерен сируп",
          },
          {
            name: "Bloody Mary",
            price: "390",
            ingredients: "Вотка, сок од домат и лимон, табаско, ворчестер сос, сол, црн пипер",
          },
        ],
      ],
    };
  },
};
</script>

<style scoped></style>
