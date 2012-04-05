---
layout: post
title: "Array to_sentence"
date: 2011-11-23 08:06
comments: true
categories: javascript
---
No es que haya descubierto la pólvora...

```javascript
	Array.prototype.to_sentence = function(){
		var self = this;
		var out = "";
		switch (self.length){
		  case 0:
		    break;
		  case 1:
		    out = self[0];
		    break;
		  case 2:
		    out = self[0] + " and " + self[1];
		    break;
		  default:
		    out = self.slice( 0, (self.length - 1) ).join(', ') + " and " + self[self.length - 1];
		}
		return out;
	};
```

Pero está bien tenerlo. Gracias, Rails.
