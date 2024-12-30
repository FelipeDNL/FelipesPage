<template>
  <div class="half-box">

    <div class="local">
      .../src/
    </div>

    <div class="opcoes">
      <slot></slot>
    </div>

  </div>
</template>

<script>
export default {
  props: {
    isSelectable: {
      type: Boolean,
      default: false,
      
    }
  },
  methods: {
    handleClick() {
      if (this.isSelectable) {
        this.$emit('update', 'Informação selecionada');
      }
    }
  }
}
</script>

<style scoped>
.half-box {
  flex: 1;
  border: 2px solid #ccc;
}

.local {
  background-color: dimgray;
}

.opcoes {
  display: flex;
  justify-content: flex-start;
  padding-left: 5px;
}

.opcoes:hover {
  background-color: #a2a1a1;
}
</style>