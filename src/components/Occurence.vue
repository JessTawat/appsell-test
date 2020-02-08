<template>
    <div>
        <input
        type="email"
        class="form-control"
        placeholder="tweet something here ..."
        v-model="Obj"/>
        <button v-on:click="tweeter(Obj)">Tweet!</button>

        <h1>{{ occuredWord }}</h1>
    </div>
</template>

<script>
export default {
    data () {
        return {
            Obj: '',
            occuredWord: ''
        }
    },

    methods: {
        tweeter (val) {
            let arr = val.split('').sort().join('');

            return this.occuredWord = arr;
        }


    }
}
</script>