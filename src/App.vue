<template>
  <div class="wrapper">

    <!-- Sidebar -->
    <nav id="sidebar">
        <div class="sidebar-header">
            <h3>DevsCulture Sidebar</h3>
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

    <!-- Page Content -->
    <div id="content">
        <!-- We'll fill this with dummy content -->
    </div>

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

</script>

<style>




</style>
