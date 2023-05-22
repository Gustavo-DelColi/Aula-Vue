<template>
    <div>
      <h1 :class="{'title':true, 'title-home': isHome}">
        Curso Vue 3
      </h1>
      <p :class="pClass">
        Sem encarar, sem voltar o rosto na direção da pessoa ou coisa para a qual se olha; de esguelha: Olhou-a de soslaio, disfarçadamente.
      </p>
      <p :style="styleClass">
        Olhar de lado , contrário de secar ,que é encarar
      </p>
      
      <img
        src="https://fakeimg.pl/600x400?text=fasdasd"
        v-bind:alt="imgAlt"
      >
      <div
        v-for="(obj, index) in todos"
        v-bind:key="obj.id"
        class="todos-item"
      >
        {{ index }} - {{ obj.title }}
      </div>
    </div>
</template>

<script>
export default {
  name: 'App',
  
  data() {
    return {
      isHome: false,
      classVar: 'title',
      imgAlt: 'Foto de Jon Snow',
      pClass: ['text', 'text-home'],
      styleClass: {'color': 'aqua','backgroundColor': 'red'},
      todos:[
            {
              "userId": 1,
              "id": 1,
              "title": "delectus aut autem",
              "completed": false
            },
            {
              "userId": 1,
              "id": 2,
              "title": "quis ut nam facilis et officia qui",
              "completed": false
            },
            {
              "userId": 1,
              "id": 3,
              "title": "fugiat veniam minus",
              "completed": false
            },
            {
              "userId": 1,
              "id": 4,
              "title": "et porro tempora",
              "completed": true
            },
            {
              "userId": 1,
              "id": 5,
              "title": "laboriosam mollitia et enim quasi adipisci quia provident illum",
              "completed": false
            }
          ]
      }

    }
  }

</script>

<style>
.title{
  font-size:  20px;
  color: blue;
}
.title-home{
  font-size: 40px;
  color: green;
}
.text {
  color: yellow;
}
.text-home{
  color:#42b983;
}
.todos-item{
  background: #000;
  margin: 0 0 5px 0;
  padding: 3px 6px;
  color: #fff

}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
