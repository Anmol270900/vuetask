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
                
            }
            //this.number = ''
        }
    }
}
</script>

<style scoped>
form {
        display: flex;
    }
    input[type="text"] {
        flex: 10;
        padding: 5px;
    }
    input[type="submit"] {
        flex: 2;
    }
</style>
