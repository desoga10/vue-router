<template lang="">
  <div>
<h1>jobs</h1>
<div v-for="job in jobs" :key="job.id">
  <h3>{{ job.title }}</h3>
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
<style lang="">

</style>