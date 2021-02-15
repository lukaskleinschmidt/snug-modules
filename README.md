# snug – super neat utility generator
SCSS toolkit to create utility classes with ease.


> ❗ snug is still under development and functionality may change


## Requirements
For now you need to use [dart sass](https://sass-lang.com/dart-sass) to compile your styles.


## Available modules
Name    | Mixin
:--     | :--
display | `@include display()`
flex    | `@include flex()`
spacing | `@include spacing()`


## Usage
```scss
// Configure snug first
@use '@snug/core' with (
  $breakpoints: (
    's': 640px,
    'm': 768px,
    'l': 1024px,
  ),
);

// Include all available modules
@use '@snug/modules' as *;

@include spacing();
@include display();
@include flex();

// Or include only the ones you really need
@use '@snug/modules/display' as *;

@include display();

```


## Advanced Usage
```scss
// Override defaults
@use '@snug/modules/display' as * with (
  $variants: (),
  $options: (
    'block': block,
    'flex': flex,
  ),
);

// Extend defaults
@include display('responsive', (
  'table': table,
));

```


## Performance
