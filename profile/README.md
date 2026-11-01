# Secnd

An AI lab building models that decide or ask for help.

A decision model takes a situation and a list of options, then returns one option with a
probability. To trust software to act alone, you need proof of when it's safe. So we measure how
many decisions a model can handle alone, with proof, per dollar.

## Ren

Ren is our first model. It has 396M parameters and it's trained once. It can work from option names
alone and gets better with a few examples.

[Weights on Hugging Face](https://huggingface.co/Secnd-AI/ren/tree/v1.1.0), under CC BY-SA 4.0.

At our 99% gate, with one seed and full history:

- **MTOP:** Ren answered 21.0% alone and made 1 error in 923 answers.
- **BANKING77:** Ren answered 0% alone, because it couldn't prove it was safe. That gap is the research problem we're working on.

## Secnd

Secnd is our first product, and it isn't available yet. It will connect to the tools where work
happens, starting with GitHub. When it's sure, it acts for you. When it isn't, it asks.
