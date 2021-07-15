<template>
    <div class="album-container">
        <div class="album-details">
            <img :src="poster" alt="">
            <h5>{{ title }}</h5>
            <div class="author">{{ author }}</div>  
            <div class="year">{{ year}}</div>     
        </div>
    </div>
</template>

<script>
export default {
    name: 'Album',
    props: {
        poster: String,
        title: String,
        author: String,
        year: String
    }
}
</script>

<style lang="scss" scoped>
    
    .album-container {
        text-align: center;
        .album-details {
            margin: 15px 10px;
            background-color: rgb(48, 58, 68);
            padding: 20px;
            height: 390px;
            
            img {
                width: 100%;
            }
            
            h5 {
                color: cadetblue;
                padding: 15px 0;
            }
            
            .author, .year {
                color: rgb(110, 110, 110);
            }
        }
    }
</style>