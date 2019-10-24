<template>
  <div>
    修改用户信息{{id}}--{{name}}
  </div>
</template>

<script>
    export default {
        name: "_id",
        layout: "test",
        async asyncData() {
            var a = await  new Promise(function (resolve, reject) {
                setTimeout(function () {
                    console.log(1)
                    resolve(1)
                }, 2000)

            });
            var b = await new Promise(function (resolve, reject) {
                setTimeout(function () {
                    console.log(2)
                    resolve(2)
                }, 1000)

            });

            return {
                name: '黑马程序员'
            }
        },
        data() {
            return {
                id: '',
            }
        },
        methods: {
            // getUser:function () {
            //     this.name="产值博客"
            // }
            a() {
                return new Promise(function (resolve, reject) {
                    setTimeout(function () {
                        resolve(1)
                    }, 2000)

                })
            },
            b(){
                return new Promise(function (resolve, reject) {
                    setTimeout(function () {
                        resolve(2)
                    }, 1000)

                })
            },
        },

        mounted() {
            this.id = this.$route.params.id;
            // this.getUser();
            // this.a().then(res=>{
            //     alert(res)
            // });
            // this.b().then(res=>{
            //     alert(res)
            // })
        }
    }
</script>

<style scoped>

</style>
