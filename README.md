# giflib
project based on spring basics course on teamtreehouse.com by Chris Ramacciotti
https://teamtreehouse.com/library/spring-basics

### next steps to add some features
#### 1 - Implementing the Favorites Page
At this point, creating a page to display all GIFs marked as favorites is well within your reach. Consider adding a method to GifRepository that would allow a controller to fetch all favorites.

Then, you need to add a controller method that intercepts the URI of your choice (e.g. /favorites), grab the list of Gif objects from your new repository method, and add it to the ModelMap.

Finally, return the name of a view that iterates over your list of Gifs, and you're rockin' and rollin'!

#### 2 - Implementing the Search Page
Creating a page for displaying search results involves the same steps as above. First, you must have a method in GifRepository that can return all Gif objects whose name field contains a specified String. (don't forget to account for case-sensitivity here).

Then, you must have a controller method that intercepts the URI specified by the search form's action attribute. This method must have a parameter annotated with @RequestParam that is named the same as the name attribute of the text input in the search form. This is similar to our use of @PathVariable, except that the search term will appear in the URI's query string, for example /search?q=compiler. In this method, you'll also call the repository method you created for searching a Gif object's name field.

Finally, in a similar fashion as you did with the Favorites page, return the name of a Thymeleaf view you've coded to iterate over the list of Gif objects in the ModelMap.
