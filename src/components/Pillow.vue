<template>
  <div>
    <img :src="image" />
    <div class="message"> {{ count }}
      <p>
        <button
          @click="decrement"
          type="button"
          class="btn btn-left"
        ><img
            src="@/assets/button/prev.png"
            class="prev"
            v-if="show"
          ></button>
        <button
          @click="increment"
          type="button"
          class="btn btn-right"
        ><img
            src="@/assets/button/next.png"
            class="next"
          ></button>
      </p>
    </div>
  </div>
</template>

<script>

export default {
  data: () => {
    return {
      count: 1,
      show: false,
    }
  },
  computed: {
    image() {
      return require(`@/assets/pillow/${this.count}.png`)
    }
  },
  methods: {
    increment() {
      if (this.count < 10) {
        this.count++;
      } if (this.count != 1) {
        this.show = true;
      }

    },
    decrement() {
      if (this.count > 1) {
        this.count--;
      }
    }
  },
}
</script>

  <style>
.message {
  padding-bottom: 20px;
  font-weight: bold;
  font-family: fantasy;
  color: #5ad8c9;
  font-size: 2rem;
}

.btn {
  outline: none;
  border: none;
  border-radius: 50%;
  justify-content: center;
  align-items: center;
}

.btn.right {
  top: 50%;
  right: 5px;
  transform: translateY(-50%);
}

.btn.left {
  top: 50%;
  left: 5px;
  transform: translateY(-50%);
}
</style>