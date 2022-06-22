# My Awesome Project
![Spokane Public Library]()

This is a clone of the Spokane Public Library's webiste built with Django,
and is currently still a work in progress.

To use the Django catalog application:
1. Clone the repository
2. Setup a python virtual enviornment
3. Run `pip install -r requirements.txt`
4. Run `python manage.py migrate`
5. Run `python manage.py runserver`
6. The catalog app will be hosted on a local server at http://127.0.0.1:8000/
7. When done, quit the server with `CONTROL-C`

Test accounts:
- testbob, password: locallibrarytest
- testsally, password: locallibrarytest
- testlibrarian, password: djangolocal
- Admin account, localhost:8000/admin:
    - user: bideinsilence
    - password: ahwpYSJ2yYe2VG

**See the homepage live:** 


## How It's Made:

**Tech used:** HTML, CSS, JavaScript, and the python Django framework

I originally built the backend catalog before moving on to recreating the
Spokane Library's homepage. I had expected the Library's site to be easy to
download and copy, but upon inspecting their source code, I discovered that
their site is an impressive amount of div soup that appears to have possibly
been built with a Wordpress site builder. So, I decided against just copying
their code and assets and chose to take the opportunity to hone my html and css
skills by rebuilding a near pixel perfect copy of their homepage from scratch.

My next step is to serve my Django library catalog and home page from my Django
app and link the catalog to my small database. I intend to also build in some
search functionality and build a copy of the Spokane Library's catalog search
result page.

After that, I'll incorporate the user sign in/sign out features I've already
built into the Django app, and then finally host the site live for demonstration
on a service such as Heroku.


## Optimizations
My library homepage is much smaller and more performant than the Spokane Library
site.

The Spokane Library's homepage footer is built with blocks that are sized with
different percentage widths and disappear and reappear depending on the size of
the viewport through which the site is viewed. I borrowed some of the same
techniques to make my version a more faithful recreation, but If I was to build
the original site myself I would build the footer (and still may build it) with
CSS grid for a simpler, easier to understand structure, and nearly similar
looking footer that would just move various blocks around as the viewport size
changes.

I would also build the site with a dynamically sized responsive root font,
something like: 
```
    /* 1rem ensures font-size never drops below the default value */
    font-size: calc(1rem + 0.5vw);
    font-size: clamp(1rem, 1rem + 0.5vw, 2rem);
```
rather than adjusting the font size at various breakpoints as the original site
does.


## Lessons Learned:

So far I've learned so much about how to recreate a website and make it look
like it's source material, how to build a functional web application with user
authentication using Django, and how to connect it all to a simple database.


