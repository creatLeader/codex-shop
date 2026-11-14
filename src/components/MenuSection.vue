<script setup>
defineProps({
  dishes: {
    type: Array,
    required: true,
  },
})
</script>

<template>
  <section class="menu-section section" id="menu">
    <div class="menu-heading">
      <div><div class="section-kicker">02 / HOUSE FAVORITES</div><h2>今天的<span>好味道</span></h2></div>
      <a class="text-link" href="#visit">查看完整菜单 <span>↗</span></a>
    </div>
    <div class="dishes">
      <article v-for="(dish, index) in dishes" :key="dish.name" class="dish">
        <div class="dish-photo">
          <img :src="dish.image" :alt="dish.alt" />
          <span class="dish-number">{{ String(index + 1).padStart(2, '0') }}</span>
        </div>
        <div class="dish-info">
          <div><h3>{{ dish.name }}</h3><p>{{ dish.description }}</p></div>
          <b>¥ {{ dish.price }}</b>
        </div>
      </article>
    </div>
    <div class="menu-foot"><span>菜单随季节更替，每天都有一点新鲜事。</span><span>价格以店内菜单为准</span></div>
  </section>
</template>
