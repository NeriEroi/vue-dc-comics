<template>
    <div>
        <div class="container">
            <div class="all_item">
                <div class="img_cont">
                    <img :src="item.thumb" :alt="item.series">
                </div>
                <h4 class="series">
                    {{ item.series }}
                </h4>
            </div>
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



</style>