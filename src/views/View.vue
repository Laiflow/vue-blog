<template>

<div class="container">

    <div class="post-container">
      <h1>
{{postinfo.title}}</h1>


  <img :src="postinfo.image">

<div v-html="postinfo.body"> </div>
 

<span class="post-date">
  Written on
  
  January
  1st
    ,
  2016
  by
  
    Paul Le
  
</span>

<div class="post-date">Feel free to share!</div>
  <div class="sharing-icons">
    <a href="https://twitter.com/intent/tweet?text=Welcome to Lagrange!&amp;url=https://lenpaul.github.io/Lagrange/journal/welcome-to-lagrange.html" target="_blank"><i class="fa fa-twitter" aria-hidden="true"></i></a>
    <a href="https://www.facebook.com/sharer/sharer.php?u=https://lenpaul.github.io/Lagrange/journal/welcome-to-lagrange.html&amp;title=Welcome to Lagrange!" target="_blank"><i class="fa fa-facebook" aria-hidden="true"></i></a>
    <a href="https://plus.google.com/share?url=https://lenpaul.github.io/Lagrange/journal/welcome-to-lagrange.html" target="_blank"><i class="fa fa-google-plus" aria-hidden="true"></i></a>
  </div>
</div>


<div class="related">
  <h1 >You may also enjoy:</h1>
  
  <ul class="related-posts">
    
      
        
        
      
        
          <li>
            <h3>
              <a href="https://lenpaul.github.io/Lagrange/journal/getting-started.html">
                Getting Started
                <!--<img src="https://lenpaul.github.io/Lagrange/images/">-->
                <!--<small>October 10, 2015</small>-->
              </a>
            </h3>
          </li>
          
        
      
        
          <li>
            <h3>
              <a href="https://lenpaul.github.io/Lagrange/journal/text-formatting-examples.html">
                Text Formatting Examples
                <!--<img src="https://lenpaul.github.io/Lagrange/images/">-->
                <!--<small>January 1, 2014</small>-->
              </a>
            </h3>
          </li>
          
        
      
    
      
        
        
      
        
        
      
        
        
      
    
  </ul>
</div>




    </div>
  
</template>

<script>
export default {
    name:'view',
    data(){
        return{
        id: this.$route.params.id, // 将 URL 地址中传递过来的 Id值，挂载到 data上，方便以后调用
      postinfo: {} 
        }
    },
 created(){
     this.getPostInfo()
 },
  methods: {
   getPostInfo(){
      this.$http.get("http://127.0.0.1:3334/posts/"+this.id).then(result => {
      this.postinfo = result.data
      window.console.log(result.data)
})
}
 }
}
</script>


<style>
.post-date {
    display: block;
    margin-top: 3px;
    margin-bottom: 1rem;
    color: #9a9a9a;
    font-family: 'Quattrocento Sans', sans-serif;
    font-size: 0.8rem;
}
body {
    font-family: "PT Serif", Georgia, "Times New Roman", serif;
    font-size: 18px;
    color: #515151;
    line-height: 1.75rem;
}
.post-container {
    margin-bottom: 4rem;
}
h1, h2, h3, h4, h5, h6 {
    font-family: "Quattrocento Sans", sans-serif;
    color: #333;
}
h1 {
    display: block;
    font-size: 2em;
    margin-block-start: 0.67em;
    margin-block-end: 0.67em;
    margin-inline-start: 0px;
    margin-inline-end: 0px;
    font-weight: bold;
}
h2 {
    display: block;
    font-size: 1.5em;
    margin-block-start: 0.83em;
    margin-block-end: 0.83em;
    margin-inline-start: 0px;
    margin-inline-end: 0px;
    font-weight: bold;
}
p {
    display: block;
    margin-block-start: 1em;
    margin-block-end: 1em;
    margin-inline-start: 0px;
    margin-inline-end: 0px;
}


</style>
