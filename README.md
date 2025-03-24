# CeneoScraper

## Algorithm for extracting opinions about a single product from ceneo.pl
1. Send a request for accesing first webpage with opinions about a product.
2. If response is ok, parse HTML page content into DOM structure.
3. Extract opinions and their components from DOM structure 
4. Assign opinions with their components to a complex data structures.
5. If there are more pages with opinions, repeat steps 1-5 for them.
6. Save data structures with opinions into database.

## Structure of single opinion in Ceneno.pl
|Component|Variable|Selector|
|---------|--------|--------|
|opinion|opinion|div.user-post_body|
|opinion ID|opinion_id||
|opinion’s author|author|span.user-post__author-name|
|author’s recommendation|recommend||
|score expressed in number of stars|stars||
|opinion’s content|content|div.user-post__text|
|list of product advantages|pros||
|list of product disadvantages|cons||
|how many users think that opinion was helpful|upvotes||
|how many users think that opinion was unhelpful|downvotes||
|publishing date|published||
|purchase date|purchased||