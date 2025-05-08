# AI ML - Tools
> ## 1. What is sklearn with example.

Scikit-learn, often referred to as sklearn, is a free, open-source machine learning library in Python. It provides a wide range of tools for various tasks, including classification, regression, clustering, and dimensionality reduction. 

It's built upon other scientific libraries like NumPy, SciPy, and Matplotlib, and it's designed to be easy to use and integrate with other Python tools. It has pre-built functions for data preprocessing, model training, and evaluation, and a variety of algorithms for different machine learning tasks.

Scikit-learn is commonly used by both beginners and experts in the field of machine learning. It's considered a gold standard for machine learning in Python. Although it's not ideal for tasks like data manipulation or reading, it excels at building machine learning models and is a key part of the Python ecosystem.

#### Key Features:
- Classification (e.g., spam detection)
- Regression (e.g., house price prediction)
- Clustering (e.g., customer segmentation)
- Dimensionality reduction (e.g., PCA)
- Model selection (e.g., cross-validation, grid search)
- Preprocessing (e.g., scaling, encoding)

Here's a **classification example** using **Scikit-learn** to predict whether an email is spam or not using the **Naive Bayes classifier**.

This is a simple demo using fake data for illustration. In a real-world scenario, you'd preprocess actual email content (e.g., using `CountVectorizer` or `TfidfVectorizer`).

---

### 📧 Spam Detection Example (Naive Bayes)

```python
from sklearn.feature_extraction.text import CountVectorizer
from sklearn.naive_bayes import MultinomialNB
from sklearn.pipeline import make_pipeline

# Sample email texts
emails = [
    "Congratulations! You've won a free iPhone",
    "Lowest price for Viagra – buy now!",
    "Hey, are we still meeting tomorrow?",
    "Your invoice for the recent purchase",
    "You have been selected for a prize",
    "Let's grab lunch today"
]

# Labels: 1 = Spam, 0 = Not Spam
labels = [1, 1, 0, 0, 1, 0]

# Create a model pipeline: vectorizer + classifier
model = make_pipeline(CountVectorizer(), MultinomialNB())

# Train the model
model.fit(emails, labels)

# Predict a new email
test_email = ["Win cash now with this limited-time offer!"]
prediction = model.predict(test_email)

print("Spam" if prediction[0] == 1 else "Not Spam")
```

### What's Happening:
1. **CountVectorizer** turns text into a numeric format (bag of words).
2. **MultinomialNB** learns which words are common in spam vs non-spam.
3. We train and predict in one go using a **pipeline**.


> ## 2. What is LangChain with example.

LangChain is an open-source framework that simplifies the development of applications using large language models (LLMs). It provides a standardized way to connect LLMs with external data sources and other tools, allowing developers to build more powerful and context-aware AI applications.

Think of it as a toolkit that helps developers build LLM-powered applications by providing components for data handling, prompt engineering, and model chaining. 

LangChain aims to make it easier for developers to create applications that leverage the capabilities of LLMs, such as chatbots, question answering systems, and text summarization tools. 

- Model-agnostic: LangChain supports various LLMs, including OpenAI's GPT models, Google's LaMDA, and others. 
- Data integration: It provides tools to connect LLMs to external data sources like databases, APIs, and knowledge bases. 
- Prompt engineering: LangChain offers components for designing and fine-tuning prompts to improve LLM performance. 
- Modular design: It allows developers to build complex applications by chaining together different components, such as LLMs, data connectors, and agents. 
- Agent support: LangChain enables the creation of agents that can perform tasks autonomously by using LLMs to make decisions. 

- Use cases: chatsBots, Question answering systems, text summarization, code generations, agent based application

```python
from langchain.chat_models import ChatOpenAI
from langchain.chains import ConversationChain
from langchain.memory import ConversationBufferMemory

# 1. Initialize the model
llm = ChatOpenAI(temperature=0)

# 2. Add memory so it remembers past messages
memory = ConversationBufferMemory()

# 3. Create a conversation chain
conversation = ConversationChain(
    llm=llm,
    memory=memory,
    verbose=True  # Print out the internal steps
)

# 4. Start chatting
response1 = conversation.predict(input="Hi, I'm John!")
response2 = conversation.predict(input="What’s my name?")

print(response1)
print(response2)  # It will remember your name is John
```
> ## 3. What is Hugging Face?

Hugging Face is a community-driven platform that provides pre-trained machine-learning models and tools. It simplifies the process of accessing and training state-of-the-art models in PyTorch, TensorFlow, and JAX, making them accessible to everyone. Often dubbed "the GitHub of Machine Learning," Hugging Face focuses on promoting open-source ML and AI development.

At its core, Hugging Face is more than just a platform, it's a thriving community and machine-learning powerhouse. Providing the essential infrastructure for deploying, running, and training ML models, Hugging Face transforms abstract concepts into live, practical applications. Think of it as a central hub where curiosity meets collaboration, and technology is built with the power of collective intelligence.

Hugging Face offers the following key features:

- Models: Pretrained models for NLP, vision, audio, and more, easily accessible via the Hugging Face Hub.
- Datasets: A wide collection of ready-to-use datasets for training and evaluation.
- Spaces: Interactive apps (built with Gradio or Streamlit) to demo models and ML projects.

