<template>
  <div>
        <Header />
        
        <main>
            <h1>Guest Home</h1>
        </main>

        <Footer />
  </div>
</template>

<script>

import Header from './components/partials/Header';
import Footer from './components/partials/Footer';

export default {
    name: "App",
    components: {
        Header,
        Footer
    }
}
</script>

<style>

</style>