<template>
    <b-navbar class="mb-3 px-3" type="dark" variant="secondary">
        <b-navbar-brand href="/">Cambra News Corp</b-navbar-brand>
        <b-navbar-nav>
            <b-nav-item><router-link to="/">Home</router-link></b-nav-item>
            <b-nav-item><router-link to="/about">About</router-link></b-nav-item>
        </b-navbar-nav>
        <b-navbar-nav class="ml-auto">
            <country-dropdown></country-dropdown>
        </b-navbar-nav>
    </b-navbar>
</template>

<script>
import CountryDropdown from "@/components/CountryDropdown";
export default {
  name: 'VHeader',
  components: {
      CountryDropdown
  }
}
</script>