# Noisebridge CPP Class

Welcome to the Noisebridge CPP class! This repository contains lesson plans,
notes, examples, and more for Noisebridge's upcoming CPP class.

## Course Description

A lot of this class is based on the way that the [Noisebridge PyClass
operates.](https://github.com/PyClass/PyClassLessons/). That is to say:

* The pace will be fast, with materials available online 24/7
* Frequent repetition of units as we iterate
* Courses are broken down into independent units. You usually won't fall behind
  if you miss a class.

There are, of course, exceptions.

Periodically (about once a month), there will be an "introduction to C++" class.
It will cover some of the basic skills needed to get a much more in depth look
at the language:

* Obligatory "Hello, World"
* Running g++ by hand
* Writing a quick makefile
* Debugging with GDB

It is unfortunate, but C++ programming isn't nearly as widespread as other
languages such as NodeJS, Python, Ruby, etc. Many folks aren't familiar with the
C++ build chain, so these introduction sessions aim to bring everyone up to
speed.

### Class Structure

Each session will use the [Socratic Method](http://www.criticalthinking.org/pages/socratic-teaching/606)

A Socratic questioner should 
1. keep the discussion focused
2. keep the discussion fact based\*
3. stimulate the discussion with probing questions
4. periodically summarize what has and what has not been dealt with and/or
   resolved
5. draw as many students as possible into the discussion.

\* [intellectually responsible](https://en.wikipedia.org/wiki/Intellectual_responsibility) can be
effectively replaced with 'fact based' for our needs.


### The Ideal student

The ideal student for this course can grasp the purpose of the following code:

```c++
#include <iostream>
#include <map>
#include <string>

int main(int argc, char* argv[])
{
  std::string s("noisebridge");
  std::map<char, int> frequencyMap;
  for(auto it = s.cbegin(); it != s.cend(); it++) {
    int freq = 0;
    if (frequencyMap.find(*it) != frequencyMap.cend()) {
      freq = frequencyMap[*it];
    }
    freq++;
    frequencyMap[*it] = freq;
  }

  for(auto it = frequencyMap.begin(); it != frequencyMap.cend(); it++) {
    std::cout << "Frequency of " << (*it).first << ": " << (*it).second << std::endl;
  }

  return 0;
}
```

If the above seems like an indecipherable jumble of line noise, an introductory
session is recommended.

### OS / Environment / Versions

This class will assume the following base environment:

* POSIX
* GCC > 4.8
* C++11
* Make 3.82

Sessions involving building graphical interfaces will require Qt 5.4.

Possible options for getting the above envrionment:

* [Qt Creator](http://www.qt.io/download-open-source/)
* Linux virtual machine
* [POSIX for Windows](http://en.wikipedia.org/wiki/POSIX#POSIX_for_Windows)

Another critical tool is git:

* Windows: http://git-scm.com/download/win    
* Mac: http://git-scm.com/download/mac    
* Linux: (use your package manager)    

## Units

The CPP class hopes to cover these units:

* The obligatory "Hello, World!" in C++
* Debugging with GDB
* Why C++ is the way that it is
* Why the way that it is isn't all that awful
* The wonderful world of STL and Boost
* All the fancy things that C++11 and C++14 brought into the world
* Template metaprogamming
* How non-trivial C++ projects are designed and built
* Writing some NodeJS modules in C++
* Embedded C++ on an AVR chip or similar
* How to not write C in your C++
* Stupid C++ Tricks and Hacks
* How to contribute to a C++ project without being an asshole
