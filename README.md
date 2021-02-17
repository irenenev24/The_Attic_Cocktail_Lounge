# **The Attic, cocktail lounge and restaurant.**

This is a website to promote a new cocktail bar and restaurant located in Manchester, England.
I want to use this website to build brand awareness and increase social media presence and reviews.
Provide a good user experience for new and returning users with an easy to navigate site and a clear, easy to use booking/contact form.


## UX

## Who is this website for?

* This website is for people who want information on "The Attic" lounge and restaurant.
* This webiste is for people looking to book a venue for private events.
* This website is for people based in England, preferably close to Manchester.
* It is aimed at people aged 18+ with disposable income.

### What do visitors want?

* Clear information on how to book the venue for events.
* Information on opening hours, location, menus and pricing.
* Information on function capacity.
* Easy to find booking/contact form.
* A trustworthy, easy to navigate site that gives clear information about the  
  bar.
* Multiple ways to contact the bar including links to social media pages.


### Business Goals:

1. Build brand awareness.
1. Showcase menu items and function room.
1. Provide potential clients with information about the bar, restaurant and function room.
1. Promote social media pages.

### Customer Goals:

#### First time customer

1. Is this site trusthworthy and easy to navigate?
1. Is the purpose of this site clear?
1. Do I understand the information provided about the business?
1. Are there any reviews about this business?
1. How can I contact them to make a booking or ask for more information?
1. Can I view an online menu or download a menu?

#### Repeat customers

1. Can I easily make a booking?
1. Can I leave an online review?
1. Can I view an online menu or download a menu?
1. Can I follow this business on social media?

### Strategy

* An easy to navigate website to promote the business and its social media accounts.
* Build brand awareness and repeat clientele.

### Scope

* How to contact the bar for further information.
* How to book the bar for functions.
* What the bar offers eg: Cocktail menu, Restaurant menu.
* A gallery to show pictures of the items on offer here.
* A review section.
* An about section to give a brief history of the business.

### Structure

* A minimalist site with clear sections or pages for menus, reviews, pictures and social links.
* Good flow across pages so user knows what to expect and how to find information.
* An easy to find and use contact form.
* Menus - both downloadable and opening on a seperate tab.

### Skeleton

* Sticky nav across all pages (home, menu, gallery, function and contact us).
* Hero image with company logo on home page, heading on other pages with page details. E.g: Menu/contact page.
* Menus that can be downloaded.
* Gallery slideshow.
* Review section.
* Contact page with email address, address, phone number.
* Section with address, opening hours, e-mail and telephone number.
* Footer with social media links, legal info.

### Surface

* Colors used:
 - #36454f charcoal,
 - #ffffec cream,
 - #fafafa off-white,
 - rgb(193, 238, 253) lightblue,
 - rgb(0, 204, 255) blue,
 - red 
* Fonts used:
 - "Courgette", cursive
 - "Roboto Slab", serif
* Images:
 - All from Unsplash.com

## Features 

### Home
* A home page with a hero image and company logo in the nav bar.
* About us section with details of opening hours, address, e-mail address and phone number.
* A review section featuring customers reviews and images.

### Menu page
* Menus 
  - one cocktail menu.
  - one restaurant menu.

### Contact page
* Contact page with an easy to fill out from requiring full name, email address and an
 input box with a placeholder of "Please provide booking details..."


### Gallery
* Mix of images featuing food and drink from the menu.

  
 ## Features left to implement

In the future I would like to build on to this site by adding:
  - An online booking system.
  - An upcoming events page.
  - A shop page to sell pre-made cocktails online.
  - Cocktail Tutorials.


## Technologies used:
* HTML5
* CSS3 
* Bootstrap 4
* Font Awesome
* Google Fonts
* Microsoft Word (Templates) for my menus.

### Testing

* W3Schools HTML/CSS validator. 
  - Picked up a few small errors eg: extra > and unclosed CSS tags in two areas.
    Fixed these issues and ran again. This returned a "Congratulations, no error found" message.
    ![w3schools-css-validator]("assets/images/screenshotw3s.png").

* Tested across multiple device sizes.
  - Found on smaller screen sizes (e.g: Galaxy Fold, iPhone 5,SE) the hero image and hero text were too large, 
    off center or at times took over the screen view. Also the reviewer images were distorted when skrunk down.
    After speaking with my mentor Brian Macharia, he suggested that maybe my image size was unsuitable for what 
    I was trying to do and how if I changed the size of my downloaded image it might suit better.
    I also added media queries at (max-300) and (max-400) to control the size of the text as the screen shrinks.

    - @media screen and (max-width: 400px) {       |       @media screen and (max-width: 300px) {
      .hero-text-h1 {                              |         .hero-text-h1{
          font-size: 3.4rem;                       |             font-size: 3rem;
          margin: 0;                               |              margin: 0;
        }                                          |           }
      }                                            |          }


  - Changing the image size also helped with the performance section in DevTool Lighthouse. My performance was 58 becasue my images 
    were too large. This is now 78 for the home page. 
    
* Also during testing I discovered that I needed to insert @media queries for my form and menu pages as they were not 
   responding correctly on small devices.
  - Form: 
     @media screen and (max-width: 800px) {
        input[type=text], input[type=email], select, textarea {
            width: 100%;
            margin-top: 0;
        }
        legend {
            font-size: 1.5rem;
        }
   }
  - Menu:
    @media screen and (max-width: 1200px) {
        .column {
            width: 100%;
        }
    }
    
