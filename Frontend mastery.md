# Front-end Mastery
Here you'll find all the necessary tools to use the GRVTY▲▼ front end stack. 

## POST-CSS

### Introduction
In GRVTY we work with postcss. And you might be wondering what is post-css? 
That's a great question, so here are some resources so you can get a grip of it.

* [PostCSS Deep Dive: What You Need to Know](https://webdesign.tutsplus.com/tutorials/postcss-deep-dive-what-you-need-to-know--cms-24535)
* [PostCSS Quickstart Guide: Instant Setup Options](https://webdesign.tutsplus.com/tutorials/postcss-quickstart-guide-instant-setup-options--cms-24536)

Those are the two first installments of the Postcss series in webtuts, we encourage you to read them all [here](https://webdesign.tutsplus.com/categories/postcss)

### Which plugins we use?

Well at this point you know that postcss works with plugins (at least I hope so) here is a list of all the plugins we currently use. If you want to add one more, chat with the development team and then add it here 😎

#### Lost Grid 🗺

* [Read the documents](http://lostgrid.org/docs.html)
* [Basic Lost video tutorial (see episodes 7 throught 13)](https://www.youtube.com/watch?v=e3J4wZWlQUk)

#### CSS next 🚙

* [Read the documents](http://cssnext.io/features/)

#### PostCSS mixins 📝

* [Read the documents](https://github.com/postcss/postcss-mixins)

#### PostCSS partial import ✂️

* [Read the documents](https://github.com/jonathantneal/postcss-partial-import)

#### PostCSS zindex order 📏

* [Read the documents](https://github.com/ben-eb/postcss-zindex)

We use some others plugins, but they're used in the background when webpack or bruch compiles your PostCSS. Here they are:

* **postcss-loader**
* **postcss-minify-params**
* **postcss-minify-selectors**
* **postcss-will-change**

## How we structure our styles

We have a particular way to write our styles, here we provide you a simple example:

#### Folder structure

Here is the simple structure we follow to develop our frontend.
```
|- CSS
  |- Waddles
    |- base.pcss
    |- texts.pcss
    |- ...
  |- Vendors
    |- animatecss.pcss
  |- [Page name]
  |- app.pcss
```

Waddles contains our base styles, from there we boostrap, so every project contains a basic skeleton of waddles.
Any component style that will be re-used through out the page should live there for now waddles contains the following files, if you want solid examples of what waddles contains (navigate this project)[https://github.com/grvty-labs/IQ-Produccion/tree/develop/iq_produccion/web/static/css/waddles]:

* **settings.pcss:** *global variables for the aplication, remember DRY*
* **base.pcss:** *general html styles, like body styles. General styles like font sizes, background color etc.*
* **buttons.pcss:** *Buttons general styles, here all our variations of buttons must live, since they're reused all along the application*
* **custom-animations.pcss:** *we love microinteractions and user delights, here we write our custom animations*
* **forms.pcss:** *pretty self explanatory, our form styles live here*
* **texts.pcss:** *Our text styles, paragraphs, headers, spans, all live here. Remember Vertical Rythms*
* **utils.pcss:** *Classes that might be used by various files, and will be repeated throuhgt all the application*
* **waddles.pcss:** *here we import only the files we need, we expect waddles to grow in the following projects. So naturally you might not need all the files in the future*

That's pretty much it for waddles, as we mentioned before we expect waddles to grow so when adding files to waddles keep in mind to make the classes modular, easy to read and modify. 
