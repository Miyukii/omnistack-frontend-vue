<template>
    <main>
        <ul v-for="dev of devs" v-bind:key="dev.id">
            <DevItem dev={{dev}}/>
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
                devs: []
            }
        },
        async created () {
            await axios.get('http://localhost:3333/devs')
            .then(response => {
                this.devs = response.data;
            })
            .catch(e => {
                console.log(e);
            })
        }
        
    }
</script>