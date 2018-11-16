Add your answers to the Algorithms exercises here.

a: In order for (n * n)+(n * n)... to equal (n*n*n), you have to add them together n times.
	The loop will need to run only n number of times, so I think the efficiency is pretty good.

b: Yeah, we have a loop. Inside a loop, inside a loop, inside a loop.
	Each time the innermost loop runs, we increase a number by 10.
	Each time n increases by 1, we run each outer loop one additional time, with each
	loop running one less times than the outermost loop.
	Meaning we have both a pretty useless function to count up by a large ammount for
	every small increase in n, but we have a very inneficient one at that.
	
c: All of that recursion is so un-needed. I think this one is probably worse
	than b, as b is just summing a number, this one is calling itself, checking each time if
	bunnies = 0 yet, returning 2, calling itself again subtracting a single digit from the
	number. Actually, this one has to be better than b. It will only run once for each bunny,
	b will just keep running and running with a larger n.
	
2:	Start from the middle floor, as from there if the egg breaks, you know you need to go lower,
	and if the egg remains intact, you need to go higher. From there, you can narrow down your range
	by either going halfway between the top and the middle, or the bottom and the middle. Repeat until
	the floor is figured out, averaging halfway between the current floor and it's previous boundries.
	
	example: 100 story building, eggs stop breaking on floor 23
	
	knowing this strategy, floor 23 will take a while to reach, as 25 barely misses it.
	
	start at 50: egg breaks.
	move to (50/2) = 25: egg breaks.
	move to (25/2) = 12: egg remains intact.
	move to ((25+12)/2) = 18: egg remains intact.
	move to ((25+18)/2) = 21: egg remains intact.
	move to ((25+21)/2) = 23: egg remains intact.
	move to ((25+23)/2) = 24: egg breaks.
	
	at that point, we've moved up one floor and the egg broke, so we know eggs remain intact up to floor 23 in 7 eggs.
	