Project #10 Smart Battleship
CS 1210 – Fall 2025
Nathania Jothiraj

# Requirements
Restate the problem specifications in your own words

I had to create a program that made the computer make more smart, memory-based moves. I was required to edit two functions. The goal was to give the computer “basic intelligence” instead of it choosing random moves.

# Design
How did you attack the problem? What choices did you make in your design, and why? 

For the updateMemory function, I chose to just follow along on the state graph and work from there. After I understood what each struct did, I was able to understand that function fairly quickly. Implementing it was far more challenging, as I found myself adding more to each block of code, when I thought I was done with that specific block. I chose to use a lot of if/else if statements as I had lots of conditions that needed to be fulfilled. I updated the structs in the program as needed. 

The smartMove function took me a long time to understand. At first, I 


# Implementation
Outline any interesting implementation details.


# Testing
Explain how you tested your program, enumerating the tests if possible.
Explain why your test set was sufficient to believe that the software is working properly,
i.e., what were the range of possibilities of errors that you were testing for.

I tested especially for when the computer tried to go over the edges. Before, I explained how my pattern was North, South, East, West. 


# Outside Help
Did you get help from anyone else on this project? Document their contribution to your learning. 

I got some help from Chase and Professor Knoerr.

# AI Use
How did you use Generative AI in this project?

I used AI for quick searches on topics. For example, I asked it for a refresher on push_back when using strings. I also searched up an ASCII table on google.

# Summary/Conclusion
Present your results. Did it work properly? Are there any limitations? 

The code works not as well as I would have liked. Sometimes it works perfectly. It goes in the order I want it to (North, South, East, West) in search mode. However, other times, it can skip a spot when it was supposed to hit a ship there. I would think there are a bunch of limitations. 


# Lessons Learned
List any lessons learned. What might you have done differently if you were going to attack this again.

I learned to 



# Time Spent
Approximately how many hours did you spend on this project?

It took a long time. I think it took more than 15 hours.

