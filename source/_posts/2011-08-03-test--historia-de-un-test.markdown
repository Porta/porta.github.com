---
layout: post
title: "Ejemplo de Factory Girl"
date: 2011-08-03 13:53
comments: true
categories: ruby
---
Ejemplo de Factory Girl

```ruby
    FactoryGirl.define do
      factory :unsaved_transaction, :class => Transaction do
        association :user, :factory => :new_random_user
        amount 24
        currency 'USD'
        state 'instant'
        validation 'QUETETIRODELASPATAS'
      end
    end
```
