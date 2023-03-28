---
title: "ILLA Cloud x Hugging Face: Unleash the possibility Of AI Model with Low-Code Tool"
seoTitle: "ILLA Cloud x Hugging Face: Unleash the AI power with LowCode Tool"
seoDescription: "ILLA proudly announces a partnership with Hugging Face, a suite of natural language processing (NLP) tools and services."
datePublished: Mon Feb 13 2023 03:00:39 GMT+0000 (Coordinated Universal Time)
cuid: cle28a3rg0125jlnvh0ki4avk
slug: illa-cloud-x-hugging-face-unleash-the-possibility-of-ai-model-with-low-code-tool
canonical: https://blog.illacloud.com/illa-cloud-x-hugging-face-unleash-the-possibility-of-ai-model-with-low-code-tool/
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1676220163917/f0a220e9-88de-427d-a8e5-0c3661dc7e83.png
tags: ai, nlp, low-code, huggingface, illa

---

> #### ***You can check ILLA’s website here at:*** [***illacloud.com***](http://illacloud.com)
> 
> #### *GitHub page:* [***github.com/illacloud/illa-builder***](http://github.com/illacloud/illa-builder)
> 
> #### *Join Discord community:* [***discord.com/invite/illacloud***](http://discord.com/invite/illacloud)

ILLA proudly announces a partnership with Hugging Face, a suite of natural language processing (NLP) tools and services. They are most well-known for their open-source NLP library, which provides text generation, language translation, and named entity recognition tools. With Hugging Face, ILLA is more productive than before. Our users can do more with AI.

## ILLA Cloud

ILLA Cloud is a low-code development platform with dozens of front-end components and database API integrations. You can use ILLA Cloud to build the front-end interface by dragging and dropping components and connecting to your database or API to complete full-stack development quickly.

## Hugging Face

Hugging Face is the Github of the machine learning community, with hundreds of thousands of pre-trained models and 10,000 datasets currently available. You can freely access models and datasets shared by other industry experts or host and deploy your models on Hugging Face.

Some examples of models available in the Hugging Face library include:

1. BERT (Bidirectional Encoder Representations from Transformers): BERT is a transformer-based model developed by Google for various NLP tasks. It has achieved state-of-the-art results in language understanding and machine translation tasks.
    
2. GPT (Generative Pre-training Transformer): GPT is another transformer-based model developed by OpenAI. It is primarily used for language generation tasks, such as translation and text summarization.
    
3. RoBERTa (Robustly Optimized BERT): RoBERTa is an extension of the BERT model that was developed to improve BERT's performance on various NLP tasks.
    
4. XLNet (eXtraordinary LanguageNet): XLNet is a transformer-based model developed by Google that is designed to improve the performance of transformer models on language understanding tasks.
    
5. ALBERT (A Lite BERT): ALBERT is a version of the BERT model that was developed to be more efficient and faster to train while maintaining good performance on NLP tasks.
    

# What you can do with Hugging Face in ILLA Cloud

In Hugging Face, over 130,000 machine-learning models are available through the public API, which you can use and test for free at [**https://huggingface.co/models**](https://huggingface.co/models). In addition, if you need a solution for production scenarios, you can use Hugging Face's Inference Endpoints, which can be deployed and accessed at [**https://huggingface.co/docs/inference-endpoints/index**](https://huggingface.co/docs/inference-endpoints/index).

ILLA Cloud provides dozens of commonly used front-end components, allowing you to build different front-end interfaces based on your specific needs quickly. At the same time, ILLA offers a connection to Hugging Face, allowing you to quickly connect to the API, send requests, and receive returned data. By connecting the API and front-end components, you can implement the requirement that users can enter content through the front end and submit it to the API. The API returns the generated content to be displayed on the front end.

# How to use Hugging Face in ILLA Cloud

### Step 1: Build UI with components on ILLA Cloud

Based on the expected usage scenario you described, build a front-end interface. For example, you could use input and image components if your product takes in text and outputs an image. If your product takes in text and outputs generated text, you could use input and text components.

The following image is an example of a front-end page for a product that answers questions based on context.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676220558573/6a2aa9e5-9ea9-4433-ba98-7679a7533c89.png align="center")

### Step 2: Create a Hugging Face Resource and config the Actions

Click `+ New` in the action list and select Hugging Face Inference API.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676220575373/03e9f887-f8ef-4793-8688-a14b5e304d9f.png align="center")

Fill in the form to connect to your Hugging Face:

Name: The name that will be displayed in ILLA

Token: Get in your Hugging Face [profile settings](https://huggingface.co/settings/tokens)

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676220645293/e7fe8229-5eeb-4909-a298-a342d244b29b.png align="center")

Confirm the model information in Hugging Face before configuring the actions:

Select a model from [Hugging Face Model Page](https://huggingface.co/models)

Let’s use [`deepset/roberta-base-squad2`](https://huggingface.co/deepset/roberta-base-squad2)as an example. Enter the detail page &gt; click Deploy &gt; Click Inference API

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676220710309/1fc12cea-b085-430a-8cc6-f1fec372d42e.png align="center")

The parameters after `“inputs”` are what you should fill in ILLA.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676220731522/0c690d76-84ac-496d-b57f-d19aaae09f84.png align="center")

In ILLA Cloud, we should fill in the Model ID and Parameter. Taking the above model as an example, the `“inputs”` is a key-value pair, so we can fill in it with key-value or JSON.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676220744359/2346c808-9122-4df6-af5a-e69e74877450.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676220754182/731f117d-0902-4a95-a03f-28c6c2efcddf.png align="center")

And we also support the text input and binary input which can meet all Hugging Face Inference API connections.

### Step 3: Connect actions to components

To pass the user's front-end input to the API, you can use {{ to retrieve data inputted in the component. For example, input2 is the component to input the question and input1 is the component to input context, we can fill `question` and `context` in key, and fill `{{ input.value }}` in value:

```jsx
{
"question": {{input2.value}},
"context": {{input1.value}}
}
```

Before displaying the output data of the Action in the front-end component, we should confirm which field the output of different models is placed in. Still taking `deepset/roberta-base-squad2` as an example, the results are as follows:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676220788349/1ab61392-21b7-47ac-aade-4565bfe05cf3.png align="center")

So we can get the answer with `{{` [`textQuestion.data`](http://textQuestion.data)`[0].answer }}`(the `textQuestion` is the name of the action).

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676220820644/42f09d3d-ce00-46e1-bb4a-d796f7d4e055.png align="center")

### Demo

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676220838940/51c0c3b9-ed14-46ca-9c2f-946711690815.gif align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676220883113/ed83f563-6a5d-49d2-a31c-00d8d98041e7.gif align="center")

## Conclusion

In conclusion, the partnership between ILLA and Hugging Face is set to revolutionize the world of low-code development. With the ability to access over 130,000 pre-trained machine-learning models, and the ease of use provided by ILLA Cloud, developers can now build highly sophisticated applications with incredible speed and efficiency. This partnership offers a complete solution for NLP and AI, making it possible for users to do more with AI than ever before.

> #### ***You can check ILLA’s website here at:*** [***illacloud.com***](http://illacloud.com)
> 
> #### *GitHub page:* [***github.com/illacloud/illa-builder***](http://github.com/illacloud/illa-builder)
> 
> #### *Join Discord community:* [***discord.com/invite/illacloud***](http://discord.com/invite/illacloud)