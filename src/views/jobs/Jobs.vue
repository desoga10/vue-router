<template lang="">
  <div>
<h1>jobs</h1>
<div v-for="job in jobs" :key="job.id" class="job">
<router-link :to="{name: 'JobDetails', params:{id: job.id}}">
  <h2>{{ job.title }}</h2>
</router-link>
</div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      jobs: [
        {
          id: 1,
          title: 'Web Developer',
          company: 'Google',
          description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, voluptatum.',
          created_at: '2021-09-01'
        },
        {
          id: 2,
          title: 'Web Designer',
          company: 'Facebook',
          description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, voluptatum.',
          created_at: '2021-09-01'
        },
        {
          id: 3,
          title: 'Frontend Developer',
          company: 'Apple',
          description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, voluptatum.',
          created_at: '2021-09-01'
        }
      ]
    }
  },
}
</script>
<style >
.job h2{
  background: #f4f4f4;
  padding:20px;
  border-radius: 10px;
  margin: 10px auto;
  max-width: 600px;
  cursor: pointer;
  color: #333;
}

.job h2:hover{
  background: #ccc;
}

.job{
  text-decoration: none;
}
</style>