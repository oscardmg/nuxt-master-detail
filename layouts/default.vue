<template>
  <div class="jumbotron jumbtron-fluid">
    <div class="display-4 text-center">
      <img src="~/assets/img/food.png" alt="logo" >
      Restauran App.</div>
    <div class="container">
      <div class="row">
        <div class="col-md-10 offset-md-1">
          <nuxt />
        </div>
      </div>
    </div>
  </div>
</template>

<style>
.jumbotron{
  padding-top: 0px;
  background: #fff;
}

.form-control,.input-group-text{
  border:1px solid #0080ff
}

table.table-hover tbody tr:hover {
  cursor: pointer;
}
</style>
