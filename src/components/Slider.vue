<template>
  <div class="slider">

  </div>

</template>

<script>
export default {
  name: 'Slider',
  data: function () {
    return {
      index: 0,
      transition: "transform 0s ease",
    }
  },
  methods: {
    next() {
      console.log(this.index);
      if (this.index === -3465) {
        this.transition = "none";
        this.index = 0;
      } else {
        this.transition = "transform 0s ease";
        this.index -= 385;
      }
    },
    prev() {
      console.log(this.index);
      if (this.index === 0) {
        this.transition = "none";
        this.index = -3465;

      } else {
        this.transition = "transform 0.1s ease";
        this.index += 385;
      }
    }
  }
}

</script>

<style scoped>
.slider {
  width: 500px;
  height: 350px;
  margin: 100px auto 0;
  overflow: hidden;
  position: relative;
  bottom: 100px;
  margin-left: auto;
  margin-right: auto;
  justify-content: center;
}

.img.slider {
  width: 100%;
  height: auto;
}

.container-slides {
  display: flex;
  width: auto;
  margin: auto;
}
.btn {
  background: none;
  outline: 0%;
  border: 0px;
  width: 40px;
  height: 40px;
  padding-bottom: 0%;
  border-radius: 50%;
}

.icone {
  width: 40px;
}

.btn.left {
  top: 50%;
  left: 5px;
  transform: translateY(-50%);
}
.btn.right {
  top: 50%;
  right: 5px;
  transform: translateY(-50%);
}
</style>
