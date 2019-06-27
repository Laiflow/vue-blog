<template>
  <div class="container">
            <a >{{title}}</a>
    <div class="post" v-for="item in bloglist" :key="item.title">
                <h1>
                            <router-link :to="'/views/' + item._id" >
<a >{{item.title}}</a>
                            </router-link>
                </h1>

                <div class="thumbnail-container">
                    <a>
                      <img :src="item.image"></a>
                </div>

                <p >
                   <a v-html=item.body> </a> <a>Read
                        more</a>
                    <span class="post-date">
                        <i class="fa fa-calendar" aria-hidden="true"></i> 
                    <fmt:formatDate value=item.created_at pattern="yyyy-MM-dd" />
                    {{item.created_at}} - 
                        <i class="fa fa-clock-o" aria-hidden="true"></i>

                        1 minute read 


                    </span>
                </p>
            </div>

  </div>
</template>

<script>
// @ is an alias to /src
export default {
  name: 'home',
  //   props: {
  //   posts
  // },
  data(){
    return {
     bloglist: [],
    }
  },
  mounted() {
    this.getPosts();
  },
  methods: {
    getPosts() {
      this.$http.get("http://127.0.0.1:3334/posts").then(result => {
      this.bloglist = result.data
      window.console.log(result.data)

});
}
  }
}
</script>

<style>
a {
    text-decoration: underline;
    color: #333;
    text-decoration: none;
}
img {
    max-width: 100%;
    height: auto;
    border-radius: 5px;
}
.thumbnail-container img {
    margin-top: -11.5%;
    margin-bottom: -11.5%;
}
.container{
  margin-left: auto;
  margin-right: auto;
  width: 615px;
}
.posts {
    margin-bottom: 5rem;
    padding: 0px;
    list-style: none;
}
.thumbnail-container {
    max-width: 100%;
    overflow: hidden;
    border-radius: 5px;
    margin-bottom: 25px;
}
</style>
