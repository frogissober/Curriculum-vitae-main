<template>
  <div id="ervaring">
    <div class="block">
      <div class="main-title">{{ $t('ervaring.title') }}</div>
    </div>



    <div class="block"> 
      <div class="float-left funktie">{{ $t('ervaring.curio.company') }}</div>
      <div class="float-right datum">{{ $t('ervaring.curio.period') }}</div>
    </div>

    <div class="block">
      <div class="sub-title">{{ $t('ervaring.curio.position') }}</div>
    </div>

    <div class="content"><p>
      {{ $t('ervaring.curio.description') }}
    </p></div>


    <div class="block"> 
      <div class="float-left funktie">{{ $t('ervaring.company100.company') }}</div>
      <div class="float-right datum">{{ $t('ervaring.company100.period') }}</div>
    </div>

    <div class="block">
      <div class="sub-title">{{ $t('ervaring.company100.position') }}</div>
    </div>
    <div class="content" style="width: 80%"><p>
      {{ $t('ervaring.company100.description') }}
    </p></div>

    <div class="block"> 
      <div class="float-left funktie">{{ $t('ervaring.bounsel.company') }}</div>
      <div class="float-right datum">{{ $t('ervaring.bounsel.period') }}</div>
    </div>

    <div class="block">
      <div class="sub-title">{{ $t('ervaring.bounsel.position') }}</div>
    </div>
    <div class="content" style="width: 80%"><p>
      {{ $t('ervaring.bounsel.description') }}
    </p></div>

    <hr>
    
  </div>
</template>

