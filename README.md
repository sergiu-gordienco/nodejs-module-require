# nodejs-module-require

> nodejs-module-require is a custom module loader

returns a {function} that is loading classes and storing them in a object,
also giving some extra functionalities

## How to use:

```javascript
	var mrequire	= require("module-require");
```

### Loading express library

```javascript
	var express	= mrequire("express");
```

### Loading a custom module and use it with a short name

```javascript
	// loading module
	mrequire("myChoosedModuleName1", "http://www......./file.js");

	// use custom module
	var m1	= mrequire("myChoosedModuleName");
```
>	also can be used relative source "./file.js"

### Link a nodejs module with onother name

```javascript
	// link "express" server to "server-module"
	mrequire("server-module", "express");
	// Using renamed module
	var server	= mrequire("server-module");
```