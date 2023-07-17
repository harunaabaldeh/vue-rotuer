<template >
    <div>
        <h1>Job Details Page</h1>
        <p>The job id is {{ id }}</p>
    </div>
</template>
<script>
export default {
    props: ['id'],
    // name: "JobDetails",
    // components: {},
    // data() {
    //     return {
    //         id: this.$route.params.id
    //     }
    // }
}
</script>
<style></style>