<template >
    <div v-if="job">
        <h1>{{ job.title }}</h1>
        <p>The job id is {{ id }}</p>
        <p>{{ job.detail }}</p>
    </div>
    <div v-else>
        <p>Loading job detatils...</p>
    </div>
</template>
<script>
export default {
    props: ['id'],
    name: "JobDetails",
    components: {},
    data() {
        return {
            job: null
        }
    },
    methods: {
        getJob() {
            fetch("http://localhost:3000/jobs/" + this.id)
                .then((res) => res.json())
                .then((data) => this.job = data)
                .catch((err) => console.log(err.message))
        }
    },
    mounted() {
        this.getJob()
    }
}
</script>
<style></style>