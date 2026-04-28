<template>
  <div id="ervaring">
    <div class="block">
      <div class="main-title">{{ $t('ervaring.title') }}</div>
    </div>

    <template v-for="item in $t('ervaring.items')">
      <div :key="`${item.company}-meta`" class="block">
        <div class="float-left funktie">{{ item.company }}</div>
        <div class="float-right datum">{{ item.period }}</div>
      </div>

      <div :key="`${item.company}-position`" class="block">
        <div class="sub-title">{{ item.position }}</div>
      </div>

      <div :key="`${item.company}-description`" class="content" style="width: 80%">
        <p>{{ item.description }}</p>
      </div>
    </template>

    <hr>
    
  </div>
</template>

