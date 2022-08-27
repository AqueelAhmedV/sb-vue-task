<template>
<div class="container-fluid d-flex justify-content-around mb-5">
  <div class="stat d-flex flex-column mt-5">
    <span class="stat-head">Total Students</span>
    <span class="stat-data">{{ students }}</span>
  </div>
  <div class="stat d-flex flex-column mt-5">
    <span class="stat-head">Partners</span>
    <span class="stat-data">{{ partners }}</span>
  </div>
  <div class="stat d-flex flex-column mt-5">
    <span class="stat-head">Affiliate Distribution</span>
    <span class="stat-data">{{ affiliate }}</span>
  </div>
</div>
</template>

<script>
    export default {
  name: 'StatsBar',
  props: {
    msg: String
  },
  data: function(){
    return {
      students: 5140,
      partners: 4123,
      affiliate: "4.18 Lac"
    }
  }
}
</script>

<style scoped>



.stat-head {
  font: normal normal bold 2.1875rem/2.9375rem Noto Sans;
letter-spacing: 0px;
color: #86919D;
}
.stat-data {
  font: normal normal bold 4.0625rem/5.5rem Noto Sans;
letter-spacing: 0px;
color: #1F2532;
box-sizing: border-box;
text-decoration-line: underline;
text-decoration-color:  #01CB63;
text-underline-offset: 7px;


}
</style>
