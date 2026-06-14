---
share: true
created: 2026-01-19T15:20
updated: 2026-06-14T15:28
title: Yêu cầu
---
Từ các [Đề bài](./%C4%90%E1%BB%81%20b%C3%A0i/index.md), nhóm [Kiến trúc sư](../../S%E1%BB%95%20tay/Vai%20tr%C3%B2/Ki%E1%BA%BFn%20tr%C3%BAc%20s%C6%B0.md) sẽ thiết kế, triển khai các [Yêu cầu chức năng](./Y%C3%AAu%20c%E1%BA%A7u%20ch%E1%BB%A9c%20n%C4%83ng/index.md) và [Yêu cầu phi chức năng](./Y%C3%AAu%20c%E1%BA%A7u%20phi%20ch%E1%BB%A9c%20n%C4%83ng/index.md).


---
## Computer Specification
A specification of the machines on which the software must run. The machine need not be hardware-for some software this section might simply be a pointer to a language reference manual.

## Input/Output Interfaces
A specification of the interfaces that the software must use in order to communicate with the outside world.

## Specification of Output Values
For each output, a specification of its value in terms of the state and history of the system's environment.

## Timing Constraints
For each output, how often, or how quickly, the software is required to recompute it. 

## Accuracy Constraints
For each output, how accurate it is required to be.

## Likely Changes
If the system is required to be easy to change, the requirements should contain a definition of the areas that are considered likely to change. You cannot design a system so that everything is equally easy to change. Programmers should not have to decide which changes are most likely.

## Undesired Event Handling
The requirements should also contain a discussion ,of what the system should do when, because of undesired events, it cannot fulfill its full requirements. Most requirements documents ignore those situations; they leave the decision about what to do in the event of partial failures to the programmer.
