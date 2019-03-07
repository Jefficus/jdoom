# jdoom

    A simple command-line Python script to generate random dates and test you on your ability to compute the day-of-the-week using John Conway's Doomsday Algorithm.

    Usage: 
        jdoom [options] [quiz]
        jdoom [options] explain DATE
        jdoom -h | --help
        jdoom -V | --version

    Options:
        -a, --after=DATE    Show only dates after DATE 
                            [default: 1800-01-01]
        -b, --before=DATE   Show only dates before DATE 
                            [default: 2199-12-31]
        -c, --config=PATH   Take run-time options from config file
                            [default: /home/jeffs/.jdoomrc]
        -n, --num-dates=N   Number of questions in the quiz.
                            Enter 0 for unlimited. [default: 3]
        -u, --untimed       Do not show how long user needed to compute answer
        -v, --verbose       Display verbose output

    Created 2019 by fantasy author Jefferson Smith (https://creativityhacker.ca)

## Caveat
This is not a tutorial. You'll have to learn the Doomsday algorithm [somewhere else](https://www.timeanddate.com/date/doomsday-weekday.html). That's too much like work. We're just here to do the fun part.

## Example Session
    Enter 'q' to quit.

    Enter the day of the week for each given date.
    Use 0 for Sunday, 1 for Monday, etc. 

    December 25, 1806: 4
    Correct
    (36.2 sec)

    Oct 13 2175: 5
    Correct
    (11.9 sec)

    1872-09-19: 1
    Wrong (3.0 sec)
        The correct answer is 4
        Doomsday for the year was: 5 6 0 0 = 4
        Anchor date for the month is: Sep 5
        Given date is offset from anchor day by: 0
        So anchor date is always a Doomsday (= 4) offset by 0 = 4

Notice that the date prompts are not always in the same format. This keeps you more nimble and able to handle the dates regardless of how they're thrown at you.

## Dependencies

*docoptcfg*: Requires this wonderful package that provides easy arg-parsing, guaranteed up-to-date --help text, local .config files, and environment variable overrides. All for the price of writing a proper help text.
