<script>
    export default { 
        // Add code in appropriate places
        data() {
            return {
                items: ['keyboard', 'mouse', 'iPhone', 'macbook', 'adapter']
            }
            
        },
        methods:{
            addItem(){
                if (this.newItem.trim() !== ''){
                    this.items.push(this.newItem);
                    this.newItem = '';
                }
            },
            deleteItem(index){
                // remove the item at the specified index
                this.items.splice(index, 1);
            }
        }
    }
</script>

<template>

    <h2>Shopping Cart</h2>
    <!-- TODO: Add Code Here -->
    <ul id="cart">
        <li v-for="(item, index) in items">{{ item }}
            <button @click="deleteItem(index)">Delete!</button>
        </li>
    </ul>

    <input v-model="newItem"></input>
    <button @click="addItem">Add!</button>
   
</template>
