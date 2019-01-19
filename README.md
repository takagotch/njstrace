### njstrace
---
https://github.com/ValYouW/njsTrace

```
npm install njstrace
```

```js
var njstrace = require('njstrace').inject();

var njstrace = require('njstrace').inject(),
  mymod = require('./mymod.js');
mymod.run(parseFload(Math.random().toFixed(4)));

exports.run = function(number){
  number = first(number);
  printResult(number);
}
function first(i){
  i *= 100;
  return second(i, 'sqrt');
}
function second(k, method){
  return {input: k, output: parseFloat(Math.sqrt(k).toFixed(4)), method: method};  
}
function printResult(res){
  require('fs').writeFileSync('output.txt', JSON.stringify(res));
}

var path = require('path');
var rel = path.relative(process.cwd(), __dirnamt);
var alljs = path.join(rel, '**', '*.js');
var noNodeMods = '!' + path.join(rel, '**', 'node_modules', '**');
var njstrace = require('njstrace').inject({files: [alljs, NodeMods]}),

var njstrace = require('njstrace').inject({enabled: false});
njstrace.enabled = true;

var console.logFormatter = {
  stdout: ture,
  inspectArgsMaxLen: 100,
  indenttionchar: ' ',
  inspectOptions: {colors: true}
};
var fileFormatter = {
  stdout: 'trace.out',
  inspectArgMaxLen: 0,
  indentationChar: '\t'
};
var njstrace = require('njstrace').inject({
  formatter: [consoleFormatter, fileFormatter]
});

// main.js
var Formatter = require('njstrace/lib/formatter.js');
function MyFormatter(){
}
require('util').injerits(MyFormatter, Formatter);
MyFormatter.prototype.onEntry = function(args){
  console.log('Got call to %s@Ts::Ts, num of args: %s, stack location: %s',
    args.name, args.file, args.line, args.args.length, args.stack.length);
};
MyFormatter.prototype.onExit = function(args){
  console.log('Exit from %s@%s::%s, had exception: %s, exit line: %s, execution time: %s, execution time: %s, has return value: %s',
    args.name, args.file, args.line, args.exception, args.retLine, args.span, args.returnalue !== null);
}
var njstrace = require('njstrace').inject({ formatter: new MyFormatter() }),
  b = require('./b.js');
setTimeout(function(){
  b.foo();
}, 1000);

function doFoo(){
  console.log('fooing');
  return 3;
}
exports.foo = function(){
  doFoo();
}
```

```
```


