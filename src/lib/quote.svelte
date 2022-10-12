<script lang='ts'>

interface quoteJSON{
    qotd_date: string;
    quote: {
        id:string;
        dialogue: boolean;
        private:boolean;
        tags: string;
        url: string;
        favorites_count:number;
        upvotes_count:number;
        downvotes_count:number;
        author: string;
        author_permalink:string;
        body:string;
        }
}
let fact: HTMLParagraphElement;
let author_of_quote: HTMLParagraphElement;

async function handleClick() {
    fact.textContent = 'Loading...';
    const number = await fetchSomeNumber();
    handleNumber(number);
}
async function fetchSomeNumber() {
    return fetch('https://favqs.com/api/qotd')
    .then((response) => response.json());
}

function handleNumber(qotd: quoteJSON) {
    fact.textContent = qotd.quote.body; 
    author_of_quote.textContent = qotd.quote.author;
}
</script>

<div class="random_number">
    <button on:click={handleClick}>Get my motto to this day.</button>
    <p bind:this={fact}>
    </p>
    <p bind:this={author_of_quote}>
    </p>
</div>