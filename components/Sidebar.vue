<template>
  <div id="sidebar">
    <div class="profile-picture">
      <img src="~/assets/images/floris2.png" />
    </div>
    <div class="language-switcher">
      <button 
        v-for="locale in $i18n.locales" 
        :key="locale"
        :class="{ active: locale === $i18n.locale }"
        @click="$i18n.setLocale(locale)"
        class="lang-btn"
      >
        {{ locale.toUpperCase() }}
      </button>
    </div>
    <nav>
      <ul>
        <li v-for="item in $t('nav.items')" :key="item.href">
          <a :href="item.href">{{ item.label }}</a>
        </li>
      </ul>
    </nav>
  </div>
</template>

