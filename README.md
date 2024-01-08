This is a fork of [cushydom88/lottery-problem](https://github.com/cushydom88/lottery-problem), which is targetted at a non-free prolog interpreter.

The code is based on research documented at [YOU NEED 27 TICKETS TO GUARANTEE A WIN ON THE UK
NATIONAL LOTTERY
DAVID CUSHING AND DAVID I. STEWART](https://arxiv.org/pdf/2307.12430.pdf)

## Installation
* Git clone this repository
* Install [SWI-Prolog](https://www.swi-prolog.org/)

## Example Usage
```
 prolog
Welcome to SWI-Prolog (threaded, 64 bits, version 8.4.2)
SWI-Prolog comes with ABSOLUTELY NO WARRANTY. This is free software.
Please run ?- license. for legal details.

For online help and background, visit https://www.swi-prolog.org
For built-in help, use ?- help(Topic). or ?- apropos(Word).

?- ['lottery.pl'].
Warning: /home/shane/GoLang/src/github.com/cushydom88/lottery-problem/lottery.pl:344:
Warning:    Singleton variables: [L]
true.

?- lottery_numbers_in_range(69,71).
%  L(69,6,6,2) = 35
%  L(70,6,6,2) = 35
% Conjecture that  L(71,6,6,2) = 38.
% BadRSTuples [R,S,A,B]:
% [0,0,0,32]
% [0,1,9,33]
% [0,2,18,34]
% [1,0,0,24]
% Delta(I) exceptions [R,S,D2U,D2L,Delta]:
% [0,0,0,0,[3,3,3,3,3]]
true .

?- possible_lottery_number(71, 35, 38).
% Conjecture that  L(71,6,6,2) = 38.
% BadRSTuples [R,S,A,B]:
% [0,0,0,32]
% [0,1,9,33]
% [0,2,18,34]
% [1,0,0,24]
% Delta(I) exceptions [R,S,D2U,D2L,Delta]:
% [0,0,0,0,[3,3,3,3,3]]
```

## Credit:
`ski` a denizen of #programming on libera was instrumental in directing this port to the SWI dialect.
