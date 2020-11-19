<template>
  <div class="home">
    <table cellspacing="0">
      <tr>
        <td>选项1</td>
        <td>选项2</td>
        <td>选项3</td>
        <td>选项4</td>
        <td>选项5</td>
      </tr>
      <tr v-for="(item, index) in list" :key="index">
        <td><input type="checkbox" :checked='false' @click="getcheck(index)"/></td>
        <td>{{ item.a }}</td>
        <td>{{ item.b }}</td>
        <td>{{ item.c }}</td>
        <td>{{ item.d }}</td>
      </tr>
    </table>

    <button>shang</button>
    <button @click="shan">xia</button>
  </div>
</template>

<script>
export default {
  name: "Home",
  data() {
    return {
      in:[],
      list: [
        { a: "1-1", b: "1-2", c: "1-3", d: "1-4" },
        { a: "2-1", b: "2-2", c: "2-3", d: "2-4" },
        { a: "3-1", b: "3-2", c: "3-3", d: "3-4" },
        { a: "4-1", b: "4-2", c: "4-3", d: "4-4" },
        { a: "5-1", b: "5-2", c: "5-3", d: "5-4" },
        { a: "6-1", b: "6-2", c: "6-3", d: "6-4" },
        { a: "7-1", b: "7-2", c: "7-3", d: "7-4" },
        { a: "8-1", b: "8-2", c: "8-3", d: "8-4" },
      ],
      
    };
  },
  methods:{
    getcheck(index){
      console.log(event.target.checked,index);
      
      if(event.target.checked==true && this.in.indexOf(index)== -1){
            this.in.push(index)
      }else if(event.target.checked==false){
         this.in.indexOf(index)
         this.in.splice(this.in.indexOf(index),1)
      }
    },
    shan(){
      for ( let i = 0; i<this.in.length;i++){
        
      }
  },},
  components: {},
};
</script>
<style lang="less" scoped>
td {
  border: 1px solid red;
  width: 200px;
}
</style>
