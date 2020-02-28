<!--
slot is use for render children
-->

<template>
    <div>
        <div class="title">
            <slot name="title">
            </slot>
            <span style="color: #ccc"><slot name="subtitle">subtitle</slot></span>
        </div>
        <div class="content">
            <slot></slot>
        </div>
    </div>

</template>

<script>

</script>

<style scoped>
    div {
        border: 1px solid #ccc;
        box-shadow: 1px 1px 2px black;
        padding: 30px;
        margin: 30px auto;
        text-align: center;
    }
    h1 {
        color: red;
    }
    .title {
        font-size: 24px;
        color: green;
    }
    .content {
        color: cornflowerblue;
    }
</style>