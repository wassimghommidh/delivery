<template>
<div>
    <h2>Add your Restaurant menu</h2>
    <input type="text" class="form-control" v-model="input.name">
    <!-- <span> -->
        <i class="fas fa-minus-circle" @click="remove(k)" v-show="k || ( !k && inputs.length > 1)"></i>
        <i class="fas fa-plus-circle" @click="add(k)" v-show="k == inputs.length-1"></i>
    <!-- </span> -->

    
    </div>
</template>

<script>

export default {
    name :"AdminMenu",
};
</script>