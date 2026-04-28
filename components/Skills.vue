<template>
  <div id="skills">
    <div class="block">
      <div class="main-title">{{ $t('skills.title') }}</div>
    </div>

    <div class="skills-list">
      <div
        v-for="category in $t('skills.categories')"
        :key="category.name"
        class="skills-category"
      >
        <div class="skills-category-title">{{ category.name }}</div>
        <ul class="skills-items">
          <li v-for="item in category.items" :key="item" class="skills-item">
            {{ item }}
          </li>
        </ul>
      </div>
    </div>

    <hr />
  </div>
</template>
