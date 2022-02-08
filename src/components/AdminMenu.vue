<template>
  <div class="menu">
    <h2>Add your Restaurant menu</h2>
    <div  v-for="(input, index) in foodTypes"
          :key="`foodInput-${index}`">
      <label>Food name</label>
      <input
        type="text"
        name="food"
        class="from-control"
        placeholder="Your food here "
        v-model="input.food"
      />

      <div class="col-4">
        <label>Price</label>
        <input
          type="number"
          name="price"
          class="form-control"
          placeholder="Price"
          v-model="input.food"
        />
      </div>
    </div>
    <button class="hello" @click="addField(input, foodTypes)">Add more</button>
    <button class="hello" @click="removeField(input, foodTypes)">Add more</button>
  </div>
</template>

<script>
export default {
  name: "AdminMenu",
  data() {
    return {
      foodTypes: [{ food: "" }],
    };
  },
  methods: {
    addField(value, fieldType) {
      fieldType.push({ value: "" });
    },
    removeField(index, fieldType) {
      fieldType.splice(index, 1);
    },
  },
};
// app.addMore()
</script>
