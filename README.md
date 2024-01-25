
Welcome to Cybertech Services, where innovation meets excellence in software solutions. We are a dynamic software company committed to delivering cutting-edge technology, tailored to meet the unique needs of our clients. With a team of skilled professionals, we strive to redefine possibilities in the digital landscape, ensuring your business stays ahead in the ever-evolving tech world. Partner with us for transformative, customized software solutions that propel your success.## mamba-minimal

Simple, minimal implementation of Mamba in one file of PyTorch.

Featuring:
* Equivalent numerical output as official implementation for both forward and backward pass
* Simplified, readable, annotated code

Does NOT include:
* Speed. The official implementation is heavily optimized, and these optimizations are core contributions of the Mamba paper. I kept most implementations simple for readability.
* Proper parameter initialization (though this could be added without sacrificing readability)

## Demo

See [demo.ipynb](demo.ipynb) for examples of prompt completions.

```python
from model import Mamba
from transformers import AutoTokenizer

model = Mamba.from_pretrained('state-spaces/mamba-370m')
tokenizer = AutoTokenizer.from_pretrained('EleutherAI/gpt-neox-20b')

generate(model, tokenizer, 'Mamba is the')
```
> Mamba is the world's longest venomous snake with an estimated length of over 150 m. With such a large size and a venomous bite, Mamba kills by stabbing the victim (which is more painful and less effective than a single stab of the bite)

150 meters... 🫢 scary!

## References

The Mamba architecture was introduced in [Mamba: Linear-Time Sequence Modeling with Selective State Spaces](https://arxiv.org/abs/2312.00752) by [Albert Gu](https://twitter.com/_albertgu?lang=en) and [Tri Dao](https://twitter.com/tri_dao?ref_src=twsrc%5Egoogle%7Ctwcamp%5Eserp%7Ctwgr%5Eauthor).

The official implementation is here: https://github.com/state-spaces/mamba/tree/main
