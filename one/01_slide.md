!SLIDE 
# Ruby Training
## @gautamrege
## @joshsoftware

!SLIDE bullets 
# Introduction

* BE - PICT, 2000
* Working in rails since 2006
* Co-founded Josh Software 2007
* Previous Experience
* Cybage, Zensar, Symantec

!SLIDE bullets
# Agenda - Day 1

* Learn Ruby
* Why, what, how?
* Basic Syntax, Block, iterators
* File handling
* Regular Expressions
* Hands on!

!SLIDE bullets
# Agenda - Day 2
* Classes, Modules & Variables.
* Threads
* Exceptions
* Hands on!

!SLIDE bullets incremental
# History of Ruby

* Yokohiro Matsumoto - @matz
* 1995
* Rails - David Hansson
* 2005

!SLIDE bullets 
# Ruby Vs others

* Script Vs object code
* Compiled Vs Interpreted
* Pure OO ?
* Pointers?
* Garbage collection?

!SLIDE
# My Mother can read my code
## Ruby Propoganga

!SLIDE
# What can this code mean??
    @@@ruby
    10.times do |i|
      puts i
    end

!SLIDE
# What can this code mean??
    @@@ruby
    ['ruby', 'rocks'].each do |word|
      puts word
    end

!SLIDE
# What can this code mean??
    @@@ruby
    { 'ruby' => 'ROCKS'}.each_pair do |k,v|
      puts "#{k.upcase} #{v.downcase}"
    end

!SLIDE center
# Challenge #1
## Summation of homogenous array

    @@@ruby
    [1, 2, 3, 4]

!SLIDE
# Obvious ruby solution
    @@@ruby
    [1, 2, 3, 4].inject(0) do |sum, i| 
      sum + i 
    end

!SLIDE
# Kick-ass solution
    @@@ruby
    [1, 2, 3, 4].reduce(:+)

!SLIDE center
# Challenge #2
## Summation of heterogenous array
    @@@ruby
    [1,'1', 1.1, 2, 3, 4, 'a', nil]
 
!SLIDE
    @@@ruby
    arr = [1, '1', 1.1, 2, 3, 4, 'a', nil]
    
    arr.inject(0) { |sum, i| sum + i.to_f }

!SLIDE bullets
# Installation

* ruby & irb
* gem -v
* gem list
* gem install 
* RVM awesomeness

!SLIDE bullets
# Language syntax

* strings & numbers
* to\_s, to\_i, to\_a
* method chaining
* sort!, include? methods

!SLIDE bullets
# Language syntax
* Symbols
* Blocks
* Array & Hashes
* def leppard

!SLIDE bullets
# Regular expressions

* rubular.com
* IP address format validation!

!SLIDE bullets
# Language constructs

* Classes & Objects
* def initialize
* Accessors
* Instance variables 

!SLIDE bullets
# Get deeper

* Closure
* Reflection
* send
* call 

!SLIDE 
# Challenge #3
# Closures

!SLIDE 
# Simple closure
    @@@ruby 
    def print_anything
      puts yield
    end

    # print_anything { 'hello' }
    # print_anything { 1 + 2 }
    # print_anything { "hello #{1 + 2}" }

!SLIDE
# Complex closure
    @@@ruby

    foo = Proc.new do |a, b|
      puts "#{a + b}"
    end

    foo.call(10, 20)

!SLIDE 
# Try Ruby
## http://tryruby.org

!SLIDE bullets
# Module Mixin

* Diamond inheritance problem
* Single class inheritance
* Interfaces in Java

!SLIDE bullets
# File Handling

    @@@ruby

    File.open("path/to/file") do |f|
      # File operations
    end

!SLIDE bullets
# File Handling

    @@@ruby

    File.open('file.txt').readlines.each do |l|
      # Process the line
    end

!SLIDE
# CSV handling

    @@@ruby
    CSV.open('f.csv').readlines.each do |l|
      # Process the array of CSV fields!      
    end

!SLIDE bullets
# File handling

* Did we close any file-handles? :)
* Write in the same way as read!

!SLIDE
# Threading

    @@@ruby
    tid = Thread.new do 
      # Thread code processing
      Thread.pass
    end

    tid.join

!SLIDE 
# Fancy stuff in Ruby

!SLIDE 
# Json built-in Hash support
    @@@ruby
    {'a' => 1, a: 1, 1 => 2, b: 'a'}

!SLIDE
# Stubby proc
    @@@ruby
    foo = -> a { puts a}
    foo.call(10)

!SLIDE
# Oniguruma 
    @@@ruby
    "yo 2012!".match(/(?<year>\d+)/)[:year]

!SLIDE bullets
# The other neat stuff

* All new GC
* Splat arguments
* OrderedHash
