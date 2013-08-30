# grunt-inline-imgsize

> Inject width and height for img tags

## Getting Started
_If you haven't used [grunt][] before, be sure to check out the [Getting Started][] guide._

From the same directory as your project's [Gruntfile][Getting Started] and [package.json][], install this plugin with the following command:

```bash
npm install grunt-inline-imgsize --save-dev
```

Once that's done, add this line to your project's Gruntfile:

```js
grunt.loadNpmTasks('grunt-inline-imgsize');
```

If the plugin has been installed correctly, running `grunt --help` at the command line should list the newly-installed plugin's task or tasks. In addition, the plugin should be listed in package.json as a `devDependency`, which ensures that it will be installed whenever the `npm install` command is run.

[grunt]: http://gruntjs.com/
[Getting Started]: http://gruntjs.com/getting-started
[package.json]: https://npmjs.org/doc/json.html

## The "inlineImgSize" task

Use the **inlineImgSize** task for injecting the width and height properties of `<img>` tags. This enhances the user experience because fewer repaints are required as a page's assets are loaded in.

### Overview
In your project's Gruntfile, add a section named `inlineImgSize` to the data object passed into `grunt.initConfig()`.

```js
grunt.initConfig({
  inlineImgSize: {
  }
})
```

### Options

#### options.encoding
Type: `String`
Default value: `'utf8'`

The encoding of the file contents.

### Usage Examples

#### Basic Image Size Inlining

```js
grunt.initConfig({
  inlineImgSize: {
    files: {
      src: ['index.html', 'contact.html']
    }
  }
})
```

#### Custom Options

```js
grunt.initConfig({
  inlineImgSize: {
    options: {
    },
    files: [{
      expand: true,
      cwd: 'src',
      src: ['*.html'],
      dest: 'dest/'
    }]
  }
})
```
