<template>
  <a-layout style="margin: 24px; padding: '24px'">
    <a-row :gutter="32">
      <a-col :span="8">
        <div class="card">
          <a-layout-content
            :style="{background: '#fff', boxShadow: '0 2px 5px rgba(0,21,41,.13)',
            borderRadius: '10px 10px 10px 10px', height: '130px'}"
          >
            <a-row>
              <a-col :span="10">
                <div class="card-icon">
                  <a-icon type="clock-circle"/>
                </div>
              </a-col>
              <a-col :span="14">
                <div class="card-info">
                  <span class="title">Avg. Waiting Time (min)</span>
                  <span class="value">{{companyStats.avgWaitingTime}}</span>
                </div>
              </a-col>
            </a-row>
          </a-layout-content>
        </div>
      </a-col>
      <a-col :span="8">
        <div class="card">
          <a-layout-content
            :style="{background: '#fff', boxShadow: '0 2px 5px rgba(0,21,41,.13)',
            borderRadius: '10px 10px 10px 10px', height: '130px'}"
          >
            <a-row>
              <a-col :span="10">
                <div class="card-icon">
                  <a-icon type="clock-circle" />
                </div>
              </a-col>
              <a-col :span="14">
                <div class="card-info">
                  <span class="title">Avg. Respose Time (min)</span>
                  <span class="value">{{ companyStats.avgResTime }}</span>
                </div>
              </a-col>
            </a-row>
          </a-layout-content>
        </div>
      </a-col>
      <a-col :span="8">
        <div class="card">
          <a-layout-content
            :style="{background: '#fff', boxShadow: '0 2px 5px rgba(0,21,41,.13)',
            borderRadius: '10px 10px 10px 10px', height: '130px'}"
          >
            <a-row>
              <a-col :span="10">
                <div class="card-icon">
                  <a-icon type="radar-chart" />
                </div>
              </a-col>
              <a-col :span="14">
                <div class="card-info">
                  <span class="title">Avg. Accuracy</span>
                  <span class="value">{{ companyStats.avgAccuracy }}</span>
                </div>
              </a-col>
            </a-row>
          </a-layout-content>
        </div>
      </a-col>
    </a-row>
  </a-layout>
</template>
<script>
export default {
  props: ['companyStats']
}
</script>
<style scoped>

.card {
  transition: all .3s ease-in-out;
}

.card:hover {
  cursor: pointer;
  transform: scale(1.05);

}
.card .card-icon {
  background-color: #001529;
  color: white;
  text-align: center;
  font-size: 60px;
  padding: 20px 0;
  border-radius: 10px 0 0 10px;
  height: 130px
}
.card-info {
  text-align: center;
}

.card-info span {
  display: block;
}
.card-info span.title {
  margin-top: 15px
}
.card-info span.value {
  font-size: 40px;
  font-weight: bold;
  margin-top: 4px;
}
</style>
