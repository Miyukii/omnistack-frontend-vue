<template>
    <main>
        <ul>
            <DevItem v-for="dev of devs" v-bind:key="dev.id" :dev="dev"></DevItem>
        </ul>
    </main>
</template>

<script>
    import DevItem from './DevItem';
    import axios from 'axios';

    export default {
        name: 'Main',
        components: {
            DevItem
        },
        data() {
            return {
                devs: [],
                errors: []
            }
        },
        async created () {
            await axios.get('http://localhost:3333/devs')
            .then(response => {
                this.devs = response.data;
            })
        }

    }
</script>

<style>
  main {
    flex: 1;
  }

  main ul {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 20px;
    list-style: none;
    text-align: start;
  }


  @media (max-width: 650px){
    main ul {
        grid-template-columns: 1fr;
    }
  }
</style>
