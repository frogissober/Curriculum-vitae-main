<template>
  <div id="skills">
    <div class="block">
      <div class="main-title">{{ $t('skills.title') }}</div>
    </div>

    <div class="block">
      <div class="sub-title">{{ $t('skills.languages') }}</div>
    </div>

    <font-awesome-icon
      :icon="['fab', 'html5']"
      class="icon alt"
      style="font-size: 50px"
    />
    <font-awesome-icon
      :icon="['fab', 'css3']"
      class="icon alt"
      style="font-size: 50px"
    />

    <font-awesome-icon
    :icon="['fab', 'js']"
    class="icon alt"
    style="font-size: 50px"
  />

    <font-awesome-icon
      :icon="['fab', 'php']"
      class="icon alt"
      style="font-size: 50px"
    />
    <font-awesome-icon
      :icon="['fab', 'python']"
      class="icon alt"
      style="font-size: 50px"
    />

    <div class="block">
      <div class="sub-title pt-4">{{ $t('skills.frameworks') }}</div>
    </div>

    <font-awesome-icon
      :icon="['fab', 'laravel']"
      class="icon alt"
      style="font-size: 50px"
    />

      <font-awesome-icon
      :icon="['fab', 'vuejs']"
      class="icon alt"
      style="font-size: 50px"
    />

    <div class="block">
      <div class="sub-title pt-4">{{ $t('skills.other') }}</div>
    </div>

    <div class="block">
      <ul>
        <li v-for="item in $t('skills.otherItems')" :key="item">{{ item }}</li>
      </ul>
    </div>

    <hr />
  </div>
</template>

