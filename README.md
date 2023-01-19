# Turing_Machine

## Introduction
 In this project, we tried to implement a Turing Machine to detect the given input language.
Turing Machine is a mathematical model which consists of an infinite length tape divided
into cells on which input is given [1]. After reading an input symbol, it is replaced with
another symbol according to the corresponding rule, its current state is changed, and it
moves from one cell to the right or left. If the TM reaches the final or accept state, the input
string is accepted, otherwise it is rejected. After we detect the input language is accepted or
rejected, program prints the states that has been visited through the process and the result
as accepted or rejected. Our input string is 000111. 

## Methodology
- An input is created in the same directory with the source code file. Input file is
started to read by a Scanner object.

- Scanner object reads the alphabet as “0” and ”1” then the tapes as “0”, “X”, ”Y” and
”1” with the blank symbol “b”.

- Alphabet and tape strings are stored in different arrays with fit_array which is
implemented to add them into a ArrayList of string objects.

- States are read by Scanner reader as “q1”, “q2”, “q3”, “qA” and “qR”. Our initial
state to start is q1 while accept state is qA and the reject state is qR. States are also
added into an ArrayList by fit_array method.

- The number of rules are initialized as number of states, except qA and qR, times
number of tapes. In our case there are 15 rules. Rules are read as tokens and a Rule
object is initialized by creating a Rule class to store its attributes.

- For each String after the rules are input strings. For each input string, we do the
detection process and they are splatted into their characters and stored in an array
of strings to make iterations characters by characters. The rule that contains the
initial state as its current state parameter and the first character of the input string
as its current symbol is the initial rule to be applied in our machine.

- Application processes until we reach accept or reject state. After each rule is
applied, its current state is stored in the array of visited_states. Rules are changing
according to the corresponding current states and current symbols after each
iteration according to the direction of it.

- After detection process is resulted as accepted or rejected, the route that we have
taken are printed as visited_states and the result as well. 
