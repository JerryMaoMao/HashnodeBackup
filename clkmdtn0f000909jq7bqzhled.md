---
title: "Fostering Imagination with ILLA Cloud: Crafting an Enchanting Animal Generator"
seoTitle: "AI Innovation with ILLA Cloud: Hugging Face Integration"
seoDescription: "Discover limitless creativity using ILLA Cloud and Hugging Face. Embrace animal generators, image generation, and furry diffusion AI"
datePublished: Fri Jul 28 2023 09:29:26 GMT+0000 (Coordinated Universal Time)
cuid: clkmdtn0f000909jq7bqzhled
slug: fostering-imagination-with-illa-cloud-crafting-an-enchanting-animal-generator
canonical: https://blog.illacloud.com/fostering-imagination-with-illa-cloud-crafting-an-enchanting-animal-generator/
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1690536242309/ab70f99e-8778-41b0-bd3e-cf25fc345335.jpeg
tags: ai, cloud, opensource, low-code, illa

---

Welcome to the world of ILLA Cloud, an open-source low-code platform that empowers you to transform your wildest ideas into reality. With its intuitive drag-and-drop builder and a plethora of pre-built components, ILLA Cloud is a playground for both seasoned developers and novices, bridging the gap between technical expertise and creative visions.

![](https://blog.illacloud.com/content/images/2023/07/illa-33.png align="left")

## Fostering AI Innovation with Hugging Face Integration: A World of Endless Possibilities

Step into a realm of AI-driven imagination and innovation with the seamless Hugging Face integration within ILLA Cloud. Embrace the power of state-of-the-art [AI models](https://blog.illacloud.com/unleashing-creativity-building-ai-anime-generators-with-illa-cloud/), including the revolutionary animal generator wheel, Auto Image, Img2img, and the remarkable Roberta base model. Unlock the magic of Hugging Face's AI prowess, blending effortlessly with ILLA Cloud's ecosystem to open doors to boundless opportunities.

![](https://blog.illacloud.com/content/images/2023/07/huggingface-7.jpeg align="left")

### The Enchanting Animal Generator Wheel: A Window to Creativity

Discover the enchanting animal generator wheel, a captivating feature that sparks creativity with every spin. Unleash the magic of [AI-driven](https://blog.illacloud.com/unleashing-creativity-building-ai-anime-generators-with-illa-cloud/) animal fusions and delightful hybrids, breathing life into the realm of mythical creatures and dreamlike beings. Witness the fascinating transformation as furry diffusion AI and stable diffusion upscaler combine their powers within the animal generator wheel, bringing imaginations to life.

### Harnessing the Hugging Face Trainer: Empowering AI Innovators

Leverage the power of the Hugging Face trainer, a versatile tool that empowers AI innovators to train and fine-tune [AI models](https://blog.illacloud.com/unleashing-creativity-building-ai-anime-generators-with-illa-cloud/) effortlessly. Delve into the world of bad prompt embedding and witness the transformative impact it has on AI-generated content. Experience the wonders of Anything V3, a feature that brings dreams to reality with unparalleled precision, and the awe-inspiring dreamlike-photoreal V.2 model that blurs the line between imagination and realism.

### Unraveling the Potential of AI Image Generation: Auto Image and Img2img

Embark on a captivating journey of [AI image generation](https://blog.illacloud.com/unleashing-creativity-building-ai-anime-generators-with-illa-cloud/) with Auto Image and Img2img, as ILLA Cloud empowers you to craft mesmerizing visuals. From stunning artistic renditions to photorealistic masterpieces, Auto Image and Img2img showcase the versatility of AI-driven creativity.

### The Power of Random Animal Generator Wheel

Embrace the unexpected with the random animal generator wheel. Witness the joy of generating unique animal combinations that spark the imagination and bring a smile to your face. From whimsical camel generators to captivating animal fusions, the random animal generator wheel unleashes the creative genius within you.

### Creating Animal Hybrids: A Journey of Imagination

Dive into the realm of animal hybrid generators as ILLA Cloud transforms your vision into reality. Discover the thrill of bringing together two distinct creatures to create a mesmerizing animal hybrid. Whether it's a majestic lion-eagle hybrid or a mystical dragon-tiger combination, the animal hybrid generator knows no bounds in bringing your creative ideas to life.

## Step-by-Step Tutorial: Building Your Animal Generator

Let's embark on a captivating journey as we build our very own animal generator using ILLA Cloud. Follow these simple steps to unleash the power of low code and [AI innovation](https://blog.illacloud.com/unleashing-creativity-building-ai-anime-generators-with-illa-cloud/):

### Step 1: Sign up and Access ILLA Cloud

Visit the ILLA Cloud website and sign up for a free account to gain access to the platform's versatile features.

Create a new App in your builder and name it `Animal Generator`

### Step 2: Add the Components

Select components from the pre-built components library and drag them onto your canvas. Customize their appearance and behavior to suit your preferences.

Add an input component, two button components labeled as `Clear` and `Generate`, a radio group labeled as `Example Prompt` with three items (optional), a radio group labeled as `Style` with three items (optional), and an image component. The overall layout can refer to the graph below.

![](https://blog.illacloud.com/content/images/2023/07/image-41.png align="left")

### Step 3: Integrate Hugging Face API

Explore the integration with Hugging Face and select the animal hybrid generator API. Connect it to your animal wheel component to enable the generation of unique animal hybrids.

At the bottom of the page, Click `+ New` under the Action list. Select `Hugging Face Inference API` from the action list.

![](https://blog.illacloud.com/content/images/2023/07/image-39.png align="left")

Fill out the configuration of Hugging Face with your Hugging Face token with `read` access from [here](https://huggingface.co/settings/tokens?ref=illa-blog).

![](https://blog.illacloud.com/content/images/2023/07/image-40.png align="left")

After creating your Hugging Face action, copy the model name of the model you want to use from Hugging Face `Model ID` (Here we use `jha2ee/StableDiffusion_finetuning_special_animal_style` for cartoon, `benlehrburger/animal-image-generation` for realistic, and `laserchalk/sketch-of-an-animal` for sketch. You can pick one of the three or find your own model from hugging face for style) and put the input components value as the input parameter into the model (ie `{{input1.value}}`)

![](https://blog.illacloud.com/content/images/2023/07/image-42.png align="left")

### Step 4: Configure the Components

For the `Style` radio group, we can manually label and assign value to each option.

![](https://blog.illacloud.com/content/images/2023/07/image-43.png align="left")

For the `Generate` button, we want to click it to generate a new image with the input sentence as the input parameter through the hugging face.

1\. Click the  \*\*\`button\`\*\* component to open its inspect page. Under \*\*\`Event handler\`\*\*, click `**+ New**`.

2\. In the Edit event handler, select \*\*\`Trigger action\`\*\* for the `action` and choose the hugging face API you want to trigger (ie `cartoon`) for the `action name`

3\. In order to only run the picked model in the `Style` radio group, we put `{{radioButton2.value == 'cartoon'}}` for `Only run when`.

Repeat the above steps for every model you want to trigger to generate different style.

![](https://blog.illacloud.com/content/images/2023/07/image-44.png align="left")

For the `Clear` button, we want to click it to clear the texts in the input components.

1\. Click the \*\*\`button\`\*\* component to open its inspect page. Under \*\*\`Event handler\`\*\*, click `**+ New**`.

2\. In the Edit event handler, select \*\*\`Control components\`\*\* for action, choose `input1` for components, and `clearValue` for Method.

Similarly, we create multiple event handlers to clear the value for `Example Prompt` and `Style` radio group.

![](https://blog.illacloud.com/content/images/2023/07/image-45.png align="left")

For the image component to display the output image from each hugging face model, we can put `{{radioButton1.value == 'realistic'? "data:image/jpeg;base64," +`[`realistic.data`](http://realistic.data) `: (radioButton1.value == 'cartoon'? "data:image/jpeg;base64," +` [`cartoon.data`](http://cartoon.data) `: "data:image/jpeg;base64," +` [`sketch.data`](http://sketch.data)`)}}` for `Image Source`.

![](https://blog.illacloud.com/content/images/2023/07/image-46.png align="left")

### Step 5: Test and Refine

Test your animal generator to ensure it functions seamlessly. Refine the design and add any additional features such as adding optional components, showing notifications when encountering an error, and customizing existing components as needed to enhance the user experience.

### Step 6: Deploy and Share

Once you are satisfied with your animal generator, deploy it to a live environment and share it with the world. Witness the delight of users as they spin the wheel to discover intriguing animal fusions and hybrid creatures.

## Conclusion: Empower Your Imagination with ILLA Cloud and Hugging Face

As you embrace the seamless integration of Hugging Face within ILLA Cloud, a world of endless possibilities unfolds before you. Witness the synergy of cutting-edge AI models like Roberta base and furry diffusion AI with ILLA Cloud's low-code power, fostering innovation in animal generators and beyond. Delight in the enchantment of [AI-driven](https://blog.illacloud.com/unleashing-creativity-building-ai-anime-generators-with-illa-cloud/) animal fusions, mythical beings, and dreamlike creatures with the animal generator wheel. Unravel the mysteries of bad prompt embedding and explore limitless creativity with Anything V3 and dreamlike-photoreal V.2. Embrace AI innovation with Hugging Face trainer, Auto Image, and Img2img, and let your imagination take flight as ILLA Cloud and Hugging Face empower your dreams to become reality.

With ILLA Cloud and Hugging Face by your side, building an animal generator becomes an immersive and delightful experience. Embrace the power of low code and [AI](https://blog.illacloud.com/unleashing-creativity-building-ai-anime-generators-with-illa-cloud/) innovation as you craft captivating animal hybrids and random animal combinations. Unleash the magic of creativity and watch in awe as your animal generator becomes a favorite among users, sparking wonder and joy with every spin of the wheel. Embrace the possibilities with ILLA Cloud and embark on a journey of imaginative animal creations like never before.

![](https://blog.illacloud.com/content/images/2023/07/group-17.png align="left")

> *Join our Discord Community:* [*discord.com/invite/illacloud*](http://discord.com/invite/illacloudTry)
> 
> *Try ILLA Cloud for free:* [*cloud.illacloud.com*](http://cloud.illacloud.com/?ref=illa-blog)
> 
> *ILLA Home Page:* [*illacloud.com*](http://illacloud.com/?ref=illa-blog)
> 
> *GitHub page:* [*github.com/illacloud/illa-builder*](http://github.com/illacloud/illa-builder)

Source:

(1) About ILLA - ILLA. [https://www.illacloud.com/en-US/docs/about-illa](https://www.illacloud.com/en-US/docs/about-illa).

(2) ILLA Cloud | Build internal tools at lightning speed. [https://www.illacloud.com/](https://www.illacloud.com/).

(3) ILLA Cloud - Product Information, Latest Updates, and Reviews 2023 .... [https://www.producthunt.com/products/illa](https://www.producthunt.com/products/illa).

(4) How to Automate Tasks with ILLA Cloud. [https://blog.illacloud.com/how-to-automate-tasks-with-illa-cloud-a-low-code-platform-for-internal-tools/](https://blog.illacloud.com/how-to-automate-tasks-with-illa-cloud-a-low-code-platform-for-internal-tools/).

(5) About ILLA - ILLA. [https://www.illacloud.com/docs/about-illa](https://www.illacloud.com/docs/about-illa).

(6) ILLA Cloud Hosting Pricing. [https://www.illacloud.com/pricing](https://www.illacloud.com/pricing)

(7) ILLA Cloud. [https://www.illacloud.com/illacloud](https://www.illacloud.com/illacloud)

(8) Updated Drag-and-Drop Feature of ILLA Cloud: Revolutionizing Component Placement and Layout. [https://blog.illacloud.com/updated-drag-and-drop-feature-of-illa-cloud-revolutionizing-component-placement-and-layout/](https://blog.illacloud.com/updated-drag-and-drop-feature-of-illa-cloud-revolutionizing-component-placement-and-layout/)

(9) Stable Diffusion Prompt Guide and How to connect stable diffusion in ILLA Cloud? [https://blog.illacloud.com/stable-diffusion-prompt-guide-and-how-to-connect-stable-diffusion-in-illa-cloud/](https://blog.illacloud.com/stable-diffusion-prompt-guide-and-how-to-connect-stable-diffusion-in-illa-cloud/)

(10) Unleashing Creativity: Building AI Anime Generators with ILLA Cloud. [https://blog.illacloud.com/unleashing-creativity-building-ai-anime-generators-with-illa-cloud/](https://blog.illacloud.com/unleashing-creativity-building-ai-anime-generators-with-illa-cloud/)