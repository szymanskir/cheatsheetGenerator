# cheatsheetGenerator

Run the app in a docker container with:
```
docker-compose up
```

## Content configuration

Content of cheatsheet can be configured by loading .yml file and/or editing Configuration (.yml) input field.

File structure is presented below:

```
name: Library name
description: Library description
footer: Content of footer
pages:
- cards:
  - title: Card title
    methods:
    - name: Method name
      description: Method description
      params:
      - name: Method parameter
        description: Parameter description

```

Elements of pages array are cards located on specific page. Cards are displayed in columns in order set in configuration file. For each card title and methods can be defined. Methods is an array containing names, descriptions and parameters. Method parameters are printed between "()" next to method name. In addition, if parameter description is defined, parameter description will appear under method description.

## Styles configuration

You can configure cheatsheet styles with css. Upload your .css file and/or edit Configuration (.css) input field.

### General
The exemplary cheatsheet with possible changes is presented below:

<img src="documentation/css-vis.png" width="500" />

To edit styles for whole cheatsheet do not specify class:
```
background-color: lightGray;
```

Header:
```
.header {
  background-color: gold;
}

.header-title {
  color: rgba(255, 102, 0);
}

.header-title-name {
  font-style: italic;
}

.header-description {
  color: white;
}
```

Logo:
```
.logo {
  transform: rotate(180deg);
}
```

Footer:
```
.footer {
  font-weight: bold;
}
```

### Card

<img src="documentation/css-card-vis.png" width="300" />

For changes affecting cards use these classes:

```
.card {
  border: 3px solid rgba(255, 102, 0);
}

.card-header {
  border: none;
  background-color: white;
}

.card-body {
  background-color: lightskyblue;
}
```

Methods are located inside cards. Use these classes to change theirs style:
```
.method {
  border-top: 2px dotted black;
}

.method-name {
  color: gold;
}

.method-parameter {
  font-size: x-small;
}

.method-description {
  font-style: italic;
}
```

Also parameters (for each method) can be changed:
```
.parameter {
  border-left: 2px solid rgba(255, 102, 0);
}

.parameter-name {
  text-decoration: underline;
}

.parameter-description {
  text-align: right;
}
```
