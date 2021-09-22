<template>

    <div>
        
        <div class="all_item">
            <div class="img_cont">
                <img :src="item.thumb" :alt="item.series">
            </div>
            <h4 class="series">
                {{ item.series }}
            </h4>
        </div>

    </div>

    
</template>

<script>
export default {
    name: 'Fumetti',
    props: ['item']
}
</script>

<style>

    .all_item {
       width: 250px;
       height: 100px;
       display: flex;
       flex-direction: column;
       justify-content: center;
    } .img_cont {
        width: 150px;
        height: 150px;
    } img {
        width: 100%;
        height: 100%;
        object-fit: cover;
    }
    h4 {
        width: 150px;
        color: white;
    } 

  
   
</style>