
<!-- <h4 align="center">
    <img alt="AdalFlow logo" src="docs/source/_static/images/adalflow-logo.png" style="width: 100%;">
</h4> -->

<h4 align="center">
    <img alt="AdalFlow logo" src="https://raw.githubusercontent.com/SylphAI-Inc/LightRAG/main/docs/source/_static/images/adalflow-logo.png" style="width: 100%;">
</h4>


<p align="center">
    <a href="https://colab.research.google.com/drive/1TKw_JHE42Z_AWo8UuRYZCO2iuMgyslTZ?usp=sharing">
        <img alt="Try Quickstart in Colab" src="https://colab.research.google.com/assets/colab-badge.svg">
    </a>
</p>

<h4 align="center">
    <p>
        <a href="https://adalflow.sylph.ai/">All Documentation</a> |
        <a href="https://adalflow.sylph.ai/apis/components/components.model_client.html">Models</a> |
        <a href="https://adalflow.sylph.ai/apis/components/components.retriever.html">Retrievers</a> |
        <a href="https://adalflow.sylph.ai/apis/components/components.agent.html">Agents</a> |
        <a href="https://adalflow.sylph.ai/use_cases/question_answering.html">Trainer & Optimizers</a>
    <p>
</h4>

<p align="center">
    <a href="https://pypi.org/project/adalflow/">
        <img alt="PyPI Version" src="https://img.shields.io/pypi/v/adalflow?style=flat-square">
    </a>
    <a href="https://star-history.com/#SylphAI-Inc/LightRAG">
        <img alt="GitHub stars" src="https://img.shields.io/github/stars/SylphAI-Inc/LightRAG?style=flat-square">
    </a>
    <a href="https://github.com/SylphAI-Inc/LightRAG/issues">
        <img alt="Open Issues" src="https://img.shields.io/github/issues-raw/SylphAI-Inc/LightRAG?style=flat-square">
    </a>
    <a href="https://opensource.org/license/MIT">
        <img alt="License" src="https://img.shields.io/github/license/SylphAI-Inc/LightRAG">
    </a>
      <a href="https://discord.gg/ezzszrRZvT">
        <img alt="discord-invite" src="https://dcbadge.vercel.app/api/server/ezzszrRZvT?style=flat">
    </a>
</p>



<!-- <a href="https://colab.research.google.com/drive/1PPxYEBa6eu__LquGoFFJZkhYgWVYE6kh?usp=sharing">
        <img alt="Try Quickstart in Colab" src="https://colab.research.google.com/assets/colab-badge.svg">
    </a> -->

<!-- <a href="https://pypistats.org/packages/lightrag">
<img alt="PyPI Downloads" src="https://img.shields.io/pypi/dm/lightRAG?style=flat-square">
</a> -->



<h2>
    <p align="center">
     ⚡ The Library to Build and Auto-optimize LLM Applications ⚡
    </p>
</h2>



# Why AdalFlow?

Embracing a design philosophy similar to PyTorch, AdalFlow is powerful, light, modular, and robust.

## Light, Modular, and Model-agnositc Task Pipeline

LLMs are like water; AdalFlow help developers quickly shape them into any applications, from GenAI applications such as chatbots, translation, summarization, code generation, RAG, and autonomous agents to classical NLP tasks like text classification and named entity recognition.

Only two fundamental but powerful base classes: `Component` for the pipeline and `DataClass` for data interaction with LLMs.
The result is a library with bare minimum abstraction, providing developers with *maximum customizability*.

You have full control over the prompt template, the model you use, and the output parsing for your task pipeline.


<p align="center">
  <img src="https://raw.githubusercontent.com/SylphAI-Inc/LightRAG/main/docs/source/_static/images/AdalFlow_task_pipeline.png" alt="AdalFlow Task Pipeline">
</p>


<!-- LLMs are like water; they can be shaped into anything, from GenAI applications such as chatbots, translation, summarization, code generation, and autonomous agents to classical NLP tasks like text classification and named entity recognition. They interact with the world beyond the model’s internal knowledge via retrievers, memory, and tools (function calls). Each use case is unique in its data, business logic, and user experience.

Because of this, no library can provide out-of-the-box solutions. Users must build towards their own use case. This requires the library to be modular, robust, and have a clean, readable codebase. The only code you should put into production is code you either 100% trust or are 100% clear about how to customize and iterate. -->

<!-- This is what AdalFlow is: light, modular, and robust, with a 100% readable codebase. -->


