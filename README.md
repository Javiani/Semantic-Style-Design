# Semantic Style Design

### What is Semantic Style Design?

Semantic Style Design is just a Css architecture proposal, based on some very consolidated ideas and projects. It's a simplified mix of some great abstractions we have today:

- [Rscss](//rscss.io/)
- [Atomic Design](//bradfrost.com/blog/post/atomic-web-design/)
- [ReactJS](//facebook.github.io/react/)

### Abstractions

On SSD you should have only 3 abstractions:

- /Components
- /Layouts
- /Pages

### Components

Every module should be created as a component. A complex structure is just a combination of
several components. Just like ReactJS model, you should start with a very basic element,
and augment it by wrapping with other components, just like a Decorator Pattern in programming.

The pattern to create components used here is one of the best and simple Css patterns out there, the [Rscss](//rscss.io/) pattern.

All concerns like, `configs`, `animations`, `grids`, or any other structures should be placed under **components** folder, using semantic names.
Not context names, like `home`, `checkout`, etc.

The semantic name should describe what that component is and represents, not where it is.

Component's class names should be exactly the file name.

```scss
//components/form/input.scss
.input{
    border :1px solid #ededed;
    border-radius:30%

    &.-disabled{ /* ... */ }
}
```

#### Folder structure
```
├── components
|   ├── configs/
|   └── animations/
|   └── grids/
|   └── forms/
|   └── inputs/
|   └── buttons/
|   └── tables/
|   └── titles/
|   └── sections/
...
├── layouts/
├── pages/

```

### Layouts

Layout is the skeleton of a page, reusable layout sections, it's where you will gonna use your grid systems.
It can be simple as a `content-sidebar-footer` or very complex with several structures and variations, or just a combination of several layout pieces. It is up to you to break it on folders or not, and naming folders following your project standard.


### Pages

Pages are the output of your css, it should import all components and templates structures in order to compose the entire page.
You can tweak/change dimensions, positioning and other kind of attributes for some specific purposes.

You may create any folder structure inside **pages** according to your project needs.

### Contribution

The idea of this project is to keep it as simple as possible.
Please, fork it, pull request it, use it =)
