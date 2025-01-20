<script>
export default {
    name: "ComicsList",
    props: ["fumetti"],
    data() {
        return {

        }
    }
}
</script>

<template>
    <div class="card">
        <img :src="fumetti.thumb" alt="">
        <p class="text-white">{{ fumetti.series }}</p>
    </div>
</template>

<!-- CSS -->
<style scoped>
.card {
    background: #222;
    border: none;
    margin: 1rem; /* Add margin around cards */
    display: flex; /* Use flexbox for card content */
    flex-direction: column; /* Stack content vertically */
    align-items: center; /* Center content inside the card */
    width: 100%; /* Allow cards to take full width */

}

.card img {
    height: 100%;
    width: 100%; /* Make image responsive */
    object-fit: cover; /* Maintain aspect ratio */
}

.card p {
    color: white; /* Ensure text is white */
    text-align: center; /* Center text */
    padding: 0.5rem;
}

/* Responsive styles */
@media (max-width: 768px) {
    .card {
        width: 100%; /* Allow cards to take more width on mobile */
    }
}
</style>