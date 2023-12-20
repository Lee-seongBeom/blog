<template>
  <nav class="navbar navbar-expand-lg bg-body-tertiary">
    <div class="container-fluid">
      <a class="navbar-brand" href="#">블로그</a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav me-auto mb-2 mb-lg-0">
          <li class="nav-item">
            <a class="nav-link active" aria-current="page" href="#">홈</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">기록</a>
          </li>
          <li class="nav-item dropdown">
            <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
              추가메뉴
            </a>
            <ul class="dropdown-menu">
              <li><a class="dropdown-item" href="#">일일 기록</a></li>
              <li><a class="dropdown-item" href="#">정보</a></li>
              <li><hr class="dropdown-divider"></li>
              <li><a class="dropdown-item" href="#">이 외 게시글</a></li>
            </ul>
          </li>
          <li class="nav-item">
            <a class="nav-link disabled" aria-disabled="true">Disabled</a>
          </li>
        </ul>
        <form class="d-flex" role="search">
          <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
          <button class="btn btn-outline-success" type="submit">Search</button>
        </form>
      </div>
    </div>
  </nav>

  <div class="container mt-4">
    <h5>블로그입니다.</h5>
    <p>- Vue로 만듦 -</p> 
  </div>

  <List :블로그글="블로그글" />
</template>

<script>
import List from './components/List.vue';
import blog from './assets/blog.js';

export default {
  name: 'App',
  data(){
    return{
      블로그글 : blog
    }
  },
  components: {
    List : List,
  },
  
}
</script>


<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
