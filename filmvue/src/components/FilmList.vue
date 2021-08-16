<template>

   <table class="table">
      <thead class="thead-dark">
        <tr>
            <th scope="col">#</th>
            <th scope="col">Tên phim</th>
            <th scope="col">Đạo diễn</th>
            <th scope="col">Năm sản xuất</th>
        </tr>
        </thead>
      <tbody id="array-rendering">
        <tr v-for="(film, index) in films" :key="index" :film="film">
          <th scope="row"></th>
            <td>{{film.name}}</td>
            <td>{{film.directors}}</td>
            <td>{{film.year}}</td>
        </tr>
      </tbody>

  </table>  

  <!-- <ul id="array-rendering">
    <li v-for="(film, index) in films" :key="index" :film="film">
      {{ film.name + " : " + film.directors + " : " + film.year}}
    </li>
  </ul> -->
</template>

<script>
export default {
  props: {
    films: {
      type: Array,
      required: true,
    },
  }
}
</script>

<style scoped>
a {
  color: #42b983;
}
</style>
