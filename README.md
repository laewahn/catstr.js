# catstr.js

![cats'tr.js Logo](/images/logo.png)

Cats'tr.js is an easy to use JavaScript library that will push the cat content of your application to its limits! It integrates nicely with Angular.js, React.js, Node.js and many more! Cats'tr.js supports ASCII kittens, PNG kittens and even vintage GIF kittens.

Cats'tr is so easy to use that we could not bother writing extensive documentation, but we will provide you with a "Hello world" example. You might figure out the rest by yourself. Meow!

## Usage

Install Cats'tr.js simply run

```
npm install -g catstr
```

Create a file named `mittens.js` with the following content:

```
var catstr = require('catstr');

var meow = catstr.request(function(requestBuilder) {
	requestBuilder.type = 1 // request ASCII
	requestBuilder.fluffiness = {
		purr : true,
		text : "meow!"
	};

	return requestBuilder.parse();
});

meow.stream().each(function(kittens) {
	console.log(kittens);
});
```

Running `node mittens.js` should output the following: 

```
   /\___/\
   (  o o  )
   /   *   \
   \__\_/__/ meow!
     /   \
    / ___ \
    \/___\/
```