Further reading: [How We Started](https://www.linkedin.com/posts/li-yin-ai_both-ai-research-and-engineering-use-pytorch-activity-7189366364694892544-Uk1U?utm_source=share&utm_medium=member_desktop),
[Introduction](https://adalflow.sylph.ai/), [Design Philosophy](https://adalflow.sylph.ai/tutorials/lightrag_design_philosophy.html) and [Class hierarchy](https://adalflow.sylph.ai/tutorials/class_hierarchy.html).


<!--

**PyTorch**

```python
import torch
import torch.nn as nn

class Net(nn.Module):
   def __init__(self):
      super(Net, self).__init__()
      self.conv1 = nn.Conv2d(1, 32, 3, 1)
      self.conv2 = nn.Conv2d(32, 64, 3, 1)
      self.dropout1 = nn.Dropout2d(0.25)
      self.dropout2 = nn.Dropout2d(0.5)
      self.fc1 = nn.Linear(9216, 128)
      self.fc2 = nn.Linear(128, 10)

   def forward(self, x):
      x = self.conv1(x)
      x = self.conv2(x)
      x = self.dropout1(x)
      x = self.dropout2(x)
      x = self.fc1(x)
      return self.fc2(x)
``` -->
## Unified Framework for Auto-Optimization

AdalFlow provides token-efficient and high-performing prompt optimization within a unified framework.
To optimize your pipeline, simply define a ``Parameter`` and pass it to our ``Generator``.
Whether you need to optimize task instructions or few-shot demonstrations,
our unified framework offers an easy way to **diagnose**, **visualize**, **debug**, and **train** your pipeline.

This [Trace Graph](https://adalflow.sylph.ai/tutorials/trace_graph.html) demonstrates how our auto-differentiation works.

### **Trainable Task Pipeline**

Just define it as a ``Parameter`` and pass it to our ``Generator``.

<p align="center">
  <img src="https://raw.githubusercontent.com/SylphAI-Inc/LightRAG/main/docs/source/_static/images/Trainable_task_pipeline.png" alt="AdalFlow Trainable Task Pipeline">
</p>

### **AdalComponent & Trainer**

``AdalComponent`` acts as the `interpreter`  between task pipeline and the trainer, defining training and validation steps, optimizers, evaluators, loss functions, backward engine for textual gradients or tracing the demonstrations, the teacher generator.

<p align="center">
  <img src="https://raw.githubusercontent.com/SylphAI-Inc/LightRAG/main/docs/source/_static/images/trainer.png" alt="AdalFlow AdalComponent & Trainer">
</p>

# Quick Install

Install AdalFlow with pip:

```bash
pip install adalflow
```

Please refer to the [full installation guide](https://adalflow.sylph.ai/get_started/installation.html) for more details.




# Documentation

AdalFlow full documentation available at [adalflow.sylph.ai](https://adalflow.sylph.ai/):
- [How We Started](https://www.linkedin.com/posts/li-yin-ai_both-ai-research-and-engineering-use-pytorch-activity-7189366364694892544-Uk1U?utm_source=share&utm_medium=member_desktop)
- [Introduction](https://adalflow.sylph.ai/)
- [Full installation guide](https://adalflow.sylph.ai/get_started/installation.html)
- [Design philosophy](https://adalflow.sylph.ai/tutorials/lightrag_design_philosophy.html)
- [Class hierarchy](https://adalflow.sylph.ai/tutorials/class_hierarchy.html)
- [Tutorials](https://adalflow.sylph.ai/tutorials/index.html)
- [Supported Models](https://adalflow.sylph.ai/apis/components/components.model_client.html)
- [Supported Retrievers](https://adalflow.sylph.ai/apis/components/components.retriever.html)
- [API reference](https://adalflow.sylph.ai/apis/index.html)


# AdalFlow: A Tribute to Ada Lovelace

AdalFlow is named in honor of [Ada Lovelace](https://en.wikipedia.org/wiki/Ada_Lovelace), the pioneering female mathematician who first recognized that machines could do more than just calculations. As a female-led team, we aim to inspire more women to enter the AI field.

# Contributors

[![contributors](https://contrib.rocks/image?repo=SylphAI-Inc/LightRAG&max=2000)](https://github.com/SylphAI-Inc/LightRAG/graphs/contributors)

# Citation

```bibtex
@software{Yin2024AdalFlow,
  author = {Li Yin},
  title = {{AdalFlow: The Library for Large Language Model (LLM) Applications}},
  month = {7},
  year = {2024},
  doi = {10.5281/zenodo.12639531},
  url = {https://github.com/SylphAI-Inc/LightRAG}
}
```
