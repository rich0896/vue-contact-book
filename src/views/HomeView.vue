<script setup>
import { ref } from 'vue';

const contacts = ref([
    { id: 1, name: 'John Doe', email: 'johndoe@email.com', phone: '123-456-7890' },
    { id: 2, name: 'Jane Doe', email: 'janedoe@email.com', phone: '123-456-7890' },
    { id: 3, name: 'John Smith', email: 'johnsmith@email.com', phone: '123-456-7890' },
]);
</script>

<template>
    <div class="contact-list">
        <ul>
            <li v-for="contact in contacts" :key="contact.id">
                <div class="contact-details">
                    <h2>{{ contact.name }}</h2>
                    <div class="contact-values">
                        <p>{{ contact.email }}</p>
                        <p>{{ contact.phone }}</p>
                    </div>
                </div>
                <div class="contact-options">
                    <button aria-label="Edit Contact">Edit</button>
                    <button aria-label="Delete Contact" class="delete-button">Delete</button>
                </div>
            </li>
        </ul>
    </div>
</template>

<style scoped>
ul {
    list-style: none;
    padding: 0;
    margin: 0;
}

li {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0.2rem 1rem;
    border-bottom: 1px solid #444;
    color: white;
}

.contact-details {
    flex: 1;
    display: grid;
    grid-template-columns: 1fr 3fr;
    /* gap: 0.7rem; */
}

.contact-values {
    display: flex;
    flex-direction: row;
    align-items: center;
    /* justify-content: space-between; */
    gap: 0.7rem;
    color: #999;
}

.contact-options {
    display: flex;
    gap: 1rem;
}

button {
    padding: 0.5rem;
    border: none;
    border-radius: 0.25rem;
    background-color: white;
    color: #202020;
    cursor: pointer;
}

button:hover, button:focus {
    background-color: #eee;
}

button:active {
    background-color: #ddd;
}

.delete-button {
    background-color: #ff0000;
    color: white;
}

.delete-button:hover, .delete-button:focus {
    background-color: #ff6666;
}

.delete-button:active {
    background-color: #000;
    color: white;
}
</style>