<template>
    <div class="container">
        <div class="row">
            <div class="col-xs-12">
               <app-quote>
                   <h1 slot="title">{{title}}</h1>
                   <p>Description</p>
               </app-quote>
            </div>


            <button @click="selectedComponent = 'Author'">Author</button>
            <button @click="selectedComponent = 'New'">New</button>
            <!--
                destroy component when not use keep-alive
           -->
            <component :is="selectedComponent"></component>

            <!--
                not destroy component when use keep-alive
            -->
            <keep-alive>
                <component :is="selectedComponent"></component>
            </keep-alive>
        </div>
    </div>
</template>

<script>
    import Quote from './Components/Quote.vue'
    import New from './Components/New.vue'
    import Author from './Components/Author.vue'

    export default {
      data: function() {
        return {
          title : 'Heading 1',
          selectedComponent: 'Author'
        }
      },
      components: {
        'appQuote': Quote,
        Author,
        New
      }
    }
</script>

<style>
</style>
