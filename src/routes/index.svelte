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
            error: new Error('Could not fetch the guides.')
        }
    }
</script>
    
<script>
    export let guides;
   /*
   https://netninja.dev/courses/sveltekit-tutorial/lectures/36982375
   */
</script>


<div class="guides">
    {#each guides as guide}
    <li>
        <a href="/">{guide.title}</a>
    </li>
    {/each}

</div>

<style>
    .guides {
        text-align: center;
        display: block;
        margin: 20px auto;
    }
</style>
