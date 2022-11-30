<template>
  <div class="nav_boolflix">
    <h1>BOOLFLIX</h1>
    <div class="right_nav">
        <label for="get">
        <input type="text">
    </label>
    <button>CERCA</button>
    </div>

  </div>
</template>

<script>
export default {
  name: 'HeaderBool',
};
</script>

<style lang="scss" scoped>
.nav_boolflix{
    display: flex;
    padding: 1rem;
    justify-content: space-between;
    align-items: center;
    height: 4rem;
    background-color: black;
    h1{
        color: red;
    }
}
.right_nav{
    input{
        margin-right: 1rem;
        padding: .5rem;
        border: none;
        border-radius: 1rem;
    }
    button{
        padding: .5rem;
        border: none;
        border-radius: 1rem;
        cursor: pointer;
    }
}
</style>
