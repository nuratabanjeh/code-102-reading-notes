# Read09

### Functional Programming Concepts

1. What is functional programming?

* is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data

2. What is a pure function and how do we know if something is a pure function?

* It returns the same result if given the same arguments (it is also referred as deterministic)

* It does not cause any observable side effects

3. What are the benefits of a pure function?

* The code’s easier to test

4. What is immutability?

* Unchanging over time or unable to be changed. When data is immutable, its state cannot change after it’s created. If you want to change an immutable object, you can’t. Instead, you create a new object with the new value.

5. What is Referential transparency?

* if a function consistently yields the same result for the same input,

* pure functions + immutable data = referential transparency

#### Modules and require()

1. What is a module?

* a module is a part of the application that has a certain functionality

2. What does the word ‘require’ do?

* it allows a code written in another file to be used.

3. How do we bring another module into the file the we are working in?

* by exporting the part we want to use and then requiring it in the main file.

4. What do we have to do to make a module available?

* export the required part.

#### Things I want to know more about