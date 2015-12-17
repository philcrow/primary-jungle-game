# Primary Jungle

A print and play board game where you are a campaign manager trying to win the Iowa Caucus, in an alternate reality where candidates from all parties compete together.

## Printing

All the files you need to print are available as postscript and pdf. Choose the one that works best with your print setup. These instructions assume you will choose pdf.
Replace .pdf with .ps if you are going with postscript.

### Cards

There are two types of cards: candidates and weapons. The weapons will be shuffled. So, print one copy of cardweapons.pdf on card stock, laminate them before cutting them apart.
I have an Amazon Basics Home Laminator which cost about $30 with a set of letter size pouches.

The candidates will not be shuffled. So, print one copy of cardcandidates.pdf on card stock of a different color, and cut them apart.

### Board

I am using a colorful file folder as my board. To make all the elements fit, they need to be trimmed close to their outlines. I used a glue stick to attach them to my board.

### Calendar

Print one copy of calendar.pdf on regular white paper. Trim excess margins.  Glue on one side of the file folder board.

### Other Board Art

On regular white paper, print one copy each of states.pdf, drawdiscard.pdf, and undecided.pdf. Trim and glue on the remaining side of the file folder board.

### Money

There are two kinds of money in Primary Jungle: candidate and Super PAC. The files call these hard and pac. There are two denominations of Super PAC cash
and three of candidate cash. It is nicest if you print each on a separate color. The paper should be light weight (not card stock).

Print one page each of hard5k.pdf and pac500k.pdf.

Print two pages each of hard1k.pdf and pac100k.pdf.

Print four pages of hard10k.pdf.

Cut all money into bills.

### Rules

Print one or more copied of rules.pdf on regular paper. Read and follow these to play the game.

## Additional Hardware Requirements

You also need these items to play the game:

- one calenadar token to sit on the calendar and count down the days to the voting
- 50 white poker chips, 10 red poker chips (or one hundred of some singe counter like pennies)
- Two dice of one color (mine are white) and One die of a different color (mine is blue)
- Tokens to represent field offices, I use small plastic star beads from a hobby store

## Building Files

The game can be built from source files, if you have

- a unix system (mine is a Mac) or familiarity with one
- latex with the tikz and fp packages
- perl 5

### Build Everything

There is a bash script call buildalltex which produces ps and pdf versions of all the files mentioned in the Printing section above.

To rebuild individual files, consult buildalltex. Note that pentagon is a perl script which prints the coordinates of the pentagon for the five person
start location. Adjust its parameters to move it to a different day on the calendar. Paste the result into calendar.tex.

## Key Files

These are the files that build the .ps and .pdf files mentioned above.

- buildalltex             bash script to build all pdf and ps files
- buildonetex             bash script to make one ps and pdf from a latex file
- calendar.tex            latex file which makes the count down calendar for the board
- pentagon                perl script which generates tikz coordinates for the pentagon on the calendar
- generatecards           perl script to turn candidates and weapons files into latex files
- hard10k.tex             latex file for making $10K candidate (hard) cash bills
- hard5k.tex              like hard10k.tex but for $5K
- hard1k.tex              like hard10k.tex but for $1K
- pac100k.tex             like hard10K.tex but for Super PAC $100K bills
- pac500k.tex             like pac100K.tex but for $500K bills
- rules.tex               latex file describing the game play
- candidates              text file naming and describing the candidates
- weapons                 text file describing the cards players play on each turn
- include/libs.tex        list of latex packages to use in latex files
- include/tikzcards.tex   latex helper to build each weapon and candidate card
- include tikzmoney.tex   latex helper to build play money

## License

Copyright (c) 2015 Phil Crow
This worked is licensed under the Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License.

