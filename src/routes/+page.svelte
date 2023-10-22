<script>
    import { goto, beforeNavigate, afterNavigate } from "$app/navigation";

    const handleClick = () => {
        console.log("Placing your order");
        goto("/products");
    }

    beforeNavigate((navigation) => {
        console.log({before: navigation});
    });

    afterNavigate(() => {
        console.log({after: navigation});
    });

</script>

<h1>Welcome home!</h1>

<a href="/blog">Blog</a>
<a href="/products">Products</a>

<button on:click={handleClick}>Place Order</button>