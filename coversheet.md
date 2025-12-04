Project #10 Smart Battleship
CS 1210 – Fall 2025
Nathania Jothiraj

# Requirements
Restate the problem specifications in your own words

I had to create a program that made the computer make more smart, memory-based moves. I was required to edit two functions. Instead of choosing random moves all the time, the computer needed to use information from previous hits, misses, and sunk ships to make smarter decisions. The goal was to give the computer “basic intelligence” instead of it choosing random moves.

# Design
How did you attack the problem? What choices did you make in your design, and why? 

I ended up using a ton of if and else if statements because there are just so many different cases the computer goes through depending on the mode it’s in (RANDOM, SEARCH, DESTROY) and whether the shot was a hit, a miss, or a sink.
My whole approach was just to slowly update each struct value right after the computer got the shot result. I kept thinking I was done with a piece of logic, and then when I tested it, something else wouldn’t work right, so I had to go back and add more conditions. It kept happening over and over.
The smartMove function took me way longer to wrap my head around. At first I had no idea how to turn the computer’s internal row/column numbers into the actual grid format like “C4”. Once I finally got that part, the rest started to fall into place. 

# Implementation
Outline any interesting implementation details.

Although I eventually scrapped this part, one interesting part was converting the internal board coordinates into a move like “C4” or “H10.” I used ASCII math to calculate the row letter and built the column number manually so that it worked for both one-digit and two-digit numbers.

Another interesting part was managing the fireDist and fireDir values. In SEARCH mode, the computer tries directions in a specific order (for me, North, South, East, West). In DESTROY mode, it extends in one direction until it misses, and then flips to the opposite direction. Getting this right required careful updates to fireDist and properly resetting values when switching states.


# Testing
Explain how you tested your program, enumerating the tests if possible.
Explain why your test set was sufficient to believe that the software is working properly,
i.e., what were the range of possibilities of errors that you were testing for.

I tested especially for cases where the computer tried to go over the edges of the board. Before debugging, I noticed that sometimes my SEARCH pattern (North, South, East, West) would hit a border and then behave incorrectly. I tested what happened when the computer started searching next to the top row, bottom row, and edges.
I also tested what happened when the computer got multiple hits on a ship. whether it continued correctly in DESTROY mode or whether it reset to RANDOM mode too early. Sometimes it worked perfectly, and other times it skipped a spot or extended too far in one direction.

I think they were sufficient for testing the possibilities of errors I would get.


# Outside Help
Did you get help from anyone else on this project? Document their contribution to your learning. 

I got some help from Chase and Professor Knoerr.

# AI Use
How did you use Generative AI in this project?

I used AI for quick searches on topics. For example, I asked it for a refresher on push_back when using strings. I also searched up an ASCII table on google.

# Summary/Conclusion
Present your results. Did it work properly? Are there any limitations? 

My code works, but not as well as I would have liked. Sometimes everything works exactly how it’s supposed to: the computer checks directions in order during SEARCH mode and successfully destroys ships by extending in the correct direction. However, in some situations, it still skips a space or returns to RANDOM mode earlier than expected.
There are definitely some limitations. The logic is complicated, and even small mistakes in updating direction or distance can make the computer behave incorrectly. But overall, the computer is much smarter than before and uses memory effectively most of the time.



# Lessons Learned
List any lessons learned. What might you have done differently if you were going to attack this again.

I learned that reading a state graph is extremely important, especially when working with multiple modes like RANDOM, SEARCH, and DESTROY. I also learned that debugging logical problems is different from debugging syntax problems



# Time Spent
Approximately how many hours did you spend on this project?

It took a long time. I think it took more than 15 hours.








