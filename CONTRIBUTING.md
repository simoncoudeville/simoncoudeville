# Contributing

You are free to contribute to Chopstick via GitHub Pull Requests. We have a couple of simple guidelines we try to follow, of which most are taken from the [CSS Tricks Sass Style Guide](http://css-tricks.com/sass-style-guide)

## Git branch model
[A successful git branching model](http://nvie.com/posts/a-successful-git-branching-model/)

## Releases
[Semantic versioning](http://semver.org/)

## How to pull request

1. [Fork](https://github.com/getchopstick/chopstick-boilerplate/fork) this repo.
2. Create a branch `git checkout -b feature--name`
3. Commit your changes `git commit -am "New feature"`
4. Push to the branch `git push origin feature--name`
5. Open a [Pull Request](https://github.com/getchopstick/chopstick-boilerplate/pulls)

## SCSS order

1. @extends
2. Regular styles
3. @includes
4. Nested selectors

Example:

    .weather {
      @extends %module; 
      background: #fff;
      @include transition(all 0.3s ease);
      > h3 {
        border-bottom: 1px solid white;
      }
    }

## Nesting

Never nest more than three levels deep, never nest more than 50 lines long. This keeps code readable and usable.

## Global files

Only `@include` in the global screen.scss file. Never write SCSS directly in screen.scss. Order of importing is always as described in `screen.scss`.

## Be generous with comments

Comments get filtered out when compiling. If you do *anything* that can not be immediately understood: comment it.

