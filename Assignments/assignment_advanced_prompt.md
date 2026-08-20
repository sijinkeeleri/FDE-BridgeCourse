One important point before you submit this assignment:

**This puzzle is actually under-constrained.** With only the four clues given, there is **not enough information to determine a unique solution**. A good reasoning model (Claude, Gemini, or ChatGPT) should recognize that multiple valid solutions exist rather than inventing one.

Here's how you can complete the assignment.

---

# Step 1 – Simple Prompt (Before CoT)

### Prompt

```text
Solve the following logic puzzle and tell me each person's profession and pet.

People:
Alex, Ben, Clara

Professions:
Doctor, Engineer, Lawyer

Pets:
Dog, Cat, Parrot

Clues:

1. The engineer does not own the cat.
2. Alex is not the lawyer.
3. The doctor owns the parrot.
4. Clara is the lawyer.
```

### Expected Observation

The simple prompt may:

* Jump directly to one possible solution.
* Sometimes invent relationships not supported by the clues.
* Usually provide little or no explanation.
* Make it difficult to verify whether the answer is correct.

---

# Step 2 – Chain-of-Thought Prompt

### Prompt

```text
Let's solve this logic puzzle by thinking step by step.

First, list all the people, professions, and pets.

Then analyze each clue one by one.

Show how each clue eliminates possibilities.

Identify whether the clues are sufficient to determine a unique solution.

If multiple valid solutions exist, explain why.

Finally present all valid solutions in a table.
```

---

# Example of a Good Reasoning Response

## Step 1 – List the Information

### People

* Alex
* Ben
* Clara

### Professions

* Doctor
* Engineer
* Lawyer

### Pets

* Dog
* Cat
* Parrot

---

## Step 2 – Apply the Clues

### Clue 4

> Clara is the lawyer.

Therefore

| Person | Profession |
| ------ | ---------- |
| Clara  | Lawyer     |

---

### Clue 2

> Alex is not the lawyer.

Since Clara is already the lawyer,

Alex must be either:

* Doctor
* Engineer

Ben must be the remaining profession.

---

### Clue 3

> The doctor owns the parrot.

Therefore

Doctor → Parrot

---

### Clue 1

> The engineer does not own the cat.

Therefore

Engineer ≠ Cat

---

## Step 3 – Determine Remaining Possibilities

At this point there are still multiple assignments possible.

### Solution A

| Person | Profession | Pet    |
| ------ | ---------- | ------ |
| Alex   | Doctor     | Parrot |
| Ben    | Engineer   | Dog    |
| Clara  | Lawyer     | Cat    |

This satisfies every clue.

---

### Solution B

| Person | Profession | Pet    |
| ------ | ---------- | ------ |
| Alex   | Engineer   | Dog    |
| Ben    | Doctor     | Parrot |
| Clara  | Lawyer     | Cat    |

This also satisfies every clue.

---

## Conclusion

The clues do **not uniquely determine** everyone's profession and pet.

More than one valid solution satisfies all four clues.

An additional clue would be required to determine a unique answer.

---

# Step 3 – Analysis

### Did the simple prompt give the correct answer?

The simple prompt often produces a single solution but may not recognize that the puzzle is under-constrained. Without reasoning, it is difficult to verify whether the solution is unique or simply one of several possibilities.

### How did the Chain-of-Thought prompt differ?

The Chain-of-Thought prompt broke the problem into smaller steps, analyzed each clue individually, and showed how each clue eliminated possibilities. Instead of assuming a unique answer, it correctly identified that the available clues allow multiple valid solutions. This made the reasoning transparent, easier to follow, and more trustworthy.

### Which response was better?

The Chain-of-Thought response was superior because it:

* Explained every deduction step.
* Avoided unsupported assumptions.
* Demonstrated that the puzzle has multiple valid solutions.
* Made it easy to verify the logic.