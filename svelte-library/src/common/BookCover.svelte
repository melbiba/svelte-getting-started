<script>
    export let book = {}

    function isValidUrl(url) {
        return url && /http.+\.(jpg|png|gif)$/.test(url);
    }
</script>

<a href="#" class="book book--interactive book--variation--{book.variation} {isValidUrl(book.cover) ? 'book--cover' : 'book--no--cover'}">
    <!-- isValidUrl will return true if the URL in question is true.
    The '?' will return the first arguement, argument before ':', if the question is true, 
    and will return the second argumnet if the question is false. -->
    <span class="cover" style={isValidUrl(book.cover) ? 'background-image: url' + book.cover + ')' : ''}>
        <!-- we will show the book's title and author on the cover.
        The {book.argument || ''} makes the page show nothing if there is no argument 
        value in the specified argumenet. If you want, you can place something in there.
        It is considered as the default value. -->
        <span class="title">{book.title || ''}</span>
        <span class="author">{book.author || ''}</span>
    </span>
</a>
