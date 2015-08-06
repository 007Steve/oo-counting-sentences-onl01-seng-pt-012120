# Counting Sentences

## Objectives
1. Practice defining instance methods on a class
2. Learn about monkey patching

## Description

In this lab, you'll be adding an instance method to Ruby's `String` class. We generally want to avoid altering built-in classes (especially if we are working with other people), but in this case, we're not overwriting any methods, and it's a good exercise in OO programming. The practice of adding methods to or altering Ruby's built in classes is called monkey patching. 

### Monkey Patching

Monkey patching is the practice of adding methods to or altering Ruby's core classes. Monkey patching is dangerous! What if, for example, you decide to monkey patch Ruby's String class to produce a quick-fix that shortens a certain section of code in your program. Then, months later, you run into major bugs as a result, or some of your collaborators don't know about your monkey patch and develop bugs of their own that they don't know the origin of? For reasons like these, monkey patching should be considered very, very carefully. We're going to do it today, just for fun, but you do want to avoid doing it when working on your own programs. 

## Instructions

What we'd like to be able to do is call a `count_sentences` method on a string, and
get back a, well, count of sentences in that string. In other words:

```ruby
"This is a string. It has three sentences. Right?".count_sentences
# => 3
```

1. Fork and clone this lab. Run the test suite to get started. 
2. Check out the `lib/count_sentences.rb` file. You'll be writing you code in the body of the `count_senteces` instance method, a monkey patch on the String class. 
3. A few things to keep in mind:

* It's difficult to count discreet units of characters in a string. An array, however, is a different stories. Arrays have a great `.count` method. How can you `.split` your string into it's component sentences?
* Make sure you take into account that a period, a comma, a question mark or an exclamation point can end a sentence.
