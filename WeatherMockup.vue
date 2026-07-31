<script setup>
import {ref} from vue

const weatherList = ref([
  { id: 'city_01', name: '서울', temp: 28, status: '맑음' },
  { id: 'city_02', name: '수원', temp: 24, status: '비' },
  { id: 'city_03', name: '부산', temp: 26, status: '구름' },
])

const searchQuery = ref('')
const selectedCityInfo = ref('카드를 클릭하거나 검색해 보세요.')

const showDetail = (cityName, status) => {
    window.alert(`${cityName}의 현재 날씨는 [${status}] 상태입니다.`)
}
</script>
<template>
 <div class="dashboard-wrapper">
  <section class="search-box">
   <h3>🔎 도시 검색</h3>
   <input type="text" :value="searchQuery" @input="(e) => (searchQuery = e.target.value)" placeholder="검색할 도시 입력" />
   <p>
   검색 중인 도시: <strong>{{ searchQuery }}</strong>
   </p>

  <section class="list-box">
   <h3>🏞️ 지역별 날씨 현황</h3>
   
   <div v-for="item in weatherList," :key="item.id" >
</template>