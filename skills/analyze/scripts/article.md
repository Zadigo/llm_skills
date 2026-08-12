# Article analysis guide

## Phase 1: Get the introduction

Read the introduction of the article to understand the main topic and purpose of the content. This will help you to identify the key points and arguments that will be discussed.

## Phase 2: Get all the main titles

Read through the article and identify level 1 titles excluding subtitles.

## Phase 3: Get the main paragraphs under each main title

Under each level 1 titles dentify the main paragraphs. You should focus on identifying the main *linking words* in each paragraphs.

### Phase 3.1: Introduction linking words

identify a linking word that starts a paragraph. If ther is none, then skip this phase.

* First, firstly, first of all, to begin with, to start with, at the beginning, in the beginning, in the first place, first and foremost

### Phase 3.3: Example introduction linking words

Identify linking words that introduces a proof or an example that supports an argument:

* Introducing examples: as follows, as exemplified by, above all, especially, for example, for instance, like, mainly, namely, notably, particularly/in particular, this includes/including, such as

### Phase 3.4: Conclusion linking words

Indentify linking words that start a conclusion:

* All in all, at last, at the end (of), finally, generally, in conclusion, in the end, on the whole, overall, to conclude, to sum up

### Phase 3.5: Other types of linking words

* Sequencing: First (ly), second (ly), third (ly), then, next, also, another point is that, additionally, eventually, finally, furthermore, moreover, subsequently

## Phase 4: Identify the plan used by the article

Generally, the type of interrogation used by the problematic statement will determine the plan used by the article. Here are the types of plans that you will consider:

**By concept**

This plan tries to explain all related concepts to the theme of the article:

1. Economic
2. Social
3. Political

**Inventory/Categorization**

This plan lists the arguments and examples that support the theme as an inventory:

1. Argument 1
2. Argument 2
3. Argument 3

**Dialectical**

This plan presents the arguments and counterarguments to the theme of the article:

* Thesis: The article presents an argument in favor of the theme.
* Antithesis: The article presents a counterargument against the theme.
* Synthesis: The article presents a conclusion that reconciles the thesis and antithesis.

**Comparative**

This plan compares arguments and examples from different perspectives or contexts:

1. A vs B
2. C vs D
3. Conclusion: Differences between the two groups of arguments: A - B and C - D

Or, alternatively, the plan can compare the arguments and examples from different perspectives or contexts:

1. Similarities between A and B
2. Differences between A and B
3. Conclusion: Reformulation of the thesis into a new thesis that takes into account the similarities and differences between A and B

**Analytical**

This plan analyzes the arguments and examples from different perspectives or contexts:

* Problems
* Causes
* Solutions

### Step 5: Provide a summary of the article

Once you have identified these elements, you can summarize the document using this template, providing it to the user for verification and feedback.

```
# Introduction

[introduction]

# Problematic Statement

[problematic statement]

Concept: [concept]
Theme: [theme]
Context: [context]

# Plan

[plan]

# [bloc title]

Linking word: [linking word]
Argument n°[number]: [argument]
Proof n°[number]: [proof]

# Conclusion

[conclusion]
```

## Phase 4: Verify with the user

Ask the user if the summary is accurate and if they would like to make any changes. If the user wants to make changes, ask them to provide specific feedback on what they would like to change. Once the user is satisfied with the summary, you can proceed to the next step.

---

**Introduction**

Summarize the introduction of the article or document in a few sentences. This should include the main topic and purpose of the content.

**Problematic statement**

The problematic statement should be clear and concise and should follow this structure:

* *theme* + *context [geographical scope] and [time frame]*

So for example, if the article is about the benefits of exercise, you might summarize the statement as follows:

* What are the benefits of exercise for individuals in the United States in 2021?

Now depending on the article you might have to adjust the structure of the question to fit the context of the article. For example on the theme of mental health, you might summarize the statement as follows:

* How can exercise help to improve mental health for individuals in the United States in 2021?
* Does exercise have a positive impact on mental health for individuals in the United States in 2021?

**Plan**

Make a best gues for the plan used. If you are not sure you can ask the user to provide feedback on the plan used. The plan should be clear and concise and should follow the structure of the plans provided in Step 5.

For instance, if the article is based on an inventory plan, you might summarize the plan as follows:

1. Argument 1: Exercise improves physical health
2. Argument 2: Exercise improves mental health
3. Argument 3: Exercise improves social health

You do not need to be exhaustive because the main idea is to help the user quickly understand the structure of the article or document.

**Concept or scope**

It is the global concept or scope of the article or document. It should be a single word that captures the essence of the content. For example, if the article is about the benefits of exercise, the concept could be "health" or "fitness".

**Bloc title**

Represents the title of the section under which the argument is located

**Linking word**

The linking word if available that starts the argument if avaiable for example *first of all*.

**Assumption**

The schematical assumption made by the argument. Follow the pattern modus tolens, modus ponens, hypothetical syllogism, disjunctive syllogism or categorical syllogism. So for example, or an argument that states that "sports is great for health because it increases ", the assumption template would be "IF A (sports) THEN B (health), A (sports) then B (health)". You must represent the logic in KaTex by choosing one of the LaTex below. By default, if the user has not specified a format, use the subscript or visual valuation method.

*Subcript method*

```LaTeX
\cfrac{A_{\text{x}} \to B_{\text{y}}, \neg B_{\text{y}}}{\therefore \neg A_{\text{x}}}
```

*Underbrace Method*

```LaTeX
\cfrac{\underbrace{A}_{\text{x}} \to \underbrace{B}_{\text{y}}, \neg B}{\therefore \neg A}
```

*Explicit Valuation Method*

```LaTeX
\cfrac{A \to B, \neg B}{\therefore \neg A}
\quad \text{where } 
\begin{cases} 
A \in \text{x} \\ 
B \in \text{y} 
\end{cases}
```

*Predicate Logic Notation*

```LaTeX
\cfrac{\forall x (T(x) \to C(x)), \neg C(s)}{\therefore \neg T(s)}
```
