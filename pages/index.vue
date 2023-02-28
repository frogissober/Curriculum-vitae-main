<template>
  <div>
    <b-container fluid style="padding: 0">
      <b-row no-gutters>
        <b-col cols="col col-xs-12 col-md-2 sticky-top">
          <div class="sticky-top">
            <div class="d-none d-md-block">
              <Sidebar />
            </div>
          </div>
        </b-col>

        <b-col cols="col col-xs-12 col-md-10">
          <Main />
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
export default {}
</script>
