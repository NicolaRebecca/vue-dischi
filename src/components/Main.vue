<template>
    <div class="bg">

        <div class="container">

            <div class="row">

                <Album class="cover" 
                v-for="(album,index) in albums" :key="index" 
                :poster="album.poster" 
                :title="album.title" 
                :author="album.author" 
                :year="album.year" />
                    
            </div>
        </div>
    </div>
</template>

<script>
import Album from '../components/Album.vue';
export default {
    name: 'Main',
    components: {
        Album
    },
    props: {
        albums:Array
    }
}
</script>

<style lang="scss" scoped>
    .bg {
        background-color: rgb(29, 45, 59);
        padding-top: 50px;
        padding-bottom: 50px;
        .container {
            .row {
                .cover {
                    
                    width: 20%;
                    
                    
                }
            }
        }
    }
</style>