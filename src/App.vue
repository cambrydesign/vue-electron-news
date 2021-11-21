<template>
<div>
    <v-header></v-header>
    <v-sidebar></v-sidebar>
    <b-container>
        <b-row>
            <b-col>
                <b-button v-b-toggle.sidebar-filter>Filter News</b-button>
            </b-col>
        </b-row>
        <b-row>
            <b-col>
                <router-view/>
            </b-col>
        </b-row>
    </b-container>
</div>
</template>

<script>
    import VHeader from "./components/VHeader";
    import VSidebar from "./components/VSidebar";
    export default {
        components: {
            VHeader,
            VSidebar,
        }
    }
</script>


<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
