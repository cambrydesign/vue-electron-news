<template>
  <div>

  </div>
</template>

<script>
export default {
  name: 'Home',
  props: {
      country: String,
  },
  data() {
      return {
          articles: [],
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
