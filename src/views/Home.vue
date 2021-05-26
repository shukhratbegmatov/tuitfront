<template>
  <div class="home">
    {{menu}}
  </div>
</template>
<script>
    import axios from 'axios'
    export default {
        data() {
            return {
                menu: []
            }
        },
        mounted() {
            axios
                .get('http://127.0.0.1:8000/api/menu')
                .then(res => {
                    this.menu = res.data
                    console.log(res.data)
                })
        }

    }
</script>