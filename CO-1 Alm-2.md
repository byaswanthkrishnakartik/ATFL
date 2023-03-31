## You

How many states (minimum) are possible to design DFA for the following language? L = {Set of
strings of 0's and 1's such that the number of 0’s is even}
A. 4
B. 3
C. 2
D. 1

## AI

We can design a DFA for the given language L = {Set of strings of 0's and 1's such that the number of 0’s is even} with 2 states. 

Let q0 be the initial state, which represents an even number of 0's seen so far. From q0, if we see a 0, we remain in the same state q0 because seeing another 0 will still result in an even number of 0's seen. If we see a 1, we transition to state q1 because seeing a 1 doesn't change the parity of the number of 0's seen so far.

From state q1, if we see a 0, we transition back to state q0, because seeing a 0 again will revert the parity back to even. If we see a 1, we remain in state q1, because it doesn't change the parity.

Finally, we make the only final state q0, because any string reaching this state will have an even number of 0's seen so far.

Therefore, the minimum number of states required to design DFA for this language is 2.
Hence, the answer is option C.

## You

What is the difference between DFA and NFA? 1. NFA allows 0, 1 or more transitions and DFA
exactly one transition 2. NFA allows Epsilon transitions and DFA does not allow Epsilon transitions
3. DFA allows Dead state where as NFA does not allow dead state
A. Option 1 only
B. Option 1 & 2
C. Option 3 only
D. All the options are correct

## AI

Option B. Option 1 & 2 are the correct differences between DFA (Deterministic Finite Automaton) and NFA (Nondeterministic Finite Automaton). 

DFA has exactly one transition from each state on every input symbol, whereas NFA can have 0, 1 or more transitions from each state on a particular input symbol. 

NFA allows Epsilon (ε) transitions which allow it to move without reading any input symbol. In contrast, DFA does not allow ε transitions.

However, option 3 is incorrect as both DFA and NFA allow dead states. A dead state is a non-accepting state in which no further transitions are defined for any input symbols.

## You

When do you say that a language L Regular?
A. L is accepted by FA
B. L is accepted by PDA
C. L is accepted by both PDA and FA
D. None of the above
ANSWER:

## AI

Option A. A language L is regular if it can be accepted by a Finite Automaton (FA), which is a type of state machine that accepts a string of symbols as input and determines whether the input string belongs to the language or not. 

A PDA (Pushdown Automaton) is a more powerful type of state machine that accepts context-free languages, but not all regular languages can be accepted by a PDA. Therefore, option B and C are incorrect.

Hence, the correct answer is Option A: L is accepted by FA.

## You

The smallest FA which accepts the language {x/length of x is divisible by 3} has
A. 2 states
B. 3 states
C. 4 states
D. 5 states
ANSWER

## AI

Option B. 

The language {x/ length of x is divisible by 3} can be recognized by a deterministic finite automaton (DFA) with 3 states, as follows:

- The DFA will have 3 states, say q0, q1, and q2.
- The starting state will be q0, which is also the only accepting state.
- For each input symbol in the alphabet, say 'a', the transition function will be defined as: 
  - δ(q0, a) = q1,
  - δ(q1, a) = q2,
  - δ(q2, a) = q0.
- This means that for every group of three consecutive symbols in the input string, the DFA will transition from its current state to the next state. If the final state after reading the entire input string is the accepting state q0, then the input string is accepted by the DFA.

It can be shown that no smaller DFA exists to recognize this language. Hence, the smallest FA which accepts the language {x/length of x is divisible by 3} has 3 states.

Therefore, option B is correct.

## You

What is the minimum number of states in the NFA accepting the language {01, 012}
A. 4
B. 5
C. 3
D. 2

## AI

Option C. 

The language {01, 012} contains two strings - "01" and "012".
To design an NFA for this given language, we can start by creating a state diagram with the minimum number of states possible to recognize both these strings.

Here is one possible way to design the NFA:

- Start with the initial state q0.
- When the input symbol is '0', move to state q1.
- When the input symbol is '1', move to state q2. This is an accepting state because it ends with "01".
- From state q1, when the input symbol is '1', move to state q3.
- From state q3, when the input symbol is '2', move to state q4. This is also an accepting state because it ends with "012".
- Any other input symbol should lead to a dead state q5.

Visual representation of the NFA:
```
(q0) --0--> (q1) --1--> (q2)*
               |
               V
             (q3) --2--> (q4)*
               |
               V
             (q5)
```
Note: The states marked with "*" are final states.

This NFA has only 3 states - q0, q1 and q3, which is the minimum number of states required to accept the language {01, 012}. Therefore, option C is correct.

## You

Transition function maps.
A. Σ * Q -> Σ
B. Q * Q -> Σ
C. Σ * Σ -> Q
D. Q * Σ -> Q

## AI

Option A.

The transition function maps each state of the finite automaton to a new state based on the input symbol. The domain of the transition function is the Cartesian product of the set of input symbols and the set of states, i.e., Σ * Q. The range of the transition function is the set of states, i.e., Q.

Therefore, the correct option is A, which represents the mapping as Σ * Q -> Σ.

## You

δ*(q,ya) is equivalent to .
A. δ((q,y),a)
B. δ(δ*(q,y),a)
C. δ(q,ya)
D. independent from δ notation
ANSWER:

## AI

Option C.

The notation δ*(q, ya) represents the state that the finite automaton will be in after reading the string ya from state q. Since y is a string, we need to consume each symbol of y until we reach the end of the string. Therefore we can represent δ*(q, ya) as δ(q, y[0]) followed by δ(δ(q, y[0]), y[1]), and so on until we read the entire string y.

So, δ*(q,ya) is equivalent to applying the transition function δ repeatedly for each symbol of y and then applying it once more with the final symbol a. Therefore, the correct option is C, which represents this as δ(q,ya).

## You

Number of final state require to accept Φ in minimal finite automata.
A. 1
B. 2
C. 3
D. None of the mentioned
ANSWER:

## AI

Option A.

The language phi (Φ) represents the empty language, which contains no strings. The minimal finite automaton for the empty language is a single state without any transitions. Since there are no strings to be accepted in this language, this final state can also act as the initial state. Therefore, we need only one final state in the minimal finite automaton that accepts Φ. 

Hence, the correct option is A, i.e., 1.

## You

Two finite state machines are said to be equivalent if they
A. have same number of states
B. have same number of edges
C. have same number of states and edges
D. recognize same set of tokens
ANSWER:

## AI

Option D.

Two finite state machines are said to be equivalent if they recognize the same set of tokens (i.e., the same language). This means that for any given input sequence, both machines will either accept or reject it. 

The number of states and edges in a finite state machine does not necessarily indicate equivalence. For example, two machines could have the same number of states and edges, but their transitions may lead to different accept/reject outcomes for certain inputs. Alternatively, two machines could have a different number of states and edges, but still recognize the same set of tokens. 

Therefore, option D is the correct answer.

## You

Languages of a automata is
A. If it is accepted by automata
B. If it halts
C. If automata touch final state in its life time
D. All language are language of automata

## AI

The answer is A. 

The language of an automata is the set of all strings or sequences of symbols that are accepted by the automata. In other words, it is the set of all inputs for which the automata reaches a final state when started in its initial state.

Option B is not correct because whether or not an automata halts does not determine the language of the automata. An automata may halt without accepting any input, or it may not halt at all.

Option C is also not correct because touching the final state of an automata only indicates acceptance of an input and not the entire language recognized by the automata.

Option D is not correct either because not all sets of strings can be recognized by an automata. There exist languages that cannot be recognized by any automaton such as the language of all Turing machines that halt on every input.