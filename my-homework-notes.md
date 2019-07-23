# GifTastic

### Overview

In this assignment, you'll use the GIPHY API to make a dynamic web page that populates with gifs of your choice. To finish this task, you must call the GIPHY API and use JavaScript and jQuery to change the HTML of your site.

### Before You Begin

1. **Hit the GIPHY API**.
   * Fool around with the GIPHY API. [Giphy API](https://developers.giphy.com/docs/).
   * Be sure to read about these GIPHY parameters (hint, hint):
     * `q`
     * `limit`
     My Notes on GIPHT Parameters:
     References:
     https://www.npmjs.com/package/giphy-api
     https://developers.giphy.com/docs/ 
     https://developers.giphy.com/docs/api/endpoint/#search

      q - search query term or phrase
      limit - (optional) number of results to return, maximum 100. Default 25.
      offset - (optional) results offset, defaults to 0.
      rating - limit results to those rated (y,g, pg, pg-13 or r).
      fmt - (optional) return results in html or json format (useful for viewing responses as GIFs to debug/test)

     // Search with options using callback
      giphy.search({
      q: 'pokemon',
      rating: 'g'
    }, function (err, res) {
    // Res contains gif data!
  });

   * Like many APIs, GIPHY requires developers to use a key to access their API data. To use the GIPHY API, you'll need a GIPHY account (don't worry, it's free!) and then obtain an API Key by [creating an app](https://developers.giphy.com/dashboard/?create=true).
   * Make sure you switch the protocol in the query URL from **`http to https`**, or the app may not work properly when deployed to Github Pages.

   // ar xhr = $.get("http://api.giphy.com/v1/gifs/search?q=ryan+gosling&api_key=YOUR_API_KEY&limit=5");
    xhr.done(function(data) { console.log("success got data", data); });

    Movie To Search: "The Tuskegee Airmen", "Red Tails", "Red Tails Reborn"

    MY API KEY:
    GIPHY Developer
    https://developers.giphy.com/dashboard/
    my1stApp
    Api Key: wPDa4EjfIpXM8MhwGbu93SBi1y7XPUhV
    my1stApp URL - https://api.giphy.com/v1/gifs/search?q=ryan+gosling&api_key=wPDa4EjfIpXM8MhwGbu93SBi1y7XPUhV&limit=5

### Commits

Having an active and healthy commit history on GitHub is important for your future job search. It is also extremely important for making sure your work is saved in your repository. If something breaks, committing often ensures you are able to go back to a working version of your code.

* Committing often is a signal to employers that you are actively working on your code and learning.

  * We use the mantra “commit early and often.”  This means that when you write code that works, add it and commit it!

  * Numerous commits allow you to see how your app is progressing and give you a point to revert to if anything goes wrong.

* Be clear and descriptive in your commit messaging.

  * When writing a commit message, avoid vague messages like "fixed." Be descriptive so that you and anyone else looking at your repository knows what happened with each commit.

* We would like you to have well over 200 commits by graduation, so commit early and often!

### Submission on BCS

* Please submit both the deployed Github.io link to your homework AND the link to the Github Repository!

### Instructions

1. Create a search form with a JQuery click handler that calls an AJAX function. The QueryURL should include your API key and the user's search term. Be sure to use https:// so the page will work on GitHub.
   * Hint: this code will look similar to your solution for Activity #26 (Movie DB Form example).

   /* var queryURL = "https://api.giphy.com/v1/gifs/search?q=ryan+gosling&api_key=wPDa4EjfIpXM8MhwGbu93SBi1y7XPUhV&limit=5" */

   /* From line 35: 
      <button id="search">Add Film</button>
      $("#search").click(function(){
      From line 36: Seach for Film 
      <input id="film-name">
      $("#film-name").val("movie"); */

2. Your app should take the image_original_url property from the first image in the JSON response and display the image in the HTML
   * Hint: you can use the HTML and JQuery code written for the poster image in Activity #21 (Movie DB JQuery example).

/* // AJAX call to OBMD API with promise and callback handler
    $.ajax({
      url: queryURL,
      method: "GET"
    }).then(function(response) {

      // Add movie name
      $("#movie-name").html(response.Title);

      // Add description
      $("#movie-description").html(response.Plot);
      
      // Create an image elment, add src attribute, and append to figure
      var posterImage = $("<img>");
      posterImage.attr("src", response.Poster);
      $("#movie-poster").append(posterImage);

    }); */

3. Change your JQuery code to loop through the JSON response and display 4 animated gif images instead of just 1.

4. Deploy your assignment to Github Pages.

5. **Rejoice**! You just made something really cool.

- - -

### Minimum Requirements

Attempt to complete homework assignment as described in instructions. If unable to complete certain portions, please pseudocode these portions to describe what remains to be completed. Adding a README.md as well as adding this homework to your portfolio are required as well and more information can be found below.

- - -

### Bonus Goals

1. Create an alt attribute for each gif.

2. When the user clicks one of the still GIPHY images, the gif should stop playing. If the user clicks the gif again, it should start animating.

3. Use local storage to remember the user's search term, and display those images again when the user returns to the page.

4. Use bootstrap to make fully mobile responsive layout. Add custom CSS for typography and colors.

### Reminder: Submission on BCS

* Please submit both the deployed Github.io link to your homework AND the link to the Github Repository!

- - -

### Create a README.md

Add a `README.md` to your repository describing the project. Here are some resources for creating your `README.md`. Here are some resources to help you along the way:

* [About READMEs](https://help.github.com/articles/about-readmes/)

* [Mastering Markdown](https://guides.github.com/features/mastering-markdown/)

- - -

### Add To Your Portfolio

After completing the homework please add the piece to your portfolio. Make sure to add a link to your updated portfolio in the comments section of your homework so the TAs can easily ensure you completed this step when they are grading the assignment. To receive an 'A' on any assignment, you must link to it from your portfolio.

- - -

### One More Thing

If you have any questions about this project or the material we have covered, please post them in the community channels in slack so that your fellow developers can help you! If you're still having trouble, you can come to office hours for assistance from your instructor and TAs.

**Good Luck!**
