<template>
  <div class="menu">
    <h2>Add your Restaurant menu</h2>
    <div v-for="(input, index) in foodTypes" :key="`foodInput-${index}`">
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
          id="price"
          type="number"
          name="price"
          class="form-control"
          placeholder="Price"
          v-model="input.food"
        />
      </div>
    </div>
    <div style="text-align: center; margin-top: 30px">
      <hr class="main-hr" />
      <button
        class="icon-btn add-btn"
        id="hello"
        @click="addField(input, foodTypes)"
      >
        <div class="btn-txt">Add</div>
      </button>
      <button class="icon-btn add-btn" @click="removeField(input, foodTypes)">
        <div class="btn-txt">Remove</div>
      </button>
    </div>
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
</script>

<style>
.menu {
  display: flex;
  flex-direction: column;
  align-items: center;
}
#price {
  margin-left: 45px;
}

.main-hr {
  width: 30%;
  border: none;
  border-top: 1px solid #c3c3c3;
}
.icon-btn {
  width: 50px;
  height: 50px;
  border: 1px solid #cdcdcd;
  background: white;
  border-radius: 25px;
  overflow: hidden;
  position: relative;
  transition: width 0.2s ease-in-out;
}
.add-btn:hover {
  width: 120px;
}
.add-btn::before,
.add-btn::after {
  transition: width 0.2s ease-in-out, border-radius 0.2s ease-in-out;
  content: "";
  position: absolute;
  height: 4px;
  width: 10px;
  top: calc(50% - 2px);
  background: red;
}
.add-btn::after {
  right: 14px;
  overflow: hidden;
  border-top-right-radius: 2px;
  border-bottom-right-radius: 2px;
}
.add-btn::before {
  left: 14px;
  border-top-left-radius: 2px;
  border-bottom-left-radius: 2px;
}
.icon-btn:focus {
  outline: none;
}
.btn-txt {
  opacity: 0;
  transition: opacity 0.2s;
}
.add-btn:hover::before,
.add-btn:hover::after {
  width: 4px;
  border-radius: 2px;
}
.add-btn:hover .btn-txt {
  opacity: 1;
}
.add-icon::after,
.add-icon::before {
  transition: all 0.2s ease-in-out;
  content: "";
  position: absolute;
  height: 20px;
  width: 2px;
  top: calc(50% - 10px);
  background: red;
  overflow: hidden;
}
.add-icon::before {
  left: 22px;
  border-top-left-radius: 2px;
  border-bottom-left-radius: 2px;
}
.add-icon::after {
  right: 22px;
  border-top-right-radius: 2px;
  border-bottom-right-radius: 2px;
}
.add-btn:hover .add-icon::before {
  left: 15px;
  height: 4px;
  top: calc(50% - 2px);
}
.add-btn:hover .add-icon::after {
  right: 15px;
  height: 4px;
  top: calc(50% - 2px);
}
</style>
