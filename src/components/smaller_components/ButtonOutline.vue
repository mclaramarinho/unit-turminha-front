<template>
    <v-row no-gutters :class="marginBottom && 'mb-3'">
        <v-btn variant="outlined" class="m-auto main-btn">{{ text }}</v-btn>
    </v-row>
</template>

<script lang="ts">
    export default {
        name: 'ButtonOutline',
        props: {
            text: String,
            marginBottom: {
                type: Boolean,
                default: false
            }
        }
    }
</script>

<style scoped>
.v-btn{
    background-color: var(--white) !important;
    border-color: var(--dark-blue) !important;
    color: var(--dark-blue) !important;
    font-weight: 700;
    width: 100%;
    cursor: pointer;
}
.mb-3{
    margin-bottom: 1rem !important;
}

</style>