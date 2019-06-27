 <template>
    <div class="container"> 
 <header class="masthead">
  <h3 class="masthead-title">
       <router-link to="/"><a>Llovky   </a></router-link>
    
    <small class="masthead-subtitle">a minimalist Jekyll theme</small>
    <div class="menu">
  <nav class="menu-content">
    
      <router-link to="/about"><a>About</a></router-link>
      <router-link to="/about"><a>Writing</a></router-link>
      <router-link to="/contact"><a>Contact</a></router-link>
      
  </nav>
  <nav class="social-icons">
    
  
  
    <a href="https://github.com/Laiflow" target="_blank"><i class="fa fa-github" aria-hidden="true"></i></a>
  

  
  
    <a href="https://weibo.com/simple" target="_blank"><i class="fa fa-twitter" aria-hidden="true"></i></a>
  

  
  
    <a href="http://www.linkedin.com/in/" target="_blank"><i class="fa fa-linkedin" aria-hidden="true"></i></a>
  

  
  
    <a href="trainbigger2@163.com" target="_blank"><i class="fa fa-envelope" aria-hidden="true"></i></a>
  

  
  
    <a href="/Lagrange/feed.xml"><i class="fa fa-rss-square" aria-hidden="true"></i></a>
  

  </nav>
</div>

  </h3>
</header>


    </div>
 </template>



<script>
export default {
  name: 'Head',
  
}
</script>

<style>
.masthead {
  padding-top: 0.5rem;
  padding-bottom: 0.5rem;
  margin-bottom: 4rem;
  font-family: "Quattrocento Sans", sans-serif;
}

.masthead a:hover {
  color:black;
}

.masthead-title a {
  font-size: 2rem;
  text-decoration: none;
  color: #505050;
}

.masthead-subtitle {
  color: #999;
}

.menu {
    padding-top: 0.5rem;
    display: block;
}
.h3 {
    display: block;
    font-size: 1.17em;
    margin-block-start: 1em;
    margin-block-end: 1em;
    margin-inline-start: 0px;
    margin-inline-end: 0px;
    font-weight: bold;
}

.container {
  margin-left: auto;
  margin-right: auto;
  width: 615px;
}
.menu {
    padding-top: 0.5rem;
    display: block;
}
.menu-content a {
    color: #999;
    font-size: 1rem;
    padding-right: 10px;
}
h3 {
    font-size: 1.17em;
    font-weight: bold;
}
h3 {
    display: block;
    font-size: 1.17em;
    margin-block-start: 1em;
    margin-block-end: 1em;
    margin-inline-start: 0px;
    margin-inline-end: 0px;
    font-weight: bold;
}
</style>
