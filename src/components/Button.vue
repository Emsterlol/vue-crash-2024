<template>
    <button @click="onClick" :style=" { background: color }" class="btn">{{ text }} </button>
  </template>
  
  <script>
  export default {
    name: 'Button',
    props: {
      text: {
        type: String,
        required: true,
      },
      color: {
        type: String,
        required: true,
      },
    },
    methods: {
      onClick() {
        this.$emit('btn-click');
      }
    }
  }
  </script>

<style scoped>
.btn {
  color: white;
  font-size: 15px;
  padding: 10px 20px;
  margin: 5px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  text-decoration: none;
  display: inline-block;
  font-family: inherit;
}

.btn:focus {
  outline: none;
}

.btn:active {
  transform: scale(0.98);
}
</style>