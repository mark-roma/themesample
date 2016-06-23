romademo theme for demonstration purposes only. code notes are as follows:

History:
On my resume you'll see a list of sites including chenmed.com, jencaremed.com, chenmedicalcenters.com, pmrmed.com, and chenmedmarketing.com (not to mention my own site at markroma.com) Aside from my own, which uses bootstrap, all of chenmed's code is protected under their rigorous NDA. So I have proposed to throw together a similar yet wholly different generic site to showcase some of my skills. You can see a demo at markroma.com/demo
The following information explains my criteria for producing a 24 hour site, some of my methods, and observations about more "proper" ways of developing when given a longer runway.

Delivery of a full site with dynamic content and all the kinds of bells and whistles I can create would take a bit more than 24 hours, so I've created some shorthand to show what I'm capable of a) on short notice and b) by using some similar design and layout from two previous projects I did for ChenMed. Namely JenCareMed.com and ChenMedMarketing.com. Since mobile development was in progress when they canned me, I've created a very similar layout with a single breakpoint to illustrate how to create mobile variations without the use of a framework.  Below is a description of the criteria I gave myself for the content. (I chose Capoeira as a subject because I know James is a fan, and there's a lot of images and video to pull quickly so it saved me a lot of time.)

content requirements- 1) frontpage/splash page 2) basic page (for about and other info) 3) toques de berimbau (for information about the music) 4) history (for information about the different eras in the timeline)

1) frontpage- should display the three available themes of basic info (about us, how to get involved)
2) should display an article with title, text, photo, and related feed block to the right
3) 6-8 different rhythms that display the name, the structure, and link to a youtube clip demo of playing the music
4) display the era (time period) major figure involved (i.e. mestre bimba) an overview of the event with in-text links to language terms

Caveats and explainations:
Rather than using a framework like bootstrap or foundation, the other clean way to create mobile degradation for a site is to use @media breakpoints. for my personal site at markroma.com I've used @media (min-width:1199px) and (max-width:1350px) for desktops, @media (min-width:992px) and (max-width:1199px) for laptops and netbooks, @media (max-width:991px) and (min-width:768px) for tablets in portrait mode, @media (max-width:767px) and (min-width:480px) for phablets and those damn big phones like the old samsung note, @media (max-width:480px) for phones. 
In this case, rather than create all those selectors and have to QA them, I used the browser client to create .body.mobile CSS exceptions, so the site has just two modes: desktop and mobile. Be aware that only minimal cross-browser QA was conducted in this short runway, so anything outside of firefox, IE, Chrome, and Android tablets and phones might go wonky on you.

When viewing on desktop you should see a static one-line main nav, a 2 column layout with a subnav on the left and a slider of content on the right. (very similar also to the ski jacket line that Mark is currently working on.) resizing the browser shows that the slider will drop items until it gets all the way down to just one item in the set (with back and forward arrows progressing through the items.) Clicking on the title will open formatted colorbox modals with content and videos in them, but the pages for these nodes are also minimally styled to illustrate CSS control of the content.

Viewing in mobile should stack the main nav items vertically creating a full width display of all links. Obviously in a full development cycle I'd be making the transitions animated and such, with the fun "three line" menu tab like i have on my personal site at markroma.com. Viewing in mobile should also drop the left column nav over the main content into a single column orientation. again, whether in portrait or landscape the jquery slider will clip items to respond to the available space. Also, clicking on the slider titles in mobile should open colorbox modals styled to fit mobile view.

Deliverables:
on my git I am sharing the entire theme for you guys to poke around in. Within the theme, you'll find 3 interesting files to review. I have included markup.css to show what my first draft CSS looks like as I'm experimenting and building off the supplied design files. the style.css is minified to speed load on the demo site at markroma.com/demo.  Also in the git is a file called scss.txt which includes SASS/SCSS coding examples of how I'd lay out the styles for the site using that methodology. given the short timeframe I wanted to knock this out and give you indicators about how my CSS markup and SCSS markup are similar and complimentary. 

