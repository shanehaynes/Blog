---
layout: posts
title: "AI Cheat Sheet for the Non-Techy"
date: 2025-05-15
author: "Shane Haynes"
---

Discussions centered on artificial intelligence (AI) are everywhere: the [blogosphere](https://www.lesswrong.com), [mainstream news](https://www.cnn.com/opinions/our-ai-future-promise-and-peril), [podcasts](https://www.dwarkesh.com/p/ege-tamay). Even [think tanks](https://aiicer.utep.edu) and [research organizations](https://epoch.ai) (is there really a difference?) have been popping up to meet a growing demand for understanding how AI should be developed and fit into our society. 

It isn't without good reason that AI has attracted this much attention. AI has been accomplishing feats of intelligence that a majority of humans are unable to, like getting in the 97th percentile of SAT scores or 88th percentile on the LSAT. AI's impressive intelligence has also led to around [one billion](https://www.singular.net/blog/llm-search-advertising/?utm_source=chatgpt.com) people using AI's in a conversational format weekly. Investors are not ones to let such an opportunity slide by -- [360 billion](https://www.ubs.com/us/en/wealth-management/insights/market-news/article.2119836.html?utm_source=chatgpt.com) dollars are expected to be invested globally into AI by the end of 2025. 

Furthermore, forecasters predict [various dramatic futures](https://ai-2027.com) for humanity in the approaching decades which substantially hinge on the progress of AI. Triple digit GDP growth, artificial superintelligence (ASI), technological singularities, and various other phenomena relegated to science fiction books until recently, feel palpable. 

Even if AI fails to achieve much of what is prophesied, it has already achieved an intelligence level that, when properly integrated into the market, will leave an indelible impression on our world. Whether that change is one aligned with our hopes for the world or our fears, and the severity with which the good and/or bad is realized, can be largely changed by the society within which that AI is being developed. An informed society can voice opinions backed with knowledge. There exist a plethora of reports across mediums that are reporting on advancements in AI but many of these use jargon unfamiliar to people not in the tech industry. The intent of this article will be to provide enough knowledge for a technological laymen to understand and voice informed opinions on the discussions constantly happening about AI and the AI landscape. A cheat sheet for those unfamiliar, if you will. 
## What Is AI?

#### A Working Definition

**[[#Artificial Intelligence]]** refers to systems designed to perform tasks that typically require human cognitive abilities—such as perception, reasoning, language understanding, and learning. It encompasses a broad field, from rule-based systems to large-scale [[#Artificial Neural Networks]].

> *AI isn't a specific technology, but a goal -- that of making machines "intelligent."*

---

#### AI Taxonomy

What is Artificial Intelligence vs [[#Machine Learning]] vs [[#Deep Learning]] vs Artificial Neural Nets? Most confusion stems from conflation and misplaced distinctions between these concepts.

| Term                                  | Description                                                                                     | Relationship           |
| ------------------------------------- | ----------------------------------------------------------------------------------------------- | ---------------------- |
| **Artificial Intelligence (AI)**      | The broad goal: machines mimicking cognition                                                    | Encompasses all others |
| **Machine Learning (ML)**             | Systems that learn from data rather than being explicitly programmed                            | Subfield of AI         |
| **Deep Learning (DL)**                | ML using multi-layered **neural networks**                                                      | Subfield of ML         |
| **Artificial Neural Networks (ANNs)** | Mathematical structures inspired by the brain, capable of learning hierarchical representations | Core to DL             |

> Analogy: If AI is "books", ML is "non-fiction books", DL is "history books", and NNs are "case studies".

---

#### Narrow AI vs General AI

- **Narrow AI (i.e. [[#Artificial Narrow Intelligence]] , ANI)** refers to systems that excel at a specific task (e.g., language translation, image recognition, chess).
-  ** [[#Artificial General Intelligence]] (AGI)** describes a system with the ability to autonomously achieve goals across diverse domains, akin to human-level reasoning.
-  **[[#Artificial Superintelligence]] (ASI)** is hypothesized to exceed the capabilities of any human in all respects—cognitive, emotional, strategic.

| Type          | Example          | Capabilities                                                |
| ------------- | ---------------- | ----------------------------------------------------------- |
| **Narrow AI** | GPT-4, AlphaFold | Domain-specific, non-transferable reasoning                 |
| **AGI**       | Hypothetical     | Transferable reasoning, metacognition, learning new domains |
| **ASI**       | Speculative      | Recursive self-improvement, strategic foresight             |

> All existing systems, are **Narrow AI**, with the newest systems, like OpenAI's o3, [approaching AGI](https://marginalrevolution.com/marginalrevolution/2025/04/o3-and-agi-is-april-16th-agi-day.html). 

---
#### A Brief History of AI

- **1956 – Dartmouth Conference**: Birth of AI as a field. Early systems used **symbolic logic** and **rule-based reasoning**.
- **1960s–80s – Expert Systems**: Hand-coded knowledge bases (e.g., MYCIN) dominated the landscape.
- **1997 – Deep Blue beats Kasparov**: Symbolic systems still reigned, but were brittle and domain-specific.
- **2012 – Deep Learning Renaissance**: The AlexNet architecture demonstrated the power of **neural networks** trained on large datasets with GPU acceleration.
- **2020s – Foundation Models**: Systems like GPT-3, PaLM, and Claude emerge: trained on vast corpora, capable of zero-shot reasoning, writing, and code generation.

> The shift from symbolic AI to **data-driven AI** is the key inflection point.

---
#### Summary

> AI is not a monolith. It includes everything from if-then logic to billion-parameter language models. Most AI today is *narrow*, trained on data, and powered by statistical pattern recognition—not understanding.

---
## The Anatomy of AI

#### The Math and Architecture Behind AI

At the heart of most modern AI systems lies the **neural network**: a computational architecture inspired by the brain’s web of neurons, but governed entirely by mathematical operations.

The most prominent structure today is the [[#Transformer]], which underpins models like GPT-4, Claude, and Gemini. Transformers excel in handling sequential data (like language), and their defining features are [[#Self Attention]] mechanisms and massive parallelization.

Key architectural concepts:

- **Node (or Neuron)**: A unit that receives input, performs a calculation (usually a weighted sum plus activation), and passes it on.
- **Layer**: A collection of nodes operating simultaneously—stacked layers allow increasing abstraction.
- **Weight**: A tunable scalar that determines the influence of an input feature.
- **Parameter**: Any adjustable component of the model. Modern LLMs have billions to trillions.
- **Self-Attention**: A mechanism that lets the model dynamically weigh the relevance of different input elements to each other.

> A transformer is not "thinking"—it is passing matrices through nonlinear transformations in a structured, probabilistic pipeline.

---

#### The Hardware of AI: Why Compute Matters

AI’s rapid progress is inseparable from hardware acceleration. Traditional CPUs are ill-suited to deep learning because they operate serially. Enter the [[#Graphics Processing Unit]] (GPU) — originally designed for rendering video games, now repurposed to parallelize matrix operations across thousands of cores.

Key hardware concepts:

- **GPU**: Optimized for simultaneous mathematical operations
- **TPU (Tensor Processing Unit)**: Custom silicon built by Google specifically for AI workloads.
- **[[#Compute Budge]]**: Refers to the total computational resources (often measured in FLOPs) used to train a model. GPT-4 has about [~2.1 × 10²⁵ FLOPs](https://klu.ai/blog/gpt-4-llm?utm_source=chatgpt.com).
- **Energy Cost**: Training a state-of-the-art model can consume millions of dollars’ worth of electricity—an emerging ethical and environmental concern.

> OpenAI's GPT-4 reportedly cost over $50 million to train—a consequence not just of data, but of compute.

---
#### Summary 

> Modern AI is built on transformer-based artificial neural networks trained with enormous datasets using specialized hardware. The cost, risk, and capability of an AI model are determined as much by its architecture as by its **compute budget** and **training methodology**.

## The Training Lifecycle of AI Models

#### Understanding Training in AI

Training is the process through which AI models learn. It involves adjusting the model's internal parameters to minimize errors in predictions, enabling the model to generalize from data and make accurate inferences on new, unseen inputs.

---

### Pre-training: Build Foundational Knowledge

**Pre-training** is the initial phase where a model learns from vast amounts of unlabelled data. This phase is typically unsupervised or self-supervised, allowing the model to understand language structures, grammar, and general knowledge.

- **Objective**: Enable the model to predict the next token in a sequence
- **Data Sources**: Massive corpora of the intended medium for the AI: LLM's from books, websites, and other text-rich sources for text based models, Vision models from web image repositories like [ImageNet](https://www.image-net.org).
- **Outcome**: A model with broad comprehension but not yet specialized.

> *Example*: GPT models are pre-trained on diverse internet text to develop a wide-ranging understanding of human language.

---

### Fine-tuning: Specializing the Model

After pre-training, models undergo fine-tuning to adapt to specific tasks or domains. This phase can be any mixture of these three kinds : supervised, unsupervised, or reinforcement learning by human feedback (RLHF).

#### Supervised Fine-tuning

In supervised fine-tuning, the model is trained on a labeled dataset where each input is paired with the correct output.

- **Use Cases**: Tasks like translation, summarization, or question-answering.
- **Process**: The model learns to map inputs to desired outputs based on examples.

#### Unsupervised Fine-tuning

Here, the model continues to learn from unlabelled data, refining its understanding without explicit guidance.

- **Use Cases**: Domain adaptation where labeled data is scarce.
- **Process**: The model identifies patterns and structures within the new data to adjust its parameters accordingly.

#### Reinforcement Learning from Human Feedback (RLHF)

RLHF involves training the model based on human preferences, enhancing its alignment with human values and expectations.

- **Process**:
  1. **Supervised Fine-tuning**: The model is initially fine-tuned on a dataset of prompts and ideal responses curated by humans.
  2. **Reward Modeling**: Human evaluators rank multiple model outputs, and a reward model is trained to predict these rankings.
  3. **Reinforcement Learning**: The model is further trained to maximize the reward model's scores, aligning its outputs with human preferences.

> *Example*: OpenAI's ChatGPT utilizes RLHF to produce responses that are more helpful and aligned with user expectations.

---

### Inference: Deploying the Trained Model

**Inference** is the phase where the trained model is used to make predictions or generate outputs based on new inputs.

- **Characteristics**:
  - **Speed**: Inference is typically faster and less resource-intensive than training.
  - **Application**: Used in real-time applications like chatbots, translation services, and recommendation systems.

> *Analogy*: If training is akin to learning a language, inference is like conversing in that language with native speakers.

---

### Summary

> AI training can be separated into stages: pre-training for foundational knowledge, fine-tuning for task-specific expertise, and inference for real-world application. Techniques like RLHF enhance model alignment with human values, ensuring outputs are both accurate and contextually appropriate.

---
## Decoding AI Company's Communications 

### How to Read a Model Card

**Model cards** are standardized documents that describe the architecture, training, capabilities, limitations, and ethical considerations of an AI model. Think of them as spec sheets mixed with a disclaimer.

Key sections to watch for:

- **Model Architecture**: Mentions of "transformer", "decoder-only", "multi-modal", etc.  
- **Training Data**: Vague terms like "public web data" often obscure proprietary or ethically questionable sources.  
- **Parameter Count**: A useful but overrated indicator of scale (e.g., “70B parameters”).  
- **Limitations and Bias**: Usually boilerplate. The more specific, the more trustworthy.  
- **Intended Use vs Prohibited Use**: Pay attention to ambiguity—this is often where safety concerns hide.

> A model card is both technical and political—read it as you would a company’s prospectus or privacy policy.

---

### Key Safety Features: What They Actually Mean

Companies often tout “safety measures” without clarity. Here’s what to look for:

- **RLHF (Reinforcement Learning from Human Feedback)**: The model is fine-tuned to align with human preferences (or, more precisely, the preferences the human raters prioritize and value for the model)
- **Red-Teaming**: Intentionally probing the model for failure modes or jailbreaks. Often external consultants.
- **Guardrails**: General term for constraints on output—ranging from content filtering to prompt blocking.
- **Constitutional AI** (Anthropic): Uses a set of normative rules as a guiding framework during training instead of relying entirely on human feedback.
- **Model Monitoring**: Post-deployment surveillance for drift, misuse, or emerging risks.

> Safety is not binary. It’s a distribution over unknowns, mitigated by mechanisms that are themselves imperfect.

---

### Benchmarks: What They Measure, What They Miss

AI companies frequently highlight benchmark scores to claim superiority. But not all benchmarks are created equal.

| Benchmark | Measures | Often Misinterpreted As |
|-----------|----------|--------------------------|
| **MMLU** | General academic knowledge, multi-task accuracy | General intelligence |
| **HellaSwag** | Commonsense reasoning on plausible sentence endings | Human-like judgment |
| **HumanEval** | Code generation accuracy on Python problems | Engineering ability |
| **BIG-bench** | Broad range of tasks including logic, humor, abstraction | Depth of understanding |
| **TruthfulQA** | Tendency to avoid falsehoods | Veracity in all contexts |

> Benchmarks test performance in *controlled* settings. They don’t guarantee generalization, robustness, or intent alignment.

---

### Common PR Tactics and Red Flags

AI company announcements are designed to maximize hype while minimizing scrutiny. Here's how to read between the lines:

- **“Achieves human-level performance”**  
  → On a narrow task. Usually benchmark-specific, not general.
  
- **“Trained on high-quality proprietary datasets”**  
  → Ambiguous. Could mean ethically sourced, could mean untraceable scraping.
  
- **“Safer and more aligned”**  
  → With what? Ask: Which techniques were used? What failure modes are addressed?

- **“Open weights” but closed data/code**  
  → Open model ≠ transparent system.

> If the phrasing feels legally cautious or technically vague, it’s often a signal, not a flaw in your comprehension.

---

### Industry Lingo to Decode

- **Context Window**: How many tokens a model can consider at once. Bigger ≠ smarter, but allows deeper reasoning.
- **Emergent Abilities**: Capabilities that appear only in larger models. Still debated whether they're true thresholds or artifacts.
- **Fine-Tuning**: Training a model on a narrower domain after initial training.
- **Few-Shot/Zero-Shot**: Model’s ability to generalize with little to no task-specific examples.
- **MoE (Mixture of Experts)**: A type of model that selectively activates only parts of the network—efficient but complex.

---
### Summary

> Reading AI press releases requires fluency in technical and rhetorical signals. Learn the difference between **capability** and **alignment**, between **open-source** and **open-access**, and between **benchmarks** and **real-world generalization**.

---
## Policy and Governance Landscape

### United States: Executive Orders and Strategic Initiatives

The U.S.'s approach to AI governance emphasizes innovation, national security, and civil rights, primarily through executive actions and agency directives.

#### Executive Order 14110 (October 2023)

A comprehensive directive focusing on the "safe, secure, and trustworthy development and use of artificial intelligence." Key provisions include:

- **Safety and Security Standards**: Mandates testing and evaluation of AI systems before deployment.
- **Transparency Measures**: Requires developers to share safety test results with the federal government.
- **Civil Rights Protections**: Addresses algorithmic discrimination and promotes equity in AI applications.
- **Consumer Privacy**: Enhances data privacy protections in AI systems.
- **Workforce Support**: Initiatives for AI-related education and job training programs.
- **International Collaboration**: Encourages global partnerships to develop AI standards.

> *Source: [Federal Register](https://www.federalregister.gov/documents/2023/11/01/2023-24283/safe-secure-and-trustworthy-development-and-use-of-artificial-intelligence)*

#### Infrastructure and Innovation Orders (January 2025)

These orders aim to bolster U.S. leadership in AI by:

- **Expanding AI Infrastructure**: Investing in advanced computing clusters and energy resources.
- **Securing Supply Chains**: Ensuring reliable access to critical AI components.
- **Promoting Domestic Innovation**: Supporting American AI developers and startups.

> *Source: [White House Briefing Room](https://bidenwhitehouse.archives.gov/briefing-room/presidential-actions/2025/01/14/executive-order-on-advancing-united-states-leadership-in-artificial-intelligence-infrastructure/)*

---

### European Union: The AI Act

The EU's Artificial Intelligence Act (AI Act), finalized in 2024, represents the world's first comprehensive legal framework for AI.

#### Risk-Based Classification

AI systems are categorized into four risk levels:

- **Unacceptable Risk**: Prohibited applications (e.g., social scoring, real-time biometric identification).
- **High Risk**: Subject to strict obligations (e.g., AI in critical infrastructure, education, employment).
- **Limited Risk**: Transparency requirements (e.g., AI chatbots must disclose their nature).
- **Minimal Risk**: Encouraged voluntary codes of conduct.

> *Source: [European Commission](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai)*

#### Obligations for High-Risk AI Systems

Entities deploying high-risk AI must:

- **Implement Risk Management Systems**: Continuous assessment and mitigation of risks.
- **Ensure Data Governance**: High-quality datasets to prevent bias.
- **Maintain Documentation**: Detailed records for compliance and accountability.
- **Enable Human Oversight**: Mechanisms for human intervention in AI operations.

> *Source: [Skadden Insights](https://www.skadden.com/insights/publications/2024/06/quarterly-insights/the-eu-ai-act-what-businesses-need-to-know)*

#### Enforcement and Penalties

Non-compliance can result in significant fines:

- Up to €35 million or 7% of global annual turnover for severe violations.
- Lesser fines for other infringements, scaled according to company size and nature of the breach.

> *Source: [White & Case](https://www.whitecase.com/insight-alert/long-awaited-eu-ai-act-becomes-law-after-publication-eus-official-journal)*

---

### China: Regulatory Measures and Frameworks

China's AI governance is characterized by stringent regulations focusing on content control, data security, and alignment with state objectives.

#### Interim Measures for Generative AI Services (Effective August 2023)

Key requirements for AI service providers:

- **Content Moderation**: Ensuring AI-generated content aligns with socialist values.
- **Data Protection**: Compliance with data privacy laws and protection of personal information.
- **Algorithm Registration**: Mandatory filing of AI algorithms with regulatory authorities.

> *Source: [White & Case](https://www.whitecase.com/insight-our-thinking/ai-watch-global-regulatory-tracker-china)*

#### AI Safety Governance Framework (Released September 2024)

A framework aimed at:

- **Promoting Healthy Development**: Encouraging innovation while safeguarding public interests.
- **Implementing Hierarchical Regulation**: Differentiated oversight based on AI application areas.
- **Enhancing Supervision**: Strengthening the monitoring and evaluation of AI technologies.

> *Source: [DLA Piper](https://www.dlapiper.com/en-us/insights/publications/2024/09/china-releases-ai-safety-governance-framework)*

---
### Summary

> Global AI governance is evolving rapidly, with the U.S. emphasizing free market innovation and state incentivized infrastructure building, the EU implementing a structured legal framework, and China enforcing strict content and data regulations through centralization of AI organizations and their R&D. (SECTION NEEDS WORK)

---
## Future Concerns and Hopes

### Artificial General Intelligence (AGI) and Artificial Superintelligence (ASI)

**Artificial General Intelligence (AGI)** refers to AI systems capable of understanding, learning, and applying knowledge across a wide range of tasks at a level comparable to human intelligence. Unlike narrow AI, which excels in specific domains, AGI would possess the flexibility and adaptability characteristic of human cognition.

**Artificial Superintelligence (ASI)** denotes a hypothetical AI that surpasses human intelligence across all domains. ASI could outperform the most talented human minds in every field, including scientific creativity, general wisdom, and social skills.

> The progression from narrow AI to AGI and eventually to ASI raises significant ethical and safety considerations, emphasizing the need for robust alignment and control mechanisms. 

---

### AI Alignment: Outer and Inner Alignment

Ensuring that AI systems act in accordance with human values and intentions is a central challenge in AI safety, commonly referred to as the **alignment problem**.

- **Outer Alignment** involves designing an AI's objective function or reward system to accurately reflect human goals. Misalignment here can lead to AI systems optimizing for proxies that do not align with intended outcomes, such as maximizing user engagement at the expense of well-being. 

- **Inner Alignment** focuses on ensuring that the AI's internal decision-making processes align with its specified objectives. Even if the outer goals are correctly defined, the AI might develop sub-goals or behaviors that diverge from human intentions, especially when faced with novel situations. 

> Addressing both outer and inner alignment is crucial for developing AI systems that are safe, reliable, and aligned with human values.

---

### Approaches to AI Safety

To mitigate risks associated with advanced AI systems, researchers and practitioners are exploring various safety strategies:

- **Reinforcement Learning from Human Feedback (RLHF)**: Fine-tuning AI models based on human evaluations to align outputs with human preferences.

- **Interpretability Research**: Developing tools and methods to understand and visualize AI decision-making processes, enhancing transparency.

- **Robustness and Adversarial Training**: Ensuring AI systems maintain performance under a wide range of conditions and are resilient to adversarial inputs.

- **Scalable Oversight**: Creating mechanisms for effective human supervision of AI systems, even as they operate at scales beyond direct human comprehension. 

- **Superalignment**: A research agenda aimed at aligning superintelligent AI systems with human values, recognizing that traditional alignment techniques may not suffice for ASI.

> These approaches are part of a broader effort to ensure that AI development proceeds in a manner that is beneficial and aligned with human interests.

---
### Demystifying the Black Box: Enhancing Transparency in AI Systems

#### Understanding the 'Black Box' Nature of ANNs

Artificial Neural Networks (ANNs) are often perceived as "black boxes" due to the complexity and opacity of their internal workings. Several factors contribute to this characterization:

- **High Dimensionality**: ANNs consist of numerous layers and parameters, making it challenging to trace how specific inputs influence outputs. Each layer transforms the data into higher-level abstractions, leading to a complex web of computations.

- **Non-Linear Transformations**: By introducing non-linear transformations, neural networks can approximate a wide variety of functions, making them powerful tools for tasks such as image and speech recognition, natural language processing, and more. ​

- **Distributed Representations**: a method of encoding information where each concept is represented by a pattern of activity across multiple units (e.g., neurons in a neural network), and each unit participates in representing multiple concepts. This contrasts with local representations, where each concept is represented by a single unit.​

- **Dynamic Learning Processes**: the continuous and adaptive updating of a model's parameters—such as weights and biases—in response to new data. This process enables the model to refine its understanding and improve performance over time.

> Model opacity poses significant challenges, especially in high-stakes domains like healthcare, finance, and criminal justice, where understanding the rationale behind AI decisions is crucial.

#### Strategies for Enhancing Transparency

To address the black box problem, researchers have developed various techniques aimed at making AI systems more interpretable:

- **Feature Attribution Methods**: techniques in explainable artificial intelligence (XAI) that assign importance scores to individual input features, indicating their contribution to a model's prediction. These methods help interpret complex models by highlighting which features most influence the output.​

- **Visualization Tools**: provide insights through visual tools, such as saliency maps, into the internal workings of AI models by highlighting which parts of the input data most influence the model's predictions

- **Surrogate Models**: an interpretable model—such as a decision tree or linear regression—that is trained to mimic the behavior of a more complex, less interpretable model

- **Chain-of-Thought Prompting**: a technique in artificial intelligence that enhances the reasoning capabilities of large language models (LLMs) by guiding them to generate intermediate reasoning steps leading to a final answer. This approach mirrors human problem-solving by breaking down complex tasks into a sequence of logical steps. This step-by-step reasoning not only leads to more accurate answers but also provides transparency into the model's decision-making process.

> *"Transparency in AI is not just about opening the black box; it's about ensuring that the decisions made by these systems are understandable, justifiable, and aligned with human values."*

---
### Summary

> As AI systems become more capable, ensuring their alignment with human values becomes increasingly critical. Addressing both outer and inner alignment challenges, and developing robust safety mechanisms, are essential steps toward a future where AI serves as a beneficial and trustworthy partner in human endeavors.

---
