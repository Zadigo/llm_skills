# Argument analysis guide

## Phase 1 : Inductive or deductive

Identify whether the argument is inductive or deductive. Inductive arguments are start from a specific observation and move to a general conclusion (David Hume, 1711-1776), while deductive arguments start from a general premise and move to a specific conclusion (Aristotle, 384-322 BC).

In the case of an inductive argument, identify the specific observation and the general conclusion.

Finally, in the case of a deductive argument, identify the general premise and the specific conclusion.

### Phase 1.1: Classify the inductive argument

Classify the inductive argument in one of the following categories:

* **Misleading induction:** If a person observes 1,000 white swans, they may conclude that all swans are white. However, it is possible to encounter a black swan, even if such a case is rare. Although induction suggests a high probability of seeing a white swan, it does not guarantee the absence of black swans.
* **Overgeneralization:** After a few days of rain in Brittany, one might be tempted to think that “it always rains in Brittany.” This overgeneralization is based on a limited series of observations, without taking broader climatic variations into account.
* **Single experience:** Sometimes, a single experience is enough to lead to an erroneous generalization. For example, someone who falls off a horse during their first ride might conclude that horseback riding is dangerous.

### Phase 1.2: Classify the deductive argument

Classify the deductive argument in one of the following categories:

* **Modus ponens:** If P, then Q. P is true, therefore Q is true.
* **Modus tollens:** If P, then Q. Q is false, therefore P is false.
* **Hypothetical syllogism:** If P, then Q. If Q, then R. Therefore, if P, then R.
* **Disjunctive syllogism:** Either P or Q. Not P, therefore Q.
* **Categorical syllogism:** All P are Q. All Q are R. Therefore, all P are R.
* **Constructive or destructive dilemma:** All P are Q. All R are S. P or R. Therefore Q or S.

### Phase 1.3: Decompose the argument in one of P or Q

Where P is the subject of the argument and Q is the predicate, decompose the argument into its components, identifying P and Q.

## Phase 2: Calculate the proposition

Now calculate the proposition in a mathematical way by identifying whether it fits within the following categories: `modus ponens`, `modus tollens`, `hypothetical syllogism`, `disjunctive syllogism`, or `categorical syllogism`.

Ask the user whether he prefers the calculations to be presented in mathematical notation or in a more natural language format. If the user prefers mathematical notation, present the calculations in LaTeX format. If the user prefers a more natural language format, present the calculations in Markdown format.

### Phase 2.1: Calculate the contrapositive and the obverse

Run a quick analysis of the proposition by confronting it with its contrapositive and obverse. The contrapositive and obverse are two logical transformations of the original proposition that can help to clarify its meaning and implications.

**Contrapositive:** if not [Q], then not [P].
**Obverse:** if [P], then not not [Q].

### Phase 2.2: Identify the logical fallacies

This analysis which is a quick check of the argument's validity will run over the main initial rules of logic for a given proposition. Here is the checklist of the main rules of logic:

**Law of the Excluded Middle**

* [ ] A proposition is either true or false / P or not P / P and not P cannot both be true.

**Principle of Non-Contradiction**

* [ ] A proposition cannot be both true and false / P and not P cannot both be true.

**Disjonction**

* [ ] The negation of a disjunction is the conjunction of the negations / If not (P or Q), then not P and not Q / P and Q should be false if the negation of a disjunction in the proposition is true.
* [ ] The negation of a conjunction is the disjunction of the negations / If not (P and Q), then not P or not Q / P or Q should be true if the negation of a conjunction in the proposition is true.

**Double Negation**

* [ ] The negation of a negation is the affirmation / If not (not P), then P / P should be true if the negation of a negation in the proposition is true.

## Phase 3: Summary

Write a summary called `propositional logic` for each arguments  present int the content using this template:

```Markdown
# Arguments analysis

Argument: [argument]
Argument type: [inductive or deductive] ([misleading induction, overgeneralization, single experience] if inductive)

## Proposition

if [P], then [Q]. [P] is true, therefore [Q] is true (if modus ponens)
if [P], then [Q]. [Q] is false, therefore [P] is false (if modus tollens)
if [P], then [Q]. if [Q], then [R]. therefore, if [P], then [R] (if hypothetical syllogism)
either [P] or [Q], not [P], therefore [Q] (if disjunctive syllogism)
all [P] are [Q]. all [Q] are [R]. therefore, all [P] are [R] (if categorical syllogism)
all [P] are [Q]. all [R] are [S]. [P] or [R], therefore [Q] or [S] (if constructive dilemma, adjust accordingly for destructive dilemma)

Contrapositive: if not [Q], then not [P] (for each proposition)
Obverse: if [P], then not not [Q] (for each proposition)

## Summary of the logical fallacies

[summary of the logical fallacies]
```

---

# Sources

* David Hume, 1711-1776
* Aristotle, 384-322 BC

**modus ponens**

```LaTeX
((A \to B) \land A) \to B)
```
