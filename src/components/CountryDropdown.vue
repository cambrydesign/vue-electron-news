<template>
    <b-nav-item-dropdown class="country-dropdown" text="Country" right>
        <b-dropdown-item href="" v-for="country in countries" :key="country.alpha2Code">
            {{ country.name }}
        </b-dropdown-item>
    </b-nav-item-dropdown>
</template>

<script>
export default {
  name: 'CountryDropdown',
  data() {
      return {
          countries: [],
      }
  },
  methods: {
      async getCountries() {
          try {
              const response = await this.$http.get(
                  'https://restcountries.com/v2/all?fields=name,alpha2Code'
              );
              this.countries = response.data;
          } catch (e) {
              console.log(e);
          }
      }
  },
  created() {
      this.getCountries();
  }
}
</script>