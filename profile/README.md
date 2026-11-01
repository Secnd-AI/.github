# Secnd

We're a research lab building models that decide or ask for help.

Most AI models are built to write. A decision model is built to choose: give it a situation and a
list of options, and it returns one option with a probability.

Accuracy can't tell you when software is safe to act without a person. Proof can. So the number we
care about is how many decisions a model can handle alone, with proof, per dollar.

## Ren

Ren is our first model. It has 396M parameters and was trained once, on 422,906 rows, for about $129
of compute. It can work from option names alone and gets better with a few examples.

| Test | No examples | 8 examples | Answered alone at our 99% gate |
| --- | ---: | ---: | --- |
| MTOP | 76.0% | 92.4% | 21.0%, with 1 error in 923 answers |
| BANKING77 | 69.0% | 89.9% | 0% |

Ren answered nothing alone on BANKING77 because it couldn't prove it was safe. Closing that gap is
the research problem we're working on now.

Ren isn't the most accurate model out there. Jev scores 79.7% on BANKING77 with no examples. The gate
results cover one seed with full history, and no real business has run Ren yet.

- [Weights on Hugging Face](https://huggingface.co/Secnd-AI/ren/tree/v1.1.0), under CC BY-SA 4.0
- [Code](https://github.com/Secnd-AI/ren)
- [All results, with comparisons and limits](https://github.com/Secnd-AI/ren/tree/main/docs/results)

## Secnd

Secnd is our first product, and we haven't built it yet. It will connect to the tools where work
happens, starting with GitHub, then Slack, email and Notion. It will learn how you decide. When it's
sure, it acts for you. When it isn't, it asks.

With consent, real decisions from Secnd will train the next Ren.

## Next

1. Build the GitHub connector.
2. Test Ren against Jev on real decisions.
3. Close the BANKING77 gap, so Ren can prove more of its answers are safe.
