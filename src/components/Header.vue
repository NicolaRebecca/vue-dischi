<template>
    <div class="container-fluid">
        <div class="logo">
            <img src="../assets/spotify-logo.png" alt="">
        </div>
        <div class="custom-select">
            <select>
                <option v-for="(album,index) in albums" :key="index">{{album.genre}}</option>
            </select>
            
        </div>
    </div>
    
</template>
 
<script>
export default {
    name: 'Header'
}
</script>

<style lang="scss" scoped>
.container-fluid {
    background-color: rgb(46, 58, 70);
    padding: 15px;
        
    img {
        width: 60px;    
    }
}

.custom-select{
    display: flex;
    margin: 0 auto;
}
</style>