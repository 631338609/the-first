<template>
    <div>
        <h2>学生姓名：{{name}}</h2>
        <h2>学生性别：{{sex}}</h2>
        <h2>学生年龄：{{myAge}}</h2>
        <button @click="updateAge">加年龄</button>
    </div>
</template>
<script>
export default {
    name:'Student',
    data() {
        return {
            // 传进的值进行一个保存，就可以动态改变值在组件中显示
            myAge:this.age
            // name:"申多多",
            // age:18,
            // sex:'女'

        }
    },
    methods:{
        updateAge(){
            this.myAge++;
        }
    },
    // props:['name','sex','age']
    props:{
        name:{
            // 对类型的限制
            type:String,
            // 默认值的限制
            default:'啦啦啦',
            // 必须存在的值，与defaul不会同时存在
            require:true
            },
            
        //对类型限制的简便写法
        age:Number,
        sex:String
    }
}
</script>
