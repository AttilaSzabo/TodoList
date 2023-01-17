<template>
    <div class="container">
        <h1>Todolist</h1>
        <form @submit.prevent="newitem()" class="add-value">
            <input v-model="newvalue" class="input" type="text" placeholder="Add value">
        </form>
        <div class="valueContainer">
            <ul class="valuelist">
                <li v-for="(value, index) in values" :key="index" class="valuebox" >
                    <div class="box">
                        <input type="checkbox">
                        <span class="span">
                            {{ value }}
                        </span>
                    </div>
                    <div class="delete">
                        <img @click="delItem(index)" src="../assets/delete.png" alt="">
                    </div>
                </li>
            </ul>
        </div>
    </div>
   
</template>

<script>
    export default {
        data() {
            return {
                newvalue : "",
                values : ["Hallo"]
            }
        },
        methods: {
            newitem: function () {
                if (this.newvalue === "") {
                    alert("adj meg nevet")
                } else {
                    this.values.push(this.newvalue)
                    console.log(this.values)
                    this.newvalue = ""
                }
            },
            delItem: function (kulcs) {
                this.values.splice((kulcs), 1)
            }
        }    
    }
</script>