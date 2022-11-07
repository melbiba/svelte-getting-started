<script>
    import BookCover from '../common/BookCover.svelte';
    import Heart from './Heart.svelte';

    export let books = [];
</script>

<style></style>

<!-- looping through the books array we are getting from Library.svelte and putting the 
titles in an unorganized list -->
<ul>
    {#each books as book}
        <li>
            <!-- <BookCover book={book} />  is the same as -->
            <BookCover {book} /> 
            {#if book.favorite}
                <div class="heart">
                    <Heart />
                </div>
            {/if}

        </li>
    {/each}
</ul>
