<template>
  <div class="hello">
    <form @submit="checkNum">
            <input type="text" v-model="number" name="number" placeholder="Enter number">
            <input type="submit" value="Submit" class="btn">
    </form>
  </div>
</template>

<script>
export default {
  name: 'Number',
  data() {
    return {
        number: ''
   }
  },
  methods: {
        checkNum() {
            if(isNaN(this.number))
            {
                alert('Please enter a numeric value');
            }
            else
            {
                this.$emit('calCube', this.number);
                this.number = ''
            }
        }
    }
}
</script>

<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
