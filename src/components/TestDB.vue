<template>
    <div>
        <h1>データベーステスト</h1>
        <button v-on:click="create()">作成</button>
    </div>
</template>

<script>
    import Database from "nedb"
    const testDB = new Database({
        filename: '.test.db'
    });
    testDB.loadDatabase((err)=>{
        if(err != null){
            console.error(err)
        }
        console.log("load db")
    });

    export default {
        name: "TestDB",
        data(){
            return {
                doc:{
                    someString:"aaaa",
                    someNumber:123,
                    someDate: new Date(),
                    someArray: [1,2,3],
                    someObject: {
                        key: "value"
                    }
                }
            }
        },
        methods:{
            create(){
                testDB.insert(this.doc, (error, newDoc) => {
                    if(error != null){
                        console.error(error)
                    }
                    console.log(newDoc)
                    console.log(process.cwd())
                })
            }
        }
    }
</script>

<style scoped>

</style>