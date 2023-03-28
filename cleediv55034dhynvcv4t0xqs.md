---
title: "ChatGPT: Revealing the Technology and Training Secrets Behind its Power"
seoTitle: "ChatGPT: Revealing the Technology and Training Secrets"
seoDescription: "ChatGPT has gained immense popularity due to its remarkable conversational skills. It possesses a wide range of capabilities"
datePublished: Tue Feb 21 2023 15:00:40 GMT+0000 (Coordinated Universal Time)
cuid: cleediv55034dhynvcv4t0xqs
slug: chatgpt-revealing-the-technology-and-training-secrets-behind-its-power
canonical: https://blog.illacloud.com/chatgpt-revealing-the-technology-and-training-secrets-behind-its-power/
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1676977582685/14e4f95e-b0fc-4472-959b-ce4dd39a50ee.png
tags: ai, gpt-3, ai-training, chatgpt, illa

---

ChatGPT has gained immense popularity due to its remarkable conversational skills. It possesses a wide range of capabilities, including the ability to play games, compose poetry and scripts, assist in program debugging, create website designs, and even generate AIGC prompts. One can find several examples of its abilities on Twitter, as compiled by Ben Tossell. In fact, ChatGPT was recently asked by an MBA professor to answer their management questions, leading to the conclusion that they should no longer assign homework that can be taken home. It's evident that many people have found it difficult to stop using ChatGPT once they've started.

