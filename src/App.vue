<script setup>
import { onMounted } from "vue";

const conectSSE = () => {
    const token = "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MSwidXNlcm5hbWUiOiJzdWRvIiwiaWF0IjoxNzI5NTc5ODAwLCJleHAiOjE3NjExMTU4MDB9.R8xMt79jZymHjdJN_gjkTSjeotrAx-7_EUwPj3epeG0";

    const url = `https://api-gh.melonku.id/events/updated-sensor?token=${token}`;
    const eventSource = new EventSource(url);

    // Menerima pesan dari server
    eventSource.onmessage = function (event) {
        const eventData = JSON.parse(event.data);

        console.log(eventData);
    };

    eventSource.onerror = function (err) {
        console.error("EventSource failed:", err);
    };
};

onMounted(() => {
    conectSSE();
});
</script>

<template>
    <router-view />
</template>
