<script lang="ts">
import { ref, defineComponent } from 'vue';

type Data = {
  nmae: string;
  age: number;
}
export default defineComponent({
  name: 'HelloWorld',
  props: {
    msg: {
      type: String,
      required: true,
    },
  },
  setup: () => {
    const count = ref(0);

    const add = () => {
      count.value += 1;
    };
    return { count, add };
  },
  data() {
    return {
      name: 'milkmidi',
      age: 18,
    } as Data;
  },
  mounted() {
    console.log(this.name);
  },
});
</script>

<template>
  <h1>{{ msg }}, {{ name }}, {{ age }}</h1>
  <button @click="add('123')">
    count is: {{ count }}
  </button>
  <p>
    Edit
    <code>components/HelloWorld.vue</code> to test hot module replacement.
  </p>
</template>

<style scoped>
a {
  color: #42b983;
}

label {
  margin: 0 0.5em;
  font-weight: bold;
}

code {
  background-color: #eee;
  padding: 2px 4px;
  border-radius: 4px;
  color: #304455;
}
</style>
