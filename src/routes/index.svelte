
    
<script>
    // export let guides;
  
   /*
   https://netninja.dev/courses/sveltekit-tutorial/lectures/36982375
   */
</script>
<div class="foo">
    <h1>index.svelte</h1>
    <a href="/">/</a><br>
    <a href="/guides">/guides</a><br>
    <a href="/guides/hello">/guides/hello</a><br>
    <a href="/about">/about</a>
</div>





<style>
    .guides {
        text-align: center;
        display: block;
        margin: 20px auto;
    }
    h1, a {
        font-size: 2rem;
        color:bisque;
    }
    .foo > a, h1 {
    background-color: bisque;
    color:#1f1f1f
  }
   
</style>
