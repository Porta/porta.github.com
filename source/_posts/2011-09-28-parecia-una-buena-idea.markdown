---
layout: post
title: "Parecia Una Buena Idea..."
date: 2011-09-28 09:16
comments: true
categories: perl
---
Cosas que pasaban cuando programaba Perl

```perl
	sub get_next {
		my $self = shift;
	
		my $array = $self->{array};
		my $row = pop(@$array);
	
		if ($row){
			bless $row, $self->{isa};
		}
		else {
			return 0;
		}
	
		return $row;
	}
```