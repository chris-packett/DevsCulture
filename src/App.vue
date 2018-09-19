<template>
  <div class="wrapper">

    <!-- Sidebar -->
    <nav id="sidebar">
        <div class="sidebar-header">
            <img src="./assets/logo.png" class="logo"> 
        </div>

        <ul class="list-unstyled components">
            <li>
                <a href="#">Home</a>
            </li>
            <li>
                <a href="#">About</a>
            </li>
            <li>
                <a href="#">Pages</a>
            </li>
            <li>
                <a href="#pageSubmenu" data-toggle="collapse" aria-expanded="false" class="dropdown-toggle">Categories</a>
                <ul class="collapse list-unstyled" id="pageSubmenu">
                    <li>
                        <a href="#">Programming Languages</a>
                    </li>
                    <li>
                        <a href="#">Front-End Techs</a>
                    </li>
                    <li>
                        <a href="#">Back-End Techs</a>
                    </li>
                    <li>
                        <a href="#">Books</a>
                    </li>
                    <li>
                        <a href="#">Design</a>
                    </li>
                    <li>
                        <a href="#">Browsers</a>
                    </li>
                    <li>
                        <a href="#">Hosting</a>
                    </li>
                    <li>
                        <a href="#">Schools</a>
                    </li>
                    <li>
                        <a href="#">News</a>
                    </li>
                    <li>
                        <a href="#">Podcasts</a>
                    </li>
                    <li>
                        <a href="#">Collaboration</a>
                    </li>
                    <li>
                        <a href="#">Meetups</a>
                    </li>
                </ul>
            </li>
            <li>
                <a href="#">Blogs</a>
            </li>
            <li>
                <a href="#">Contact Us</a>
            </li>
            <li>
                <a href="#">Sponsors</a>
            </li>
        </ul>
    </nav>

    <div>
      <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <div class="container-fluid">
          <button type="button" id="sidebarCollapse" class="btn btn-info">
            <i class="fas fa-align-left"></i>
            <span></span>
          </button>
        </div>
      </nav>
    </div>

    <!-- Page Content -->
    <!-- <div id="content">
      <div class="tiler">
        <img src="https://picsum.photos/1000/600?image=1067" />
      </div>

      <div class="tiler">
        <img src="https://picsum.photos/1000/600?image=1061" />
      </div>

      <div class="tiler">
        <img src="https://picsum.photos/1000/600?image=1057" />
      </div>

      <div class="tiler">
        <img src="https://picsum.photos/1000/600?image=1052" />
      </div>

      <div class="tiler">
        <img src="https://picsum.photos/1000/600?image=1043" />
      </div>

      <div class="tiler">
        <img src="https://picsum.photos/1000/600?image=1055" />
      </div>

      <div class="tiler">
        <img src="https://picsum.photos/1000/600?image=1036" />
      </div>

      <div class="tiler">
        <img src="https://picsum.photos/1000/600?image=1037" />
      </div>

      <div class="tiler">
        <img src="https://picsum.photos/1000/600?image=1039" />
      </div>
    </div> -->

</div>       
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "app",
  components: {
    HelloWorld
  }
};

$(document).ready(function () {
    $('#sidebarCollapse').on('click', function () {
        $('#sidebar').toggleClass('active');
        $(this).toggleClass('active');
    });
});

</script>

<style>

@import "https://fonts.googleapis.com/css?family=Poppins:300,400,500,600,700";

body {
    font-family: 'Poppins', sans-serif;
    background: #fafafa;
}

#content {
    display: flex;
    flex-wrap: wrap;
}

.logo {
  width: 12em;
  height: auto;
}

.tiler {
  display: inline-block;
  cursor: pointer;
  visibility: hidden;
  width: 32%;
  margin: auto;
}

.tiler img { 
  display: block;  
  margin: auto; 
  max-width: 100%;
  visibility: visible;
}

a, a:hover, a:focus {
    color: inherit;
    text-decoration: none;
    transition: all 0.3s;
}

.wrapper {
    display: flex;
    align-items: stretch;
    perspective: 1500px; 
}

#sidebar {
    min-width: 250px;
    max-width: 250px;
    min-height: 100vh;
    background: #1D1E19;
    color: #fff;
    transition: all 0.3s cubic-bezier(0.945, 0.020, 0.270, 0.665);
    transform-origin: center left;
}

#sidebar.active {
    margin-left: -250px;
    transform: rotateY(100deg);
}

#sidebar .sidebar-header {
    padding: 20px;
    background: #1D1E19;
}

#sidebar ul.components {
    padding: 20px 0;
}

#sidebar ul p {
    color: #fff;
    padding: 10px;
}

#sidebar ul li a {
    padding: 10px;
    font-size: 1.1em;
    display: block;
}
#sidebar ul li a:hover {
    color: #7386D5;
    background: #fff;
}

#sidebar ul li.active > a, a[aria-expanded="true"] {
    color: #fff;
    background: #49C7D0;
}
ul ul a {
    font-size: 0.9em !important;
    padding-left: 30px !important;
    background: #49C7D0;
}

a[data-toggle="collapse"] {
    position: relative;
}

.dropdown-toggle::after {
    display: block;
    position: absolute;
    top: 50%;
    right: 20px;
    transform: translateY(-50%);
}

.btn-info {
    color: #fff;
    margin: 10px 10px 10px 0px;
    background-color: #49C7D0;
    border-color: #49C7D0;
}

@media (max-width: 768px) {
    
    #sidebar {
        margin-left: -250px;
        transform: rotateY(100deg);
    }

    #sidebar.active {
        margin-left: 0;
        transform: none;
    }
}

</style>
