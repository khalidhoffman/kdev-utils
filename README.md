# gulp-utils [![Build Status](https://travis-ci.org/khalidhoffman/gulp-utils.svg?branch=master)](https://travis-ci.org/khalidhoffman/gulp-utils)
A personal dev library for quicker for development

#### How To Use
1. run `npm i --save-dev git://github.com/khalidhoffman/gulp-utils.git`
2. Run `gulp --tasks` from root folder to see list of tasks.
 
#### Example Config
```
{
  "name": "project_name"
  "prefix": "wp_table_prefix",
  "dbNamePrefix" : "for_wordpress_dev",
  "avocodeSelector" : "for_avocode_dev",
  "basePath" "/an/absolute/path",
  "tasks" : [
    {
      "name" : "stylus",
      "input": "relative/path/to/stylus/folder/from/basePath",
      "output": "relative/path/to/stylesheets/folder/from/basePath"
    },
    {
      "name" : "pug",
      "input": "relative/path/to/pug/folder/from/basePath",
      "output": "relative/path/to/php/folder/from/basePath"
    }
  ]
}
```
* 

##### Config Details
* All paths are relative to `basePath`. `basePath` is an absolute path.
* `basePath` defaults to `{current working directory}`
* using the predefined value `wordpress` for `basePath`  to `{current working directory}/wp-content/themes/dp-{projectName}`

###### Task Options

Task Names   | Details
-------------|---------
`pug`        | [additional helper functions](commands/pug/helpers/_functions.pug) are saved  and included before compilation. compiles to `.php` files
`stylus`     | [additional helper functions](commands/stylus/lib/stylus/) are included at compilation. compiles to css
`less`       | compiles to css
`js`         | beautifies js. Overwrites file
`js-bundle`  | bundles and minfies with requirejs. input path should be a path to a requirejs config `build.js`
`compass`    | compiles to css
`jsx`        | compiles js to same directory as original `.jsx` file
`sass`       | compiles to css
`pugjs`      | [additional helper functions](commands/pug/helpers/_functions.pug) are saved  and included before compilation. compiles to `.ejs` files