Transformers:
- Hugging Face Transformers is a well-liked package for PyTorch and TensorFlow-based natural language processing applications. Hugging Face Transformers offers pre-trained models for a range of natural language processing (NLP) activities, including translation, named entity identification, text categorization, and more. Using pretrained models will reduce your compute costs, carbon footprint, and save your time and resources required to train a model from scratch.

    
    These models support common tasks in different modalities, such as:

- Natural Language Processing: text classification, named entity recognition, question answering, language modeling, summarization, translation, multiple choice, and text generation.
- Computer Vision: image classification, object detection, and segmentation.
- Audio: automatic speech recognition and audio classification.
- Multimodal: optical character recognition, table question answering, information extraction from scanned documents, visual question answering, and video classification.

Tokenizers: Text Transformers
- In the world of NLP, tokenizers play a crucial role as they are like translators for machines. Their job is to turn text into a language that machine learning models can easily grasp. This is super important when dealing with different languages and types of text.
- Think of tokenizers as language architects. They break down text into smaller chunks called tokens—these can be words, subwords, or characters. These tokens become the building blocks that help models understand and create human language.

> ## 4. What is PyTorch and TensorFlow.

PyTorch and TensorFlow are both open-source deep learning frameworks widely used for building and training machine learning and artificial intelligence models, especially neural networks.

> 1. PyTorch:

PyTorch is primarily considered a deep learning framework rather than just a library, though it also functions as a library. While it offers a library of pre-built modules and functionalities, it also provides a higher-level structure and support for building and deploying deep learning models. It is primarily used for developing and training neural networks. PyTorch is known for its flexibility, ease of use, and dynamic computational graphs, which allow for efficient model optimization at runtime.

PyTorch is primarily used for:

1. **Building and Training Neural Networks**  
   It provides tools to define, train, and evaluate deep learning models for tasks like image recognition, natural language processing, speech recognition, and more.

2. **Research and Experimentation**  
   Its dynamic computation graph lets researchers quickly prototype and test new ideas without needing to compile the whole model, making it popular in academia.

3. **Production and Deployment**  
   PyTorch models can be optimized and exported for deployment in real-world applications, including mobile and cloud environments.

4. **GPU Acceleration**  
   It uses GPUs to speed up tensor computations, which is essential for handling large datasets and complex models efficiently.

In short, PyTorch helps developers and researchers create, train, and deploy deep learning AI models easily and effectively.

> 2. TensorFlow:

TensorFlow is a software library for machine learning and artificial intelligence. It can be used across a range of tasks, but is used mainly for training and inference of neural networks. It is one of the most popular deep learning frameworks, alongside others such as PyTorch.

TensorFlow is an open-source software library, primarily used for numerical computation and large-scale machine learning. Developed by Google, it is a popular choice for building and deploying various machine learning models, particularly deep neural networks. TensorFlow provides tools for data preparation, model construction, training, and deployment across different platforms and hardware. 

TensorFlow is used for a wide range of machine learning and artificial intelligence tasks, including:

1. **Building and Training Machine Learning Models**  
   Creating models for tasks like image recognition, natural language processing, speech recognition, and recommendation systems.

2. **Deep Learning Research**  
   Experimenting with neural networks and developing new architectures.

3. **Large-Scale Distributed Training**  
   Training models on big datasets using multiple GPUs or across machines in a cluster.

4. **Production Deployment**  
   Deploying trained models to servers, mobile devices (via TensorFlow Lite), and browsers (via TensorFlow.js).

5. **Dataflow and Computation Graphs**  
   Managing complex workflows with its powerful dataflow graph system, which helps optimize computations.

In essence, TensorFlow helps researchers and developers design, train, and deploy machine learning models efficiently and at scale.

| Aspect                  | PyTorch                                | TensorFlow                           |  
|-------------------------|--------------------------------------|------------------------------------|  
| **Computation Graph**   | Dynamic computation graph (eager execution by default) — easy to debug and flexible | Originally static graph, but now supports eager execution as well |  
| **Ease of Use**          | More Pythonic and intuitive, often preferred for research and prototyping | Slightly steeper learning curve but powerful for production |  
| **Debugging**            | Easier to debug because you can use standard Python debugging tools | Harder with static graph, easier with eager mode |  
| **Deployment**           | TorchScript and ONNX for deployment; PyTorch has improved production tools | More mature deployment options (TensorFlow Serving, TensorFlow Lite, TensorFlow.js) |  
| **Community & Ecosystem**| Strong in academia and research; growing industry adoption | Large ecosystem, widely used in industry and production |  
| **Performance**          | Comparable performance; TensorFlow better for large-scale distributed training | Good for both research and production, excels at distributed setups |  
| **Visualization**        | Uses tools like TensorBoardX, but TensorBoard support is secondary | Includes built-in TensorBoard for powerful model visualization |  
| **Language Support**     | Primarily Python (with C++ backend) | Multiple language APIs (Python, C++, JavaScript, Java, Swift, etc.) |  

> ## 5. What is Matplotlib.

**Matplotlib** is a popular Python library used for creating static, interactive, and animated visualizations in Python. It’s widely used for plotting graphs, charts, histograms, and other types of data visualizations.

### Key Features:
- Produces high-quality 2D plots.
- Supports various plot types: line plots, scatter plots, bar charts, histograms, pie charts, and more.
- Highly customizable (colors, labels, legends, styles).
- Integrates well with other scientific Python libraries like NumPy and Pandas.
- Can be used in scripts, Python shells, web servers, and Jupyter notebooks.
