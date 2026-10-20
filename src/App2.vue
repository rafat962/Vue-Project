<
<script>
export default {
    name: "App",
    data() {
        return {
            name: "Vue1",
            status: "pending",
            tasks: ["Task 1", "Task 2", "Task 3"],
            link: "https://www.google.com",
        };
    },
    methods: {
        changeStatus() {
            if (this.status === "pending") {
                this.status = "active";
            } else if (this.status === "active") {
                this.status = "inactive";
            } else {
                this.status = "pending";
            }
        },
    },
};
</script>

<template>
    <h1>{{ name }}</h1>
    <p v-if="status === 'active'">Status: {{ status }}</p>
    <p v-else-if="status === 'pending'">Status: {{ status }}</p>
    <p v-else>User is inactive</p>

    <ul>
        <li v-for="task in tasks" :key="task">
            {{ task }}
        </li>
    </ul>

    <a :href="link" target="_blank">Go to Google</a>

    <button @click="changeStatus">Change status</button>
</template>

<style>
h1 {
    color: red;
}
</style>
