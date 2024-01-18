<script setup>
import { ref, reactive } from 'vue'

const render = ref(true)
const items = ref(["Item 1", "Item 2", "Item 3", "Item 4", "Item 5", "Item 6"])
const objects = reactive([
    {
        property_1: 'Value 1',
        property_2: 'Value 2',
        property_3: 'Value 3'
    },
    {
        property_1: 'Value 1',
        property_2: 'Value 2',
        property_3: 'Value 3'
    },
    {
        property_1: 'Value 1',
        property_2: 'Value 2',
        property_3: 'Value 3'
    }
])

</script>

<template>
    <div class="container">
        <h1>Home Page</h1>
        <main>
            <button @click="render = !render">Toggle</button>

            <p v-if="render">
                Texto 1 <br />
                Lorem ipsum dolor sit amet consectetur adipisicing elit.
                Error ducimus sequi quis eum alias? Eius, corporis. Voluptate
                earum voluptatum accusantium inventore cupiditate, recusandae,
                eius, minus reiciendis dolores aperiam sapiente ea?
            </p>
            <p v-else>
                Texto 2 <br />
                Lorem ipsum dolor sit amet consectetur adipisicing elit.
                Error ducimus sequi quis eum alias? Eius, corporis. Voluptate
                earum voluptatum accusantium inventore cupiditate, recusandae,
                eius, minus reiciendis dolores aperiam sapiente ea?
            </p>

            <div>
                <h2 class="list-title">Lista de Items</h2>
                <ul>
                    <li v-for="item in items">
                        {{ item }}
                    </li>
                </ul>

                <h2 class="list-title">Lista de Objetos</h2>
                <ul>
                    <li v-for="(object, index) in objects">
                        <h3>Objeto {{ index }}</h3>
                        <ul>
                            <li v-for="(value, key, index) in object">
                                {{ index }}. {{ key }}: {{ value }}
                            </li>
                        </ul>
                    </li>
                </ul>
            </div>
        </main>
    </div>
</template>

<style>
.container {
    padding-top: 2rem;
    max-width: 1024px;
    margin: auto;
    padding-inline: 2rem;
}

h1 {
    color: #3d648f;
}

p {
    font-size: medium;
}

main {
    display: flex;
    flex-direction: column;
    gap: 1rem;
}

button {
    width: 5rem;
}

.list-title {
    color: #42b883;
}
</style>
