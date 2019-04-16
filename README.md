MY WEBSITE

1. I created a website containing 4 HTML sites: index.html, jazz.html, blues.html and classical.html.
    Every website reachable from each site.

2. Every of the HTML pages contains one picture. Page index.html contains a table, pages jazz.html and blues.html contain ordered lists.

3. The website has two styling sheet files: Style.css and variables.scss (compiled variables.css).

4. With the stylesheets I used the following CSS selectors (containing a .class and #ID selector):
    h1, h2 - multiple element selector
    .flexcontainer > div  - child selector
    img[src*="jpg"] - attribute selector
    .btn:hover - pseudoclass selector
    #indexhd::before - pseudoelement selector

    With the stylesheets I used the following CSS properties:
    text-align: center;
    background: rgba(238, 226, 187, 0.9);
    padding: 15px 20px;
    font-size: 20px;
    margin: 15px;
    cursor: pointer;
    width: 20%;
    transition: 0.8s;
    text-decoration: none;
    border-radius: 0;
    .....and many more.

5. The styling sheets contain a mobile-responsive @media query where the welcoming message changes, the background changes from a picture background to a white background if the screen-size is smaller than 700px:

    @media (max-width: 699px){
      #indexhd::before{
        content: "Welcome!!!!"
          }
      .indexbody{
        background-color: white;
      }

      @media (min-width:700px){
        #indexhd::before{
          content: "Welcome to my page! Discover my taste in music!!!"
        }
        .indexbody{
          background: URL(https://4.imimg.com/data4/UP/HW/MY-22869148/vinyl-wallpaper-500x500.jpg);
          background-repeat: no-repeat;
          background-size: 100%;
        }

6. Using Bootstrap component for Paragraphs

      div class="alert alert-success" role="alert">
        <h2>Short Biography</h2>
        <p id="par1">...</p>
        <hr>
        <p id="par2" class="mb-0">...</p>
        <hr>
        <p id="par3" class="mb-0">...</p>

   Using Bootsrap flexbox:

    <div class="container flexcontainer">

   Using Bootstrap columns:

     <div class= "container my-container">
       <div class="row my-row">
         <div class="col-3 my-col">
           Favourite Artist
         </div>
         <div class "col-4 my-col">
           Years active
         </div>
       </div>

7. Using SCSS:

      /*Variable*/
      $color:olive;

      /*Nesting*/
      #orderedlist {
        font-size: 20px;

        ol{
        color:$color;
        font-weight: bold;
        margin-left: 40%;
        }
      }

      /*Inheritance*/
      .message1{
        font-size: 20px;
        font-weight: bold;
        text-align: center;
      }

      .message2{
        @extend .message1;
        background-color: lighten($color,75%);
      }


index.html contains: buttons used for navigation through the pages, a header that changes to a smaller header while resizing the screen, a table, bootstrap columns, a       picture background that changes to white background when resizing the screen

jazz.html, blues.html and classical.html contain: buttons, headers, pictures, paragraphs formated using bootstrap, ordered lists, flexbox

style.css contains: different CSS selectors and properties as already described at the begining of the README file.

variables.scss contains: variables, nesting and inheritance definitions. A mapping to a variables.css file was created through CMD also WATCHING was turned on to update the variables.css file after saving.


YouTube upload: https://youtu.be/svOmGSf98Dc
