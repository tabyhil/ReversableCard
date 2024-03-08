<template>
    <div class="card">
        <div class="front">
            <div>正面</div>
        </div>
        <div class="opposite">
            <div>背面</div>
        </div>
    </div>
</template>

<script setup>

</script>

<style lang="css" scoped>
.card {
    width: 100px;
    height: 100px;
}

.card .front,
.card .opposite {
    position: absolute;
    width: 100px;
    height: 100px;
    transition: all 1s ease;
    backface-visibility: hidden;
}

.card .front {
    background-color: yellow;
}

.card .opposite {
    background-color: green;
    transform: rotateY(180deg);
}

.card:hover .front {
    transform: rotateY(180deg);
}

.card:hover .opposite {
    /* 注意rotate是指定角度 */
    transform: rotateY(0deg);
}
</style>