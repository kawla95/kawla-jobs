<template>
  <h1> Job List</h1>
  <div v-for=" job in jobs" :key="job.id" class="job">
    <router-link :to="{name: 'JobDetails', params: {id: job.id}}"> {{ job.title }} </router-link>

  </div>
</template>

<script>
export default {
    data() {
        return {
            jobs: [ 
            {title: "web developer", id: 1, details: "lorem"},
            {title: "graphic designer", id: 2, details: "lorem"},
            {title: "data analyst", id: 3, details: "lorem"}
        ]
           
        }
    }


}
</script>

<style>

.job {
  background: #f4f4f4;
  padding: 20px; 
  border-radius: 10px;
  margin: 10px auto; 
  max-width: 600px;
  cursor: pointer; 
  color: #444;
}
.job h2:hover {
  background: #ddd;
}

.job a{
  text-decoration: none;
}


</style>