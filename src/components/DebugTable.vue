<template>
    <div>
        <h1>デバッグ用テーブル</h1>
        <vue-good-table
                :columns="columns"
                :rows="rows"/>
    </div>
</template>

<script>
    import 'vue-good-table/dist/vue-good-table.css'
    import { VueGoodTable } from 'vue-good-table';

    // add to component

    export default {
        name: 'DebugTable',
        components: {
            VueGoodTable,
        },
        data(){
            return {
                columns: [
                    {
                        label: 'AAA',
                        field: 'name',
                    },
                    {
                        label: 'Age',
                        field: 'age',
                        type: 'number',
                    },
                    {
                        label: 'Created On',
                        field: 'createdAt',
                        type: 'date',
                        dateInputFormat: 'yyyy-MM-dd',
                        dateOutputFormat: 'MMM Do yy',
                    },
                    {
                        label: 'Percent',
                        field: 'score',
                        type: 'percentage',
                    },
                ],
                rows: [
                    { id:1, name:"John", age: 20, createdAt: '2011-10-31',score: 0.03343 },
                    { id:2, name:"Jane", age: 24, createdAt: '2011-10-31', score: 0.03343 },
                ],
            };
        },
    };
</script>


<style scoped>

</style>