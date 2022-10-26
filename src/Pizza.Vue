<template>
     <div>
        <h2>Pizza Name: {{ pizzaName }} // {{ reverseName }}</h2>
        <p>Pizza Price: {{ pizzaPrice }}</p>
        <button @click="changeName"> Change name</button>

     </div>
</template>

<script>
export default {
//    props: ['pizzaName', 'pizzaPrice',],
props: {
    pizzaName: String,
    pizzaPrice: Number,
},
    methods: {
        changeName () {
            this.pizzaName = "Margarita",
            this.$emit ('nameChanged', this.pizzaName)
        },
        
    },
    computed: {
        reverseName () {
            return this.pizzaName.split('').reverse().join('')
    }
}
}

</script>