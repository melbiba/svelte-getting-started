<script>
    import BookGrid from './BookGrid.svelte'
    import Button from '../common/Button.svelte'

    const books = [
        {
            "id": 1,
            "title": "Moes Beggining",
            "author": "Moe's Father & Life",
            "cover": "",
            "about": "Moe gets 20 years older in a blink",
            "variation": "0"
        },
        {
            "id": 2,
            "title": "Moes Preparation",
            "author": "Life's Reality",
            "cover": "",
            "about": "Moe's journey to prepare for the bomb to go off",
            "variation": 1
        },
        {
            "id": 3,
            "title": "Living the Reality",
            "author": "Moe ElBiba",
            "cover": "",
            "about": "Moe handling everything in the best way possible",
            "variation": 3,
            "favorite": true
        }
    ]
</script>


<style>
header{
    margin: var(--spacingMedium) 0 var(--spacingLarge) 0;
}
h1{
    font-size: var(--typeSizeXXLarge);
    font-weight: var(--typeWeightBold);
    line-height: var(--typeLineHeightTight);
}
.preamble{
    display: block;
}
.greeting{
    font-size: var(--typeSizeSmall);
}
</style>


<header>
    <span class="preamble">Welcome to the</span>
    <h1>Library</h1>
</header>

<p class="greeting">
    This is a lib for the peeps. Welcome. Read the books here. Be inspired.
    Go home, and share them with your homies.
</p>

<Button> + Add Book</Button>
<!-- adding the BookGrid component and calling the books component ({books}) 'books' by (books={books}) -->
<!-- It is called from another file component in the same dirctory -->
<!-- the directory itself will have an html mark up. So, we are importing the prop -->
<!-- creted in the component we are creating and it is all coming as if we are importing -->
<!-- a function from a module where everything well be handled there. -->
<BookGrid books={books} />