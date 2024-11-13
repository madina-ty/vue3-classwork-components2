<template>
    <div class="card">
        <div class="card-body">
            <slot></slot>
        </div>
        <i class="fa-solid fa-heart"></i>
    </div>
</template>

<script>
export default {
    name: "PostComp"
}
</script>