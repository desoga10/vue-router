<template >
  <div v-if="job">
    <h1>{{ job.title }}</h1>
    <p>The Job ID is {{ id }}</p>
    <p>{{ job.description }}</p>
  </div>
  <div v-else>
    <p>Loading Job Description...</p>
  </div>
</template>
<script>
export default {
  props: ['id'],
  data() {
    return {
      job: null
    }
  },
  mounted() {
    fetch('http://localhost:3000/jobs/' + this.id)
      .then(response => response.json())
      .then(data => {
        this.job = data
      }).catch(error => {
        console.log(error)
      })
  }
}
</script>
<style ></style>