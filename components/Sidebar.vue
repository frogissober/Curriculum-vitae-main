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
        <li><a href="#">{{ $t('nav.about') }}</a></li>
        <li><a href="#ervaring">{{ $t('nav.experience') }}</a></li>
        <li><a href="#opleiding">{{ $t('nav.education') }}</a></li>
        <li><a href="#skills">{{ $t('nav.skills') }}</a></li>
        <li><a href="#interesses">{{ $t('nav.hobbies') }}</a></li>
      </ul>
    </nav>
  </div>
</template>

