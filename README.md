# LR4

## Part 1. Subtractor truth table

A | B | C | R | P
---|---|---|---|---
0 | 0 | 0 | 0 | 0
0 | 0 | 1 | 1 | 1
0 | 1 | 0 | 1 | 1
0 | 1 | 1 | 0 | 1
1 | 0 | 0 | 1 | 0
1 | 0 | 1 | 0 | 0
1 | 1 | 0 | 0 | 0
1 | 1 | 1 | 1 | 1

R: (!A&!B&C)|(!A&B&!C)|(A&!B&!C)|(A&B&C) уже минимальная
![R](./screens/part1-1.png)

P: (!A&!B&C)|(!A&B&!C)|(!A&B&C)|(A&B&C) -> (!B&!C)|(A&!B)|(A&!C)
![P](./screens/part1-1.png)

## Part 2. Sifter

 A |  B | C | D | | | | |
 ---|---|---|---|---|---|---|---
 A |  B |  C |  D | 1 | 0 | 0 | 0
 A |  B |  C | !D | 0 | 1 | 1 | 1
 A |  B | !C |  D | 0 | 1 | 1 | 0
 A |  B | !C | !D | 0 | 1 | 0 | 1
 A | !B |  C |  D | 0 | 1 | 0 | 0
 A | !B |  C | !D | 0 | 0 | 1 | 1
 A | !B | !C |  D | 0 | 0 | 1 | 0
 A | !B | !C | !D | 0 | 0 | 0 | 1
!A |  B |  C |  D | 0 | 0 | 0 | 0
!A |  B |  C | !D | 1 | 1 | 1 | 1
!A |  B | !C |  D | 1 | 1 | 1 | 0
!A |  B | !C | !D | 1 | 1 | 0 | 1
!A | !B |  C |  D | 1 | 1 | 0 | 0
!A | !B |  C | !D | 1 | 0 | 1 | 1
!A | !B | !C |  D | 1 | 0 | 1 | 0
!A | !B | !C | !D | 1 | 0 | 0 | 1

1. (!A&!B&!C&!D)|(A&!B&!C&D)|(A&!B&C&!D)|(A&!B&C&D)|(A&B&!C&!D)|(A&B&!C&D)|(A&B&C&!D)|(A&B&C&D) -> (AB)|(AC)|(AD)|(!A!B!C!D)
![1](./screens/part2-1.png)

2. (!A&!B&!C&D)|(!A&!B&C&!D)|(!A&!B&C&D)|(!A&B&!C&!D)|(A&!B&!C&D)|(A&!B&C&!D)|(A&!B&C&D)|(A&B&!C&!D) -> (!BC)|(!BD)|(B!C!D)
![2](./screens/part2-2.png)

3. (!A&!B&!C&D)|(!A&!B&C&!D)|(!A&B&!C&D)|(A&!B&!C&D)|(A&!B&!C&D)|(A&!B&C&!D)|(A&B&!C&D)|(A&B&C&!D) -> (!CD)|(AC!D)|(!BC!D)
![3](./screens/part2-3.png)

4. (!A&!B&!C&D)|(!A&!B&C&D)|(!A&B&!C&D)|(!A&B&C&D)|(A&!B&!C&D)|(A&!B&C&D)|(A&B&!C&D)|(A&B&C&D) -> D
![4](./screens/part2-4.png)
