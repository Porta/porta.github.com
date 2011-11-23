---
layout: post
title: "Por Estas Cosas Me Gusta Hacer Apps De Uso Interno"
date: 2011-09-15 18:29
comments: true
categories: javascript
---
```javascript
	$('#accept').live('click', function(){
		should = confirm('You sure, bitch?');
		if(should){
		 window.location.href = "#{accept_assignment_url(@assignment).html_safe}";
		}
	});
```
