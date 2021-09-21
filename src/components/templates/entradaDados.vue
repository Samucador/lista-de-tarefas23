<template>
  <input @keyup="$emit('input', valorInterno)" @keyup.enter="$emit('enviando') " v-model="valorInterno" type="text"/>
</template>

<script>
export default {
    props: ["value"],
    data() {
        return {
            valorInterno: this.value
        };
    },
};
</script>

<style>
input {
    margin-left: 8px;
    margin-right: 8px;
    border-radius: 5px;
    padding: 5px;
}
</style>