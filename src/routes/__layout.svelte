<script>
    import Title from '$lib/title.svelte'
    import '../styles/global.css'
</script>

<header>
    <Title title="Ninja Gaming Guides" />
</header>

<div class="foo">
    <h1>/guides/__layout.svelte</h1><br>
    <a href="/">/home</a><br>
    <a href="/guides">/guides</a><br>
    <a href="/guides/hello">/guides/hello</a><br>
    <a href="/about">/about</a><br>
    <a href="/guides/hello">/guides/hello</a><br>
  </div>

<div style="color:#fff;">page: __layout.svelte</div>
<main>
    <slot></slot>
</main>
<footer>
    <p>Copyright 2022 Ninja Gaming Guides</p>
</footer>

<style>
    header {
        display: flex;
        justify-content: center;
    }
    main {
        max-width: 960px;
        margin: 20px auto;
    }
    footer {
        text-align: center;
    }
</style>