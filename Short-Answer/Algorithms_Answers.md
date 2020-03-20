#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a) O(n)
There's only 1 execution, so it's linear, but it's going to run each time in the loop.

b) O(n^2)
2 separate yet linear executions. the inside `while` runs it's cycle for every increment of the outer `for`.


c) O(n)
Only one execution inside of a recursion.

## Exercise II

Sounds like a binary sort. 

Let's say that the building is the Empire State in NYC (102 floors) because it's really the only modern skyscraper where you could feasibly **open a window**. Let's also say that, we don't know it, but the first floor that the egg will break is 17.

But we don't know it's 17... so we will wind up having to test both 16 and 17 to get the specific. 

Get your clipboard.

	floor = height = 102
	drop = floor / 2
	notes = object

	while [still dropping]
		OkEgg = results of drop

		if (OkEgg is broken)
			notes{[drop]: broken}
			if notes[drop-1] is Ok
				[stop dropping]
				return "{drop-1} is highest floor"
			drop = drop MINUS (half of difference between this try and last try)		// go halfway DOWN

		else if (OkEgg is Ok)
			notes{[drop]: Ok}
			if notes[drop+1] is broken
				[stop dropping]
				return "{drop} is highest floor
			drop = drop PLUS (half of difference between this try and last try)		// go halfway UP

always round up.
Go to half of height 51 > drop > splat. 
Go down half of 51 = 26 > drop > splat.
Go down half of 26 = 13 > drop > OkEgg is Ok.
Go up half of 13 = 20 > drop > splat
Go down half of difference between this and last try
	20 - 13 = 7, / 2 = 3.5, round up = 4
Go to 20 - 4 = 16 > drop > OkEgg is Ok.
Go up half of difference between this and last try = 1
Go to 16 + 1 17 > drop > splat.

We have a note that says 16 is ok, so 16 is the answer.