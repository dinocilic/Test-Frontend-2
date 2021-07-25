<template>
    <div class="container main-wrapper">
        <header class="header">
            <h4 class="display-5">
                Home Component
            </h4>
        </header>

        <div class="content">

            <h4 class="display-5">
                List of item components: 
            </h4>
            
            <ul class="list-group" v-for="item in items" :key=item.id>
                <li class="list-group-item">
                    {{ item }}
                </li>
            </ul>

        </div>
    </div>
</template>

<script>
export default {
    name: "Home",
    data () {
        return {
            items: ["Item one", "Item two", "Item three"]
        }
    }
}
</script>

<style scoped>

.main-wrapper {
    display: flex;
    flex-direction: column;
    align-items: center;
    height: 100vh;
    background-color: #EA6903;
}

.header {
    width: 38%;
    position: relative;
    top: 70px;
    text-align: center;
}

.header h4 {
    background-color: #fff;
    padding: 10px;
    color: #000;
}

.content {
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
}

.content h4 {
    color: #000;
    margin-bottom: 25px;
}

</style>