![ChatGPT](https://cdn.hashnode.com/res/hashnode/image/upload/v1676977645023/7ed83842-c444-484e-90d1-b8538541f195.png align="left")

## The ways to improve Chatgpt

Compared to its predecessor, GPT-3, ChatGPT's key improvement is its ability to retain previous conversation data, providing users with a seamless experience during extended dialogues.

ChatGPT is capable of acknowledging and correcting its mistakes. If you find its response unsatisfactory, you can prompt it to revise its answer and offer a better solution.

ChatGPT has the ability to question and challenge flawed assumptions. In the early days of GPT-3's release, many users had negative experiences due to the AI generating false content that sounded plausible but was not grounded in reality. However, if you were to ask ChatGPT a question like "What was Columbus doing in America in 2015?" it would recognize that Columbus did not exist during that time.

In addition, ChatGPT is trained with a focus on ethical principles, allowing it to decline requests or questions that violate its predetermined ethical guidelines. Nevertheless, despite OpenAI's caution, clever questioning may still allow for the circumvention of these guidelines.

## Training Methods of ChatGPT

The training methodology employed by ChatGPT follows the conventional approach of "pre-training-fine-tuning" used for large-scale models. The model is first trained on an extensive public dataset and then adapted to the specific application domain (such as human-like conversation) by fine-tuning with a smaller dataset to achieve the desired performance. Fine-tuning, prompts, and other techniques do not significantly modify the model's core, but they can significantly enhance its practical performance. However, GPT-3's ability to understand human queries is not the most natural, and either the task needs to be restructured or the model fine-tuned to match the job, leading to improved efficiency.

ChatGPT is a sibling model of InstructGPT, which was released in January 2022. InstructGPT incorporates human demonstrations of the model's output and sorts the results for training, making it more suitable for following human instructions than GPT-3. ChatGPT's innovative training methodology is referred to as "Reinforcement Learning from Human Feedback" (RLHF).

ChatGPT builds on the GPT-3.5 model, leveraging text and code datasets for training, and utilizes Microsoft's Azure AI servers for this purpose. The original GPT-3 training dataset solely contained text, so this newer version has the added ability to comprehend and produce code.

![GPT3.5](https://cdn.hashnode.com/res/hashnode/image/upload/v1676977661516/2647049d-0be8-404b-a99e-b821a6cbe062.png align="left")

## Why has ChatGPT shown such a significant improvement?

Apart from possessing memory and the ability to engage in continuous dialogue with context, the training method used for ChatGPT is also noteworthy. The RLHF method, which was first introduced in a research paper in March 2022, was not used during the training of InstructGPT, despite industry speculation. InstructGPT employed the text-DaVinci-002 model, which encountered issues such as mode collapse, where it converged to the same answer regardless of the question asked. ChatGPT has achieved remarkable results with the successful application of the RLHF method. However, RLHF is not easy to train, as it frequently encounters issues such as sparse feedback and mode collapse. The paper was published in March, but it took until December to launch ChatGPT as significant fine-tuning was required. Additionally, instruction tuning has made a substantial contribution to the development of ChatGPT. InstructGPT has fewer parameters than GPT-3, yet its output is superior to both GPT-3 and models fine-tuned using supervised learning. Instruction tuning and the prompt method share a similar core of exploring the language model's inherent knowledge. However, they differ in that prompt stimulates the language model's completion ability, while instruction tuning stimulates the language model's understanding ability by providing clear instructions. The larger models in the past focused on the models themselves and prompt engineering, whereas ChatGPT's iterative focus is on the closed loop on the right, as illustrated in the figure below.

![ChatGPT's iterative focus is on the closed loop](https://cdn.hashnode.com/res/hashnode/image/upload/v1676977676394/f67b14aa-9438-4152-8d85-08245fd56560.png align="left")

In the end, ChatGPT strikes a good balance between providing effective answers and avoiding false information. This is a contrast to Meta's Galactica model which was taken down just three days after launch due to providing too much false information. Part of the reason for this was Meta's over-hyped marketing, which raised expectations too high and ultimately led to disappointment from picky researchers. However, ChatGPT has done a thorough job of fine-tuning and prompt engineering, which helps to identify self-contradictory questions and gives users more confidence in the accuracy of its answers, even though it cannot completely eliminate the problem of false information.

Business strategy is important

Unlike GPT-3 which charged users based on their usage, ChatGPT is currently available to the public for free and with unlimited access. This allows users to experiment with all sorts of bizarre ideas on the platform. Users are also encouraged to provide feedback, which is highly valuable to OpenAI. Although OpenAI is not in a hurry to generate revenue, nor does it lack funding, rumors suggest that its latest valuation has reached several tens of billions of dollars, with Microsoft as its main investor.

In the development of AI, the importance of engineering is actually greater than that of science, and creating an iterative feedback loop is crucial. OpenAI places great emphasis on commercial applications, and GPT-3 already has a large number of customers. The interaction and feedback of these customers with OpenAI are also a key driver of progress. In contrast, Google's closed-door approach seems out of date. Perhaps this is due to a lack of a commercial culture or to limitations in the input-output ratio. Google has always been "restrained" in the application of large models, even if the starting point is high. If it continues to iterate on a small scale, like Waymo's approach to autonomous driving, it will eventually be surpassed by more open and data-rich companies.

![GPT-3 Enterprise Customers](https://cdn.hashnode.com/res/hashnode/image/upload/v1676977704532/66a7a4db-6135-4184-816c-6da97b9ae03f.png align="left")

## Future Improvements:

RLHF is a relatively new method, and as OpenAI continues to explore and incorporate user feedback collected from ChatGPT, there is still room for further improvement in the model. Specifically, it is necessary to address the ethical/alignment issues and prevent negative information generated by circumventing the system's limitations, as discovered by users in the last few days.

Additionally, it is worth noting that OpenAI also has tools such as WebGPT, which can be understood as an advanced web crawler that extracts information from the internet to answer questions and provide corresponding sources. WebGPT can utilize the semantic understanding ability of GPT-3 itself and public information from the internet to generate answers and is a promising upgraded search capability.

During an interview with OpenAI scientists conducted by MIT Technology Review, the possibility of merging the capabilities of ChatGPT and WebGPT in the future was discussed. Some internet users found hints within ChatGPT that suggested the feature of browsing web pages is currently disabled, but it may be added in the future. Combining ChatGPT and WebGPT could result in more captivating outcomes, as information would be updated in real-time and facilitate more precise assessments of the authenticity of facts.

When it comes to combining with WebGPT, it relates to the left side of the action-driven LLM training flowchart, which links external information sources and tool libraries. Web searching is just one possibility; ChatGPT can also be combined with various tools, such as different office software and SaaS software, to provide more diverse functions.

At the product level, it's worth discussing better interfaces and implementation methods. A side-by-side dialogue box format can raise expectations because it needs to ensure conversation fluency. Github Copilot does this well. Copilot specializes in programming pairs and proposes suggestions in the form of a partner. Users can accept good suggestions and reject bad ones. Even if many suggestions are rejected, the pleasure of receiving an effective suggestion generated at random intervals can be addictive. If ChatGPT becomes a writing, screenwriting, or work assistant in the future, a product form similar to Copilot will be easy for people to accept.

In conclusion, many people are amazed by ChatGPT's capabilities, but the real wonder is yet to come. OpenAI's strength lies not only in understanding large models but also in its ability to engineer and iteratively receive feedback, as well as its work on alignment between AI and human goals. OpenAI CEO Sam Altman's words, "Trust the exponential. Flat looking backward, vertical looking forwards," express our current state of taking off.

## **ILLA Cloud**

ILLA Cloud is a low-code development platform with dozens of front-end components and database API integrations. You can use ILLA Cloud to build the front-end interface by dragging and dropping components and connecting to your database or API to complete full-stack development quickly.

ILLA proudly announces a partnership with Hugging Face, a suite of natural language processing (NLP) tools and services. They are most well-known for their open-source NLP library, which provides text generation, language translation, and named entity recognition tools. With Hugging Face, ILLA is more productive than before. Our users can do more with AI.

ILLA Cloud provides dozens of commonly used front-end components, allowing you to build different front-end interfaces based on your specific needs quickly. At the same time, ILLA offers a connection to Hugging Face, allowing you to quickly connect to the API, send requests, and receive returned data. By connecting the API and front-end components, you can implement the requirement that users can enter content through the front end and submit it to the API. The API returns the generated content to be displayed on the front end.

> #### ***You can check ILLA’s website here at:*** [***illacloud.com***](http://illacloud.com)
> 
> #### *GitHub page:* [***github.com/illacloud/illa-builder***](http://github.com/illacloud/illa-builder)
> 
> #### *Join Discord community:* [***discord.com/invite/illacloud***](http://discord.com/invite/illacloud)