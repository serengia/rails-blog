### How to configure Boostrap 5 and Rails 7 for an existing Project

1. Add the following to the GemFile
   `gem 'sassc-rails'` # (after ruby and before gem rails) `gem 'bootstrap', '~> 5.2.0'` (after gem rails)

2. Navigate to the command line and run `bundle install`

3. Navigate to your `app > asset > stylesheets` and change the file `application.css` to `application.scss` (Sass file)

4. Delete all the content of `application.scss` then write `@import "bootstrap";`
5. For the Bootstrap js dependencies, navigate to `app>javascript>application.js` then add these before the `// Configure your import map...` :

```
//= require popper
//= require bootstrap-sprockets
```

6. Boostrap 5 should now be working with the Rails 7.
