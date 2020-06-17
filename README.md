# bergamot
TeaCSS/CommonJS capable simple and blazing fast bundler without AST transforms
## Description
Bundle css && js into single files for use on frontend
Can also process `.tea` files

## Install
npm install --global bergamot 

## Use
can be used in next ways:
- make "bergamot.config.js"
```javascript
module.exports = {
    project: {
        entry_point: "<path_to_folder>/index.js",
        bundle_path: "<path_to_bundle>/bundle.min.js", //file name can be changed
        js_transform: (js) => ''// custom js transformation 
    }
}
```
-- call 
```
bergamot <command>
```
You can have a few configs:
```javascript
module.exports = {
    project: {
        entry_point: "<path_to_folder>/index.js",
        bundle_path: "<path_to_bundle>/bundle.min.js", //file name can be changed
        js_transform: (js) => ''// custom js transformation 
    },
    other_project: {
        entry_point: "<path_to_folder>/index.js",
        bundle_path: "<path_to_bundle>/bundle.min.js", //file name can be changed
        js_transform: (js) => ''// custom js transformation 
    }
}
```
then call
```
bergamot <command> <config_name: other_config>
```
Also you can use in next way:
```
bergamot <command> <entry_point> <bundle_path>
```

### Commands
- "build"  - build project files (without minify them)
- "watch"  - build and rebuild when some project file changed (usefull for development)
- "minify" - build and minify js & css files (for production)



