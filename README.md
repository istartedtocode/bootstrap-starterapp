# bootstrapstarter
=============

This is a basic Rails 4 app with [Bootstrap] 3.1.1 included without using a gem. I build this for myself after looking at several tutorials and want to share it.

## Installation

Just clone this repository to your computer and get started building your app.

* Ruby version: ruby 2.1.1p76
* Rails: 4.1.0.rc1


## How To build it yourself

### Rails app

Generate a new rails app

```bash
$ rails new [yourappname]
```

### Download Bootstrap
Download the latest version from [Bootstrap](http://www.getboostrap.com/getting-started) (In my case that it 3.1.1) and unzip its contents. There are several files in it but we need only the following

`bootstrap-3.1.1-dist/css/bootstrap.min.css`

`bootstrap-3.1.1-dist/js/bootstrap.min.js`

The .min files are the same as the ones without it but in a more compact form. You could also use the other ones.

If you wanna include glyphicons you also need all files out of

*bootstrap-3.1.1-dist/fonts/*

### Copy the files to your app

Copy `bootstrap.min.css` to *bootstrap-starterapp/vendor/assets/stylesheets/*

Copy `bootstrap.min.js` to *bootstrap-starterapp/vendor/assets/javascripts/*

For the use of glyphicons copy the folder `fonts` to *bootstrap-starterapp/vendor/assets/fonts*

### Adding the files to your assets


Go to *app/assets/stylesheets/application.css.scss* and add:
```ruby
 *= require bootstrap.min
 *= require_tree .
 *= require_self

```

Go to *app/assets/javasctips/application.js* and add
```ruby
//= require jquery
//= require jquery_ujs
//= require bootstrap.min
//= require turbolinks
//= require_tree .

```

And you are done! You can use all the bootstrap layouts you want.

## License
None. Please feel free to use however you want it.