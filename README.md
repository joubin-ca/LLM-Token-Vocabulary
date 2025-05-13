# LLMs *generate* text

**A really smart autocomplete, trained on billions of examples!**

What it is actually doing: is predicting the most statistically likely next word.

Uses probability distributions over its vocabulary to predict/decide what comes next.

For example, if you type **"I need a cup of"**, the model might assign:
- P("coffee") = 0.75
- P("tea") = 0.15
- P("water") = 0.05
- P("sunshine") = 0.01

**Coffee** seems to be the most likely next word.

Conditional probability of the next word given the previous words.

The more context the model sees, the better it gets at choosing relevant words. -- **Is this the Attention Part?**

### Token Vocabulary
- A list of all valid tokens (words, subwords, symbols, etc.) and their corresponding token IDs.
- For **GPT-4**, this is around **~100,264 tokens**.

### Merge Rules (Byte Pair Encoding)
- A ranked list of the most common token pairs seen during training.

### Spaces Can Carry Meaning
In natural language, spaces aren’t always just separators. Consider:
- Indentation in code
- Formatting in poetry or screenplays
- Double spaces after a period (some people still do this!)
