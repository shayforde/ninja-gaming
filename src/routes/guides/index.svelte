<script context="module">
  export async function load({ fetch }){
      const res = await fetch('https://jsonplaceholder.typicode.com/posts')
      const guides = await res.json();

      if (res.ok){
          return {
              props: {
                  guides
              }
          }
      }

      return {
          status: res.status,
          error: new Error('Could not fetch Shays guides.')
      }
  }
</script>

<script>
  export let guides;
</script>

<div class="foo">
  <h1>/guides/index.svelte</h1>
  <a href="/">/</a><br>
  <a href="/guides">/guides</a><br>
  <a href="/guides/hello">/guides/hello</a><br>
  <a href="/about">/about</a>
</div>

<div class="guides">
  {#each guides as guide}
  <li>
      <a href="/">{guide.title}</a>
  </li>
  {/each}

</div>


<div style="color:#fff;">page: guides/index.svelte</div>
<a href="/">home</a>
<div class="index">
  <h2>Welcome</h2>
  <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Sunt laborum magnam deleniti recusandae, quis aperiam, architecto neque, voluptatem dicta expedita aut id voluptate omnis consectetur dolore! Quo quae perferendis vel dignissimos quasi illum aperiam dolores, id, laudantium voluptatibus fugiat accusantium impedit velit modi ratione iure qui culpa! Repellendus cupiditate aliquid quam magni. Laudantium, laboriosam quibusdam. Provident, quae incidunt! Aspernatur, vel?</p>
  <a href="/guides">View Guides</a>
  <a href="/about">About</a>
</div>

<style>
  .index {
    text-align: center;
    display: block;
    margin: 20px auto;
  }
  .foo {
    text-align: center;
    background-color: bisque;
    color:#1f1f1f
  }
  .foo > a , h1{
    text-align: center;
    background-color: bisque;
    color:#1f1f1f
  }
</style>