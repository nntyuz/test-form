<template lang="pug">
.main
  Header
  Hero
  FormComponent
  </template>
  
  <script>
  import Header from '@/components/header'
  import Hero from "@/components/hero";
  import FormComponent from "@/components/form";
  
  export default {
    name: "App",
    components: {
      Header,
      Hero,
      FormComponent,
    },
  };
  </script>
  
  <style lang="scss" scoped></style>