* While doing a last test I noticed that my images on the small screen were too large to fit and so were sending my
   nav bar toggler icon to the left. About multiple attemps to resize the pics, which didnt work, I searched online and found an article 
   which suggested using flexbox to create a responsive gallery. This required rewriting the gallery code and adding media queries
   at two different screen sizes, (min-600px) and (min-1000px).
    
  -     @media screen and (min-width: 600px) {     |       @media screen and (min-width: 1000px) {
      .grid {                                      |         .cell {
          display: flex;                           |                width: 33%;
          flex-wrap: wrap;                         |                background-color: black;
          flex-direction: row;                     |                }
      }                                            |              }
      .cell {                                      |
          width: 50%;                              |
          background-color: black;                 |
            }                                      |
      }                                            |
   
   This causes the gallery to appear stacked in one single row on a phone screen,
   stacked in two rows on a tablet screen and as a grid of three rows on a desktop screen. 
   This also helped with the performance section of  DevTool Lighthouse which was at 68 but is now at 76.

* I also recieved feed-back about the font selection from friends who felt the font I had originally selected
   did not suit the site, so I changed it to "Courgette", cursive, "Roboto Slan", serif.

* While using DevTools Lighthouse it suggested I put description tags in the mate section. Also included are tag
  words which help with searches and accessibility.

### User stories

* Customer Goals
 - Clear purpose.
 - Trustworthy.
 - Provides clear information for booking and contacting via the contact page and function page.
 - Clear information about address, email, phone number in the footer section..
 - Clear opening hours details on the footer section..
 - Clear reviews located on the home page.
 - Clear social media links in the footer area..
 - Clear menus and a download version of each menu opening onto a new tab so user can still see original page.
 - Clear menu pricing.
 - Clear about function details and capacity, descrided in the function page.
* Business Goals 
 - Builds brand awareness by highlighting what the company does.
 - Promotes social media presence with social links which, if a real company, would link to the relevant social media pages.
 - Showcases menus and function room.
 - Clear business details.
* Repeat Customer Goals
 - Can easily book and contact, via contact form.
 - Can leave online review/follow on social media.
 - Option to view or download menus for ease of access.

 After viewing the site with each of these goals in mind, I feel happy that the goals have been fulfilled and that users,
 both new and repeat will be able to use this site effectively.
 I also feel from a business point of view that the website effectively promotes and presents "The Attic" to the public,
 helping to create a positive awareness of "The Attic" brand.

 ### Manual Testing Links
 
 - I manually tested each link in the nav bar to make sure that they all individually worked and took me where I expected to go.
 - I also manually checked the links to the social media pages to make sure that they also took me to the intended social media pages.
 - I manually checked that both of my menus opened up onto seperate pages when the "Download PDF" links are clicked.
 - I also checked that my form cannot be sent without a name, email address or text provided in the text area.
 - In the footer area I have an email link. When tested I found it wasnt working as I had only written it in.
   I corrected this by making it in to a link and when tested again found it to work. **As this is not a real email address, 
   I have set it to go to the contact page**.
 - I also found when hovered over the link was hard to see as the text was too dark so I changed it to match the light cream background seen  
   throughout the site.
## Tested on
- Windows 10
- Microsoft Edge
- Apple Macbook Project
- Samsung Galaxy Tab A 8.0
- Various devices screens available on DevTools

### Deployment 

## Deploy from GitHub
 - Sign into GitHub and access your repositories.
 - Select desired repository.
 - Once clicked on, this bring you to a code and deploy page which contains details of your READme.md, a description of the 
   repository details and other info.
 - Located near the top, under the repository name is a tool bar. At the end of this bar is a settings selector.
 - Click on settings and scrool down to GitHub Pages. Here you will click on the dropdown menu under source. (Currently showing "None"),
   click on this and select "Master", click save. Page will automatically refresh. Once refreshed, scroll down to find the link to your 
   website high-lighted in green.
 - Click on this or copy and paste into browser to access your site.

 ## Run project locally
 - If you have a GitHub account you will need to log in. If not you will need to sign up at https://www.GitHub.com/ to access this file.
 - To run project, go to the repository for that project and click on it.
 - Click the Green button to start the repositroy. This should only be clicked once as each time it is clicked it opens a new 
   copy of the GitHub workspace.
 - The workspace is now open to be viewed and edited locally.
 - 

## To clone repository so it can be used in different editors effectively
 - To clone select desired repository.
 - Once clicked on, this bring you to a code and deploy page which contains details of your READme.md, a description of the 
   repository details and other info.
 - Located beside the green gitpod button is a button with "Code" written on it. Here you will find a drop-down menu,
   that when selected gives you the option to clone or download the repository file.


### Credits

## Code used
* For my navbar I used code from W3Schools/bootstrap with jquery and pooper.js.
* To style my navbar, I used code from geeksforgeeks.org and medium.com (Article written by Carol Skelley).
* For my responsive gallery, I used code from taniarascia.com.
* CSS for the row and column class for the menu page was taken from W3Schools.
* The CSS for my hero-text was taken from W3Schools and amended to suit.
* Part of my hero-image CSS was given to me by my mentor, Brian Macharia.

## Images
* All images used in this project were taken from Unsplash.com

### Content
* Majority of content for this Milestone 1 Project was created by myself, Irene Neville, with help from the Code Institute
  and my mentor Brian Macharia, and other exceptions previously stated. 

### Media
* All media from Unsplash.com

### Acknowledgements

I would like to take this opportunity to thank my mentor Brian Macharia for all his help during this project
and to Anna Gilhespy and Haley Schafer for ideas on how to complete a READMEmd.

I would also like to thank the student support team, all on the CI Slack community and everyone at Code Institute for helpful
advise, videos and content.