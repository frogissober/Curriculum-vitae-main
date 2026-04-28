<template>
  <div id="opleiding">
    <div class="block">
      <div class="main-title">{{ $t('opleiding.title') }}</div>
    </div>

    <template v-for="item in $t('opleiding.items')">
      <div :key="`${item.school}-meta`" class="block">
        <div class="float-left funktie">{{ item.school }}</div>
        <div class="float-right datum">{{ item.period }}</div>
      </div>

      <div :key="`${item.school}-degree`" class="block">
        <div class="sub-title">{{ item.degree }}</div>
      </div>

      <div :key="`${item.school}-description`" class="content">
        <p>{{ item.description }}</p>
      </div>
    </template>

    <hr>
    
  </div>
</template>

