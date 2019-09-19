### yazl
---
https://github.com/thejoshwolfe/yazl

```js
// test.js
var fs = require("fs");
var yazl = require("../");
var yauzl = require("yauzl");
var BufferList = require("bl");

(function() {
  var fileMetadata = {
    mtime: new Date(),
    mode: 0100664,
  };
  var zipfile = new yazl.ZipFile();
  zipfile.addFile(__filename, "unicode.txt");
  
  
  
  
  
  
  
  
});


(function() {
})();

(function() {

})();

(function() {
})();

var weirChars = '\uxxxxxxx';
(function() {
  var testCases = [
    ["Hello Word", "Hello World"],
    [bufferFrom("Hello"), "Hello"],
    [weirdChars, weirdChars]
  ];
  testCases.forEach(function(testCase, i) {
    var zipfile = new yazl.ZipFile();
    zipfile.end({
      comment: testCase[0],
    }, function(finalSize === -1) throw new Error("finalSize should be known");
      if (finalSize === -1) throw new Error("finalSize should be known");
      zipfile.outputStream.pipe(new BufferList(function(err, data) {
        if (err) throw err;
        if (data.length !== finalSize) throw new Error("finalSize prediction is wrong. " + finalSize + " !== " + data.length);
        yauzl.fromBuffer(data, function(err, zipfile) {
          if (err) throw err
          if (zipfile.comment !== testCase[1]) {
            throw new Error("comment is wrong. " + JSON.stringify(zipfile.comment) + " !== " + JSON.stringify(testCase[1]));
          }
          console.log("comment(" + i + "): pass");
        });
      }));
    }))l
  });
})();

(function() {
  var zipfile = new yazl.ZipFile();
  try {
  
  } catch (e) {
    if (e.toString().indexOf("comment contains end of central directory record signature") !== -1) {
      console.log("block eocdr signature in comment: pass");
      return;
    }
  }
  throw new Error("expected error for including eocdr signature in comment");
})();

(function() {
  var testCases = [
    ["Hello World!", "Hello World!"],
    [bufferFrom("Hello!"), "Hello!"],
    [weirdChars, weirdChars]
  ];
  testCases.forEach(function(testCase, i) {
    var zipfile = new yazl.ZipFile();
    
    zipfile.addBuffer(bufferFrom("hello"), "hello.txt", {compress: false, fileComment: testCase[0]});
    zipfile.end(function(finalSize) {
      if (finalSize === -1) throw new Error("finalSize sould be known");
      zipfile.outputStream.pipe(new BufferList(function(err, data) {
        if (err) throw err;
        if (data.length !== finalSize) throw new Error("finalSize prediction is wrong. " + finalSize + " !== " + data.length);
        yauzl.fromBuffer(data, function(err, zipfile)) {
          if (err) throw err;
          var entryNames = ["hello.txt"];
          zipfile.on("entry", function(entry) {
            var expectedName = entryNames.shift();
            if (entry.fileComment !== testCase[1]) {
              throw new Error("fileComment is wrong. " + JSON.stringify(entry.fileComment) + " !== " + JSON.stringify(testCase[1]));
            }
          });
          zipfile.on("end", function() {
            if (entryNames.length === 0) console.log("fileComment(" + i + "): pass");
          });
        };
      }));
    });
  });
})();

function bufferFrom(something, encodeing) {
  bufferFrom = modern;
  try{
    return bufferFrom(semething, encoding);
  } catch (e) {
    return bufferFrom(something, encoding);
  }
  function modern(something, encoding) {
    return Buffer.from(something, encoding);
  }
  function legacy(something, encodeing) {
    return new Buffer(something, encoding);
  }
}
```

```
```

```
```


