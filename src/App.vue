<script setup>
import { ref } from 'vue';
const paragraphContainer = ref(null);
const paragraphFirst = ref(null);
const paragraphSecond = ref(null);
const paragraphThird = ref(null);
const paragraphFourth = ref(null);
const paragraphFifth = ref(null);
const activeIndex = ref(0);
const titleList = ['Title1', 'Title2', 'Title3', 'Title4', 'Title5']
const divList = [paragraphFirst, paragraphSecond, paragraphThird, paragraphFourth, paragraphFifth]
const handleScroll = (el) => {
  const { target: parentNode } = el;

  divList.forEach((vueRef, index) => {
    const { value: el } = vueRef;
    const rect = el.getBoundingClientRect()
    if (rect.top < parentNode.clientHeight && rect.bottom >= 0) {
      activeIndex.value = index;
    }
  })
}
const handleNavClick = (index) => {
  const el = divList[index].value;
  const rect = el.getBoundingClientRect();
  const parentNode = paragraphContainer.value;
  parentNode.scrollTop += rect.top - 24;
}
</script>

<template>
  <main>
    <section ref="paragraphContainer" @scroll="handleScroll">
      <div ref="paragraphFirst">
        <h3>Title1</h3>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eligendi similique pariatur quam culpa nulla nobis
          facere! Voluptate atque ullam libero accusamus nemo eaque hic aliquam illo ipsam maxime nobis sunt maiores
          excepturi
          sapiente praesentium labore quisquam, eveniet impedit eos exercitationem facilis, suscipit fuga! Deleniti
          accusamus
          animi unde placeat autem voluptas commodi, quos impedit eligendi mollitia ab! Molestiae aut, recusandae
          veritatis
          expedita dolor facere totam autem, magni sequi doloremque sunt exercitationem laborum nihil! Animi debitis
          assumenda
          saepe, dolore a numquam hic sequi laboriosam obcaecati doloremque, mollitia iure, amet ipsam sunt eveniet
          nesciunt!
          At accusantium libero sunt hic neque earum nostrum molestiae maiores, quo nobis nulla officiis possimus? Beatae,
          voluptatum. Natus corrupti odio nam quasi hic quisquam molestiae sit non ullam quibusdam eos minima aut eius, in
          maxime recusandae sint doloremque quae numquam inventore velit, vitae culpa praesentium. Rerum accusamus,
          corporis
          eius iure sint ipsum hic quae aut itaque expedita ex eum maiores id sit obcaecati nemo alias ducimus asperiores
          delectus dolores! Officiis non quibusdam optio illo? Ad, animi facilis repudiandae deleniti ut perferendis
          voluptatem ex quibusdam esse vitae, sed, consectetur voluptates. Corporis repellat quae exercitationem, sed,
          temporibus laudantium quas ea consectetur veritatis at facilis? Natus tempore minima assumenda nemo perspiciatis
          suscipit eius possimus iure molestiae voluptas, ea explicabo consectetur alias, aperiam maiores velit et aut
          adipisci, molestias similique quis voluptates. Est ut quia veniam perspiciatis doloribus nam fugit quaerat,
          tempore
          unde nobis cum dolor quasi ex itaque? Voluptates deleniti velit eius ad asperiores porro possimus eveniet iste
          fugiat natus atque culpa non labore sequi voluptate quas ex quisquam harum ipsum, dignissimos provident minima
          commodi libero. Dolorem impedit omnis reprehenderit amet veritatis inventore voluptatem neque iste unde
          repudiandae
          suscipit, eligendi asperiores placeat, enim rerum minima sequi. Voluptas, excepturi odio repellendus nam illo
          tempore reprehenderit cumque saepe? Quod aspernatur cupiditate doloribus mollitia cum.</p>
      </div>

      <div ref="paragraphSecond">
        <h3>Title2</h3>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eligendi similique pariatur quam culpa nulla nobis
          facere! Voluptate atque ullam libero accusamus nemo eaque hic aliquam illo ipsam maxime nobis sunt maiores
          excepturi
          sapiente praesentium labore quisquam, eveniet impedit eos exercitationem facilis, suscipit fuga! Deleniti
          accusamus
          animi unde placeat autem voluptas commodi, quos impedit eligendi mollitia ab! Molestiae aut, recusandae
          veritatis
          expedita dolor facere totam autem, magni sequi doloremque sunt exercitationem laborum nihil! Animi debitis
          assumenda
          saepe, dolore a numquam hic sequi laboriosam obcaecati doloremque, mollitia iure, amet ipsam sunt eveniet
          nesciunt!
          At accusantium libero sunt hic neque earum nostrum molestiae maiores, quo nobis nulla officiis possimus? Beatae,
          voluptatum. Natus corrupti odio nam quasi hic quisquam molestiae sit non ullam quibusdam eos minima aut eius, in
          maxime recusandae sint doloremque quae numquam inventore velit, vitae culpa praesentium. Rerum accusamus,
          corporis
          eius iure sint ipsum hic quae aut itaque expedita ex eum maiores id sit obcaecati nemo alias ducimus asperiores
          delectus dolores! Officiis non quibusdam optio illo? Ad, animi facilis repudiandae deleniti ut perferendis
          voluptatem ex quibusdam esse vitae, sed, consectetur voluptates. Corporis repellat quae exercitationem, sed,
          temporibus laudantium quas ea consectetur veritatis at facilis? Natus tempore minima assumenda nemo perspiciatis
          suscipit eius possimus iure molestiae voluptas, ea explicabo consectetur alias, aperiam maiores velit et aut
          adipisci, molestias similique quis voluptates. Est ut quia veniam perspiciatis doloribus nam fugit quaerat,
          tempore
          unde nobis cum dolor quasi ex itaque? Voluptates deleniti velit eius ad asperiores porro possimus eveniet iste
          fugiat natus atque culpa non labore sequi voluptate quas ex quisquam harum ipsum, dignissimos provident minima
          commodi libero. Dolorem impedit omnis reprehenderit amet veritatis inventore voluptatem neque iste unde
          repudiandae
          suscipit, eligendi asperiores placeat, enim rerum minima sequi. Voluptas, excepturi odio repellendus nam illo
          tempore reprehenderit cumque saepe? Quod aspernatur cupiditate doloribus mollitia cum.</p>
      </div>

      <div ref="paragraphThird">
        <h3>Title3</h3>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eligendi similique pariatur quam culpa nulla nobis
          facere! Voluptate atque ullam libero accusamus nemo eaque hic aliquam illo ipsam maxime nobis sunt maiores
          excepturi
          sapiente praesentium labore quisquam, eveniet impedit eos exercitationem facilis, suscipit fuga! Deleniti
          accusamus
          animi unde placeat autem voluptas commodi, quos impedit eligendi mollitia ab! Molestiae aut, recusandae
          veritatis
          expedita dolor facere totam autem, magni sequi doloremque sunt exercitationem laborum nihil! Animi debitis
          assumenda
          saepe, dolore a numquam hic sequi laboriosam obcaecati doloremque, mollitia iure, amet ipsam sunt eveniet
          nesciunt!
          At accusantium libero sunt hic neque earum nostrum molestiae maiores, quo nobis nulla officiis possimus? Beatae,
          voluptatum. Natus corrupti odio nam quasi hic quisquam molestiae sit non ullam quibusdam eos minima aut eius, in
          maxime recusandae sint doloremque quae numquam inventore velit, vitae culpa praesentium. Rerum accusamus,
          corporis
          eius iure sint ipsum hic quae aut itaque expedita ex eum maiores id sit obcaecati nemo alias ducimus asperiores
          delectus dolores! Officiis non quibusdam optio illo? Ad, animi facilis repudiandae deleniti ut perferendis
          voluptatem ex quibusdam esse vitae, sed, consectetur voluptates. Corporis repellat quae exercitationem, sed,
          temporibus laudantium quas ea consectetur veritatis at facilis? Natus tempore minima assumenda nemo perspiciatis
          suscipit eius possimus iure molestiae voluptas, ea explicabo consectetur alias, aperiam maiores velit et aut
          adipisci, molestias similique quis voluptates. Est ut quia veniam perspiciatis doloribus nam fugit quaerat,
          tempore
          unde nobis cum dolor quasi ex itaque? Voluptates deleniti velit eius ad asperiores porro possimus eveniet iste
          fugiat natus atque culpa non labore sequi voluptate quas ex quisquam harum ipsum, dignissimos provident minima
          commodi libero. Dolorem impedit omnis reprehenderit amet veritatis inventore voluptatem neque iste unde
          repudiandae
          suscipit, eligendi asperiores placeat, enim rerum minima sequi. Voluptas, excepturi odio repellendus nam illo
          tempore reprehenderit cumque saepe? Quod aspernatur cupiditate doloribus mollitia cum.</p>
      </div>

      <div ref="paragraphFourth">
        <h3>Title4</h3>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eligendi similique pariatur quam culpa nulla nobis
          facere! Voluptate atque ullam libero accusamus nemo eaque hic aliquam illo ipsam maxime nobis sunt maiores
          excepturi
          sapiente praesentium labore quisquam, eveniet impedit eos exercitationem facilis, suscipit fuga! Deleniti
          accusamus
          animi unde placeat autem voluptas commodi, quos impedit eligendi mollitia ab! Molestiae aut, recusandae
          veritatis
          expedita dolor facere totam autem, magni sequi doloremque sunt exercitationem laborum nihil! Animi debitis
          assumenda
          saepe, dolore a numquam hic sequi laboriosam obcaecati doloremque, mollitia iure, amet ipsam sunt eveniet
          nesciunt!
          At accusantium libero sunt hic neque earum nostrum molestiae maiores, quo nobis nulla officiis possimus? Beatae,
          voluptatum. Natus corrupti odio nam quasi hic quisquam molestiae sit non ullam quibusdam eos minima aut eius, in
          maxime recusandae sint doloremque quae numquam inventore velit, vitae culpa praesentium. Rerum accusamus,
          corporis
          eius iure sint ipsum hic quae aut itaque expedita ex eum maiores id sit obcaecati nemo alias ducimus asperiores
          delectus dolores! Officiis non quibusdam optio illo? Ad, animi facilis repudiandae deleniti ut perferendis
          voluptatem ex quibusdam esse vitae, sed, consectetur voluptates. Corporis repellat quae exercitationem, sed,
          temporibus laudantium quas ea consectetur veritatis at facilis? Natus tempore minima assumenda nemo perspiciatis
          suscipit eius possimus iure molestiae voluptas, ea explicabo consectetur alias, aperiam maiores velit et aut
          adipisci, molestias similique quis voluptates. Est ut quia veniam perspiciatis doloribus nam fugit quaerat,
          tempore
          unde nobis cum dolor quasi ex itaque? Voluptates deleniti velit eius ad asperiores porro possimus eveniet iste
          fugiat natus atque culpa non labore sequi voluptate quas ex quisquam harum ipsum, dignissimos provident minima
          commodi libero. Dolorem impedit omnis reprehenderit amet veritatis inventore voluptatem neque iste unde
          repudiandae
          suscipit, eligendi asperiores placeat, enim rerum minima sequi. Voluptas, excepturi odio repellendus nam illo
          tempore reprehenderit cumque saepe? Quod aspernatur cupiditate doloribus mollitia cum.</p>
      </div>

      <div ref="paragraphFifth">
        <h3>Title5</h3>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eligendi similique pariatur quam culpa nulla nobis
          facere! Voluptate atque ullam libero accusamus nemo eaque hic aliquam illo ipsam maxime nobis sunt maiores
          excepturi
          sapiente praesentium labore quisquam, eveniet impedit eos exercitationem facilis, suscipit fuga! Deleniti
          accusamus
          animi unde placeat autem voluptas commodi, quos impedit eligendi mollitia ab! Molestiae aut, recusandae
          veritatis
          expedita dolor facere totam autem, magni sequi doloremque sunt exercitationem laborum nihil! Animi debitis
          assumenda
          saepe, dolore a numquam hic sequi laboriosam obcaecati doloremque, mollitia iure, amet ipsam sunt eveniet
          nesciunt!
          At accusantium libero sunt hic neque earum nostrum molestiae maiores, quo nobis nulla officiis possimus? Beatae,
          voluptatum. Natus corrupti odio nam quasi hic quisquam molestiae sit non ullam quibusdam eos minima aut eius, in
          maxime recusandae sint doloremque quae numquam inventore velit, vitae culpa praesentium. Rerum accusamus,
          corporis
          eius iure sint ipsum hic quae aut itaque expedita ex eum maiores id sit obcaecati nemo alias ducimus asperiores
          delectus dolores! Officiis non quibusdam optio illo? Ad, animi facilis repudiandae deleniti ut perferendis
          voluptatem ex quibusdam esse vitae, sed, consectetur voluptates. Corporis repellat quae exercitationem, sed,
          temporibus laudantium quas ea consectetur veritatis at facilis? Natus tempore minima assumenda nemo perspiciatis
          suscipit eius possimus iure molestiae voluptas, ea explicabo consectetur alias, aperiam maiores velit et aut
          adipisci, molestias similique quis voluptates. Est ut quia veniam perspiciatis doloribus nam fugit quaerat,
          tempore
          unde nobis cum dolor quasi ex itaque? Voluptates deleniti velit eius ad asperiores porro possimus eveniet iste
          fugiat natus atque culpa non labore sequi voluptate quas ex quisquam harum ipsum, dignissimos provident minima
          commodi libero. Dolorem impedit omnis reprehenderit amet veritatis inventore voluptatem neque iste unde
          repudiandae
          suscipit, eligendi asperiores placeat, enim rerum minima sequi. Voluptas, excepturi odio repellendus nam illo
          tempore reprehenderit cumque saepe? Quod aspernatur cupiditate doloribus mollitia cum.</p>
      </div>
    </section>
    <ul>
      <li v-for="(item, index) in titleList">
        <a :class="{ active: activeIndex === index }" href="javascript:;" @click="handleNavClick(index)">{{ item }}</a>
      </li>
    </ul>
  </main>
</template>

<style>
section {
  max-width: 500px;
  height: 80vh;
  overflow-y: scroll;
}

ul {
  position: fixed;
  right: 120px;
  top: 20px;
  list-style: none;
}

a.active {
  color: red;
}
</style>
