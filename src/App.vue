

<template>
  <div id="app">
    <header>
      <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" @click="open" />

      <div  @click="close">
aaa
      </div>
    </header>

    <main>

    </main>
  </div>
</template>

<script setup>

function open(){

 $zoho.salesiq.chat.start()
}


function close(){   
  $zoho.salesiq.reset();

}

</script>


<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
