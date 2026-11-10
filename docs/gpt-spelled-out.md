
# Quick summary
This markdown has been used to noting down everything when learning through Karpathy's video.

# Reading and exploring data

Tiny Shakespeare dataset is used in this repo. Lets start with getting all unique characters that appear in this text.

```python
chars = sorted(list(set(text)))
vocab_size = len(chars)

print(''.join(chars)) 
# This include all special characters, both uppercase and lowercase (sorted as well) 
print(vocab_size) # 65 possible characters that model can see or emit.
```

# Tokenization

Moving to tokenizing the input text, "tokenize" means converting the raw text as a string to a some sequences of integers according to a notebook or a vocabulary of possible characters.

Get this piece of code as an example:

```python
stoi = { ch:i for i, ch in enumerate(chars) }
itos = { i:ch for i, ch in enumerate(chars) }
encode = lambda s: [stoi[c] for c in s ] # encoder: take a string, return a list of integers

decode = lambda l: ''.join([itos[i] fro i in l]) # decoder 

```


