<script setup>
import { ref } from 'vue'

const color = ref(true)
</script>

<template>
    <div class="container">
        <h1>About Page</h1>
        <main>
            <p>
                Lorem ipsum dolor, sit amet consectetur adipisicing elit.
                Ducimus reiciendis eos expedita dolorum? Porro mollitia 
                necessitatibus nihil molestiae aliquid, quibusdam distinctio. 
                Ipsam provident magni quisquam commodi nulla recusandae iusto repellat?
            </p>
        </main>
    </div>
</template>

<style>
.container {
    padding-top: 2rem;
    max-width: 1024px;
    margin: auto;
}

p {
    font-size: medium;
}
</style>
