<template lang='pug'>
v-app
  v-toolbar(hidden-sm-and-down id='base' dark flat)
    v-container(fluid fill-height text-xs-center)
      v-toolbar-title(id='title') {{title}}
    v-container(hidden-sm-and-down fill-height fluid wrap)
      v-spacer
      v-toolbar-item
        v-btn(id='btn' flat app large to='/') Home
      v-toolbar-item
        v-btn(id='btn' flat app large to='/about') About
      v-toolbar-item
        v-btn(id='btn' flat app large to='/info') Further info
      v-toolbar-item
        v-btn(id='btn' flat app large to='/contact') Contact
      v-toolbar-item
        v-btn(id='sign' app large href='' exact) Link to action
  v-container(hidden-md-and-up id='small' text-xs-center)
    span(v-for='(item, i) in pages') 
      router-link(:to='item.link') {{item.name}}
      br
    v-btn(id='sign' app large href='' exact) Link to action
  v-content(id='dark')
    router-view
  v-footer(id='foot' dark height='auto' class='text-xs-center')
    v-flex(lg3 xs12)
      img(src='./assets/DC.png')
    v-flex(lg3 xs12)
      img(src='./assets/OL.png')
    v-flex(lg3 xs12)
      img(src='./assets/NCL.png')
    v-flex(lg3 xs12)
      img(src='./assets/EPSRC.png')
</template>
 

<script>
export default {
  data() {
    return {
      // Change the name of the project
      title: "Name of project",
      pages: [
        { name: "Home", link: "/" },
        { name: "About", link: "/about" },
        { name: "Info", link: "/info" },
        { name: "Contact", link: "/contact" }
      ]
    };
  }
};
</script>
 