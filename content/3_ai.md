---
title: AI Models
nav: AI Models
permalink: /3_ai/
gallery: true
---

<br>

The article this presentation is based on was written for a special issue of the Collections journal focusing on ethical AI in galleries, libraries, archives, and museums. Unlike writing for a technical journal, we found conflicting emotions among cultural heritage workers: scholarly journals seem genuinely interested in AI, whether that takes the form of excitement, dread, or skepticism, but only up to a certain level of technical detail. While I'll spare you as much jargon as possible, we found while writing the article that it's important to distinguish a few technical concepts to help explain how we arrived at our findings.

{% include gallery-figure.html img="practice_07.png" alt="A Venn diagram illustrating the relationships between different AI models, including algorithms, transformer models, large language models, and convolutional neural networks. It highlights that large language models are transformer models but not all transformer models are large language models." caption="7." %}

<br>

Though the AI landscape is vast, this study focuses on specific model types relevant to OCR. A neural network (NN) is a “form of machine learning algorithm inspired by the structure of the human brain, where interconnected nodes are organized in layers, with each performing a mathematical operation to produce an output.” Computer vision and page segmentation models are examples of convolutional neural networks (CNN), a “type of machine learning algorithm designed to process data arranged in a regular grid, such as digital images,” which excel at pattern recognition. 

The next advancement beyond NNs are transformer model (TM) architectures, which integrate a weighted “attention mechanism” and a streamlined structure that helps find solutions to complex requests more easily. Finally, large language models (LLM) refer to a series of algorithms that “leverage the transformer based. . . architecture and undergo extensive training on a massive textual corpora” as a basis for generating natural-sounding text. Of the models discussed here, LLMs are uniquely vulnerable to hallucination, in which the model generates “seemingly plausible yet factually unsupported content,” and specifically intrinsic hallucination, in which “generated output contradicts the source content.”

{% include gallery-figure.html img="practice_08.png" alt="A document with handwritten text, labeled Aron T. Vickers, and a title By the President followed by Abraham Lincoln." caption="8." %}

When I work on these projects, I use a programming language called Python. In addition to my normal practice of importing libraries, implementing configurations, and setting up a structure to handle the processing and output of materials, testing open large language models also involved writing a prompt in the script, exactly as one might through ChatGPT. For these examples of hallucinations, my prompt was:

```
PROMPT = (
    "<image>\nTranscribe only the text visible in this image, exactly as "
    "written. Output the raw text and nothing else — no quotes, no "
    "commentary, no formatting. If there is no legible text, output nothing."
)
```

In most cases, the basis of the hallucination is rooted in the design of a model trained on a massive corpus of English language material which is attempting to establish patterns in the visual information inside the image of a page.

<br>

- In this foundational document, Abraham Lincoln (alternate name: Arnold Vinick) is interrupted by a long string of BW’s. Possibly an interpretation of the slight crease in the paper. 

{% include gallery-figure.html img="practice_09.png" alt="A document titled LLM HALLUCINATION EXAMPLES with a prompt instructing to transcribe the text visible in the image, exactly. Below the prompt, there is a handwritten document labeled Article VI with a note stating, Left in the school fund from which money is sought to be drawn." caption="9." %}

<br>

- In this cursive passage whose last two lines read “in the school fund from which said moneys are sought to be drawn,” the LLM interprets “In 2. As soon as the trick shall be en- Him to see me any port in the sea.” This is of interest not as a misidentification, but because we can see the model attempt to partially invoke an idiom “any port in a storm” perhaps only through context clues of the style of cursive, level of distortion in the paper, to make human sounding patterns of speech as opposed to 1:1 reflections of writing on a word by word basis. 
- In the example on the right, we can see another trend of lines of dialogue repeating at seemingly random points within a paragraph.

{% include gallery-figure.html img="practice_10.png" alt="A document with text that is not fully legible due to OCR errors, accompanied by examples of hallucinations from an AI model." caption="10." %}

<br>

- Despite explicitly stating it in the prompt, another frequent phenomenon is the interjection of the model commenting on its ability to transcribe the material becoming embedded into the OCR page. It can be seen here not only in the repeated $ERROR$ messages but also comments at the tops and bottoms of pages like “I am not sure what you are asking. Can you please provide more context or information?”

{% include gallery-figure.html img="practice_11.png" alt="A document titled LLM HALLUCINATION EXAMPLES with a prompt that instructs to transcribe the text visible in the image, exactly as written, outputting raw text and nothing else—quotes. Below the title, there are two sections on the left, handwritten text from a document labeled 3rd Session Council Bill No." caption="11." %}

<br>

- Here is an unsettling example where the model may have gleaned from the context clues of the other materials I was testing that I was located in Moscow, Idaho, as a suggestion for this particularly difficult block of decorative cursive writing. 

- Finally, after correctly interpreting the page number from this scrapbook from the Taylor Wilderness Research Station Archive, this Spanish hallucination tells us to “Determine the maximum habitat of the species, distributed across…” a fairly large area.

{% include gallery-figure.html img="practice_12.png" alt="A woman wearing headphones operates an Optiphone in 1918. To the right, a diagram illustrates how musical notes combine to form parts of each letter in a word, with labeled notes and terms like run of high and low notes and diverging and converging notes." caption="12." %}

<br>

As Rebecca mentioned, archivists have been integrating OCR into preservation practices since the 1980s, but people have been attempting to transcribe the printed word into other mediums for more than a hundred years. In 1912, Edmund Edward Fournier d'Albe debuted an invention called the Optophone, which converted the printed page into musical notes as an alternative to braille. Similarly, the roots of AI go back to around that same time, in the form of N-grams and probability statistics. It isn’t until 2022, when OpenAI’s ChatGTP debuted that most people were introduced to both artificial intelligence and large language models in tandem, which is why most people would generally conflate this particular model with its umbrella term. For processing cultural heritage materials where introducing any amount of LLM generated hallucinations is detrimental to the historical record, I've found that stepping back to more binary, non-prompt-driven neural networks and transformer models maintain a more consistent 1:1 reflection of the original document, which capture a document’s “flaws” instead of attempting to make sense of them.

<br>