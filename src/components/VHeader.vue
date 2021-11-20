<template>
    <b-container fluid>
        <b-row no-gutters>
            <b-col no-gutters>
                <b-navbar type="dark" variant="secondary">
                    <b-navbar-brand href="/">Cambra News Corp</b-navbar-brand>
                    <b-navbar-nav>
                        <b-nav-item><router-link to="/">Home</router-link></b-nav-item>
                        <b-nav-item><router-link to="/about">About</router-link></b-nav-item>
                    </b-navbar-nav>
                </b-navbar>
            </b-col>
        </b-row>
    </b-container>
</template>

<script>
export default {
  name: 'VHeader',
}
</script>                     