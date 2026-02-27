<template>
  <div id="over">
    <div class="ik">
      <div class="flex column">
        <span class="naam">floris</span> <span class="achternaam">Bogers</span>
      </div>
        <span class="adres">Nieuwe Heilaarstraat 37 - 4813AR  BREDA - +31 6 36493167 - <span class="email"><a href="mailto:floris@tonbogers.nl">floris@tonbogers.nl</a></span></span>
    </div>
    <div class="content">{{ $t('over.description') }}</div>
    <div class="socials">
      <a href="https://www.linkedin.com/in/floris-bogers-42ab26224/" target="_blank" class="linkedin">
        <div class="circle">
          <font-awesome-icon :icon="['fab', 'linkedin-in']" class="icon alt" style="font-size:30px" />
        </div>
      </a>
      <a href="https://github.com/ItzFloris" target="_blank" class="linkedin">
        <div class="circle">
          <font-awesome-icon :icon="['fab', 'github']" class="icon alt" style="font-size:30px" />
        </div>
      </a>
      
    </div>
    <hr>
  </div>
</template>

