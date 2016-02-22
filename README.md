# What's included?

#### Defaults

* Font Size - Sane default values for responsive text sizing (from [typecast.com](http://typecast.com/blog/a-more-modern-scale-for-web-typography))
* Fonts - Includes Google Web Fonts "montserrat" and "open sans".  Make sure to comment
this out if you don't plan to use these.
* Variables - Includes variables for defining media queries, for example:

```sass
  .my-class {
    @include media($ipad) {
      background: inherit;
    }
    background: #FFF;
  }
```

This requires Bourbon.

* Tags - Basic defaults for the html, body, a, ul, and li tags.

#### Elements

* Color bar - A mixin for a full-width horizontal bar of a given color.

Specify the height and what color(s) you want, and it will accept a variable number
of arguments and create a horizontal bar of the given colors:

```scss
.color-bar-top {
  @include color-bar(10px, #3FB8AF, #7FC7AF, #DAD8A7, #FF9E9D, #FF3D7F);
}
```

```slim
 .color-bar-top
   ul
     - 5.times do |_|
       li
```

This is the resulting color bar:   

![image](https://cloud.githubusercontent.com/assets/6726985/13217337/1cc78922-d9a5-11e5-9f41-9405c5a0e0c6.png)

See [this codepen](http://codepen.io/etdev/pen/KVjode?editors=1100) for more info.

# Dependencies
* [Sass](https://github.com/sass/sass)
* (Optional) [Bourbon](https://github.com/thoughtbot/bourbon)

# Install

I haven't gotten around to packaging it as a gem, so you'll have to `git clone`
the repo, move it to your assets/stylesheets folder and `@import scss_helpers`
