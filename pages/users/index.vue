<template>
  <div>
      hola
  </div>
</template>

<script>
export default {

    data: () => ({
        resource: 'user',
        search: '',
        data: {},
    }),

    created() {
        this.getData()
    },

    methods: {
        getData( page=1 ){
            this.$axios.get('/users')
            .then( res => {
                data = res.data;
                console.log(data)
            }) 
            .catch( err => {
                console.log(err.response)
            })
            
        }    
    },

    
}
</script>

<style>

</style>