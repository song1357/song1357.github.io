<template>
    <div id="page-top">
        <router-view></router-view>
    </div>
</template>

<script>
    import Resume from './components/resume/resume.vue'
    export default {
      components: {
        appResume: Resume
      }
    }
</script>
