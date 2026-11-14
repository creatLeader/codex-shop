<script setup>
import SiteHeader from './components/SiteHeader.vue'
import HeroSection from './components/HeroSection.vue'
import StorySection from './components/StorySection.vue'
import MenuSection from './components/MenuSection.vue'
import VisitSection from './components/VisitSection.vue'
import SiteFooter from './components/SiteFooter.vue'

const dishes = [
  {
    name: '酱香慢炖红烧肉',
    description: '肥而不腻 · 米饭绝配',
    price: '38',
    image: 'https://images.unsplash.com/photo-1512058564366-18510be2db19?auto=format&fit=crop&w=900&q=85',
    alt: '酱香慢炖红烧肉',
  },
  {
    name: '春笋腊味焖饭',
    description: '当季春笋 · 锅气十足',
    price: '32',
    image: 'https://images.unsplash.com/photo-1547592180-85f173990554?auto=format&fit=crop&w=900&q=85',
    alt: '春笋腊味焖饭',
  },
  {
    name: '时蔬手撕鸡',
    description: '清爽鲜嫩 · 每日限量',
    price: '42',
    image: 'https://images.unsplash.com/photo-1512621776951-a57141f2eefd?auto=format&fit=crop&w=900&q=85',
    alt: '时蔬手撕鸡',
  },
]
</script>

<template>
  <SiteHeader />
  <main id="top">
    <HeroSection />
    <div class="ticker" aria-label="餐馆特色">
      <div>今日好好吃饭 <span>✳</span> 鲜香现做 <span>✳</span> 四季有味 <span>✳</span> 街坊小馆 <span>✳</span> 今日好好吃饭 <span>✳</span> 鲜香现做 <span>✳</span> 四季有味 <span>✳</span> 街坊小馆 <span>✳</span></div>
    </div>
    <StorySection />
    <MenuSection :dishes="dishes" />
    <VisitSection />
  </main>
  <SiteFooter />
</template>
