<template>
  <navbar 
    :pages="pages"
    :active-page="activePage"
    :nav-link-click="(index) => activePage = index"
  ></navbar>

  <page-viewer
    :page="pages[activePage]"
  ></page-viewer>
</template>

<script>
import PageViewer from './components/PageViewer.vue';
import Navbar from './components/Navbar.vue';

export default{
  components:{
    PageViewer,
    Navbar
  },
  data(){
    return {
      activePage: 0,
      pages:[
        {
          link: {text: 'Home', url: 'index.html'},
          pageTitle: 'Home Page',
          content: 'This is the home page content.'
        },
        {
          link: {text: 'About', url: 'index.html'},
          pageTitle: 'About Page',
          content: 'This is the about page content.'
        },
        {
          link: {text: 'Contact', url: 'index.html'},
          pageTitle: 'Contact Page',
          content: 'This is the contact page content.'
        },
      ]
    }
  }
}
</script>

