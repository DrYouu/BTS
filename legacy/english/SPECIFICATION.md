SPECIFICATION.md (documento técnico)

1. Origin (epoch)

Day D0 is defined as the day of birth.

All counters are 0-based.

2. Atomic unit

One day = 24 hours

Internal timekeeping may use standard hours/minutes/seconds for compatibility

3. Decimal hierarchy

Symbol	Name	Size	Description

d	day-in-block	1 day	0–9
B	block	10 days	primary unit
H	hectablock	100 days	optional
K	kiloblock	1000 days	optional

4. Canonical absolute counter

Let:

D = total days since origin

Then:

K = floor(D / 1000)
H = floor((D % 1000) / 100)
B = floor((D % 100) / 10)
d = D % 10

5. Primary human-readable format

B,d

Example:

1325,3

6. Full positional format

K,H,B,d

Example:

13,2,5,3

This is true decimal positional notation.