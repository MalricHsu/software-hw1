<script setup>
import { ref } from 'vue'

const navData = ref([
  { id: 1, name: '全部' },
  { id: 2, name: '品牌設計' },
  { id: 3, name: '平面設計' },
  { id: 4, name: 'UIUX設計' },
  { id: 5, name: '網頁設計' },
  { id: 6, name: '設計規範' },
  { id: 7, name: '前端技術' },
  { id: 8, name: '後端架構' },
  { id: 9, name: 'AI趨勢應用' },
])
const navActiveId = ref(1)
const articles = ref([
  {
    id: 1,
    title: '網頁裡的微互動藝術：利用 CSS 與 JS 動畫為諮詢網站注入靈魂並提升用戶轉化率',
    image:
      'https://github.com/hexschool/2022-web-layout-training/blob/main/2026-web-camp/blog_1.png?raw=true',
    categories: ['UIUX 設計', '網頁設計', '前端技術'],
    date: '2022-10-16',
    dateFormatted: 'Oct 16, 2022',
    views: 110,
    shares: 2,
  },
  {
    id: 2,
    title: '10年職人手記：如何運用 Figma 與 Storybook 打造美感與邏輯兼具的企業級設計系統',
    image:
      'https://github.com/hexschool/2022-web-layout-training/blob/main/2026-web-camp/blog_2.png?raw=true',
    categories: ['UIUX 設計', '設計規範', '前端技術'],
    date: '2022-10-16',
    dateFormatted: 'Oct 16, 2022',
    views: 110,
    shares: 2,
  },
  {
    id: 3,
    title: '從平面識別到數位體驗：以「植感生活」為例，探討跨媒體品牌視覺在網頁上的精準轉譯',
    image:
      'https://github.com/hexschool/2022-web-layout-training/blob/main/2026-web-camp/blog_3.png?raw=true',
    categories: ['品牌設計', '平面設計', 'UIUX 設計'],
    date: '2022-10-16',
    dateFormatted: 'Oct 16, 2022',
    views: 110,
    shares: 2,
  },
  {
    id: 4,
    title: '當 AI 遇上介面設計：資深設計師如何利用生成式工具重塑前端開發工作流與視覺想像力',
    image:
      'https://github.com/hexschool/2022-web-layout-training/blob/main/2026-web-camp/blog_4.png?raw=true',
    categories: ['UIUX 設計', '前端技術', 'AI 趨勢應用'],
    date: '2022-10-16',
    dateFormatted: 'Oct 16, 2022',
    views: 110,
    shares: 2,
  },
  {
    id: 5,
    title: '揭開金融 App 的設計密碼：如何優化 Open Bank API 的複雜數據呈現與後端串接安全性',
    image:
      'https://github.com/hexschool/2022-web-layout-training/blob/main/2026-web-camp/blog_5.png?raw=true',
    categories: ['前端技術', '後端架構', 'AI 趨勢應用'],
    date: '2022-10-16',
    dateFormatted: 'Oct 16, 2022',
    views: 110,
    shares: 2,
  },
])
</script>

<template>
  <section class="py-20">
    <div class="container">
      <div class="row">
        <div class="col-lg-2">
          <div class="nav-scroll-container">
            <ul class="list-unstyled custom-nav">
              <li
                class="nav-item text-center fs-heading-xx-small"
                v-for="nav in navData"
                :key="nav.id"
                :class="{ active: nav.id === navActiveId }"
                @click="navActiveId = nav.id"
              >
                {{ nav.name }}
              </li>
            </ul>
          </div>
        </div>
        <div class="col-lg-10">
          <ul class="list-unstyled">
            <li
              class="card-item"
              :class="{ 'mb-6': index < articles.length - 1 }"
              v-for="(article, index) in articles"
              :key="article.id"
            >
              <div class="row">
                <div class="col-md-6">
                  <img
                    :src="article.image"
                    :alt="article.title"
                    class="img-fluid object-fit-cover"
                  />
                </div>
                <div class="col-lg-6 d-flex flex-column justify-content-center">
                  <div class="d-flex align-items-center justify-content-start mb-3">
                    <template v-for="(item, index) in article.categories" :key="item">
                      <span class="fs-paragraph-medium">{{ item }}</span>
                      <span class="mx-2" v-if="index < article.categories.length - 1">·</span>
                    </template>
                  </div>
                  <h3 class="fs-heading-small mb-3">
                    {{ article.title }}
                  </h3>
                  <div class="d-flex justify-content-lg-between align-content-center">
                    <time class="fs-paragraph-small" :datetime="article.date">{{
                      article.dateFormatted
                    }}</time>
                    <div class="d-flex align-items-center">
                      <span class="d-flex me-3">
                        <span class="material-symbols-outlined me-1"> visibility </span
                        >{{ article.views }} views
                      </span>
                      <span class="d-flex">
                        <span class="material-symbols-outlined me-1"> share </span
                        >{{ article.shares }} shares
                      </span>
                    </div>
                  </div>
                </div>
              </div>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>
