---
layout: post
title: "Supersize Me"
date: 2011-10-13 00:05
comments: true
categories: javascript
---
Anda, digamos.

```javascript
	(function( $ ){
	  $.fn.redimension = function( options ) {
	    var settings = {
	      'to'       : window,
	      'sides'    : []
	    };
	    return this.each(function() {
	      var $this = $(this);
	      if ( options ) {
	        $.extend( settings, options );
	      }
	      $.each(settings.sides, function(i, side){
	        var attr = 'min-'+ side;
	        $this.css(attr, ( $(settings.to)[side]() ) );
	      });
	    });
	  };
	})( jQuery );

	//Resize my_div to window object
	$('#my_div').redimension({to: document, sides: ['height','width']});

	//Resize my_div only in width, if no "to" param, it defaults to window
	$('#my_div').redimension({sides: ['width']});

	//Resize my_div to another div height and width
	$('#my_div').redimension({to: '#other_div', sides: ['height','width']});
```

Pero sin exagerar.

