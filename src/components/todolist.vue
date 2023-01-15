<template>
    <div class="container">
        <h1>Todolist</h1>
        <ul class="unList">
            <li v-for="(kincs, index) in card" :key="index">
                {{ kincs }}
            </li>
        </ul>
        <form @submit.prevent="card.push(news)" class="form">
            <input v-model="news" class="text" type="text" placeholder="add value">
            <input class="submit" type="submit" value="Submit">
        </form>
        <p>
            {{ news }}
        </p>  
    </div>
</template>

<script>
    export default {
        data() {
            return {
                news: "",
                card: ["Welcome!"]
            }
        }
    }
</script>

<style>

    * {
        list-style: none;
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }

    body {
        background-color: rgb(56,56,56);
    }

    .container {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        text-align: center;
    }

    .container h1 {
        color: whitesmoke;
    }

    .unList li{
        background-color: rgb(0, 0, 0);
        margin: 5px;
        padding: 5px;
        border-radius: 5px;
        color: #daba55;
    }

    .form {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    .text {
        text-align: center;
        border: none;
        padding: 5px 10px;
        border-radius: 5px;
        margin: 15px 0 20px 0;
    }

    .submit {
        border: none;
        padding: 5px 10px;
        border-radius: 5px;
        background-color: #daba55;
        color: black;
        font-weight: 600;
        box-shadow: inset 0px 0px 10px rgb(32, 32, 32);
        transition: 0.3s;
        margin: 10px;
    }

    .submit:hover {
        transform: translateY(-5px);
        box-shadow: 5px 5px 5px black;
    }

</style>