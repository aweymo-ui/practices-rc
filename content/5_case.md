---
title: Case Study
nav: Case Study
permalink: /5_case/
gallery: true
---

<br>

{% include gallery-figure.html img="practice_19.png" alt="A document titled ADOBE ACROBAT OUTPUT with examples of majority text generated from Acrobat version 20.6, highlighting that the same collection has documents processed with version 9 and earlier. The left side of the document contains a lengthy typed text, while the right side displays a newspaper article about Thunder City, Idaho, with a headline Thunder City, Idaho – another gateway to nowhere and accompanying images." %}

<br>

At the Center for Digital Inquiry and Learning, it has been standard practice to run all scanned PDF digital derivatives through Adobe Acrobat to generate a layer of OCR. In a test of 30 sample items, I found that Adobe Acrobat accurately identified typewritten text 25 percent of the time, but had only 1.15 percent accuracy when faced with handwritten (print or cursive) material, which makes up a large portion of the University of Idaho Library's digitized archival documents.

{% include gallery-figure.html img="practice_20.png" alt="Handwritten notes and calculations in a notebook, with a title ADOBE ACROBAT OUTPUT at the top. The notes include examples of handwritten print and cursive text." %}

<br>

Adobe Acrobat also struggles to identify words in unconventional formats, such as diagrams, bolded titles, and signs. Since staff at CDIL have been digitizing materials for over ten years, it's reasonable to assume that the transcription quality of documents processed with older versions of Adobe Acrobat are even less accurate than the results of our test with the current version. Based on these conclusions, I decided to focus on an OCR tool that can reprocess nearly 18,000 document files across our digital collections, rather than surveying and cherry-picking collections known to have particularly poor-quality OCR.

{% include gallery-figure.html img="practice_21.png" alt="A person stands in a room filled with shelves, looking at documents. The image is black and white, with a title on the left side reading GOALS FOR DEVELOPING THE OCR TOOL." %}

<br>

My goals in developing this OCR tool locally continue to be:

<br>

- Implementing free, open-source models for sustainability.
- Ensuring these models don't require an API login or tokens, and run locally after their initial download, for data privacy.
- Achieving a significant improvement in the accuracy of both typed and handwritten text materials.
- Keeping file size growth relatively minimal (5–15 percent) with the addition of the OCR layer.
- Ensuring that processed files meet the definition of "programmatic text" as described in WCAG 2.1 Level AA standards.	
- Making the tool freely available to other institutions facing similar challenges.

<br>

Beginning summer 2025, I set out to survey open-source models, create Python tools using them, and test them against the same set of sample documents. The sample set of roughly 120 documents for testing the OCR models comes from the U of I digital collections, including a selection of typed, handwritten, and cursive text, as well as items containing a combination of all three. For the initial tests, only single-page PDF files were used. In later iterations, I tested multi-page documents to ensure that the PDF files were collating correctly.

{% include gallery-figure.html img="practice_22.png" alt="A document with visible text, accompanied by a section titled LLM HALLUCINATION EXAMPLES at the top." %}

<br>

I began the survey by testing three open large language models that produced the hallucinations I shared with you earlier. The findings highlighted a fundamental danger in incorporating LLM processes in the archives: untraceable errors. When an LLM is prompted to identify the words on a page, it is inherently prone to generating a solution based on context clues from legible material, one that may not actually reflect what's in the text. Moreover, these hallucinations may be nearly impossible to identify and correct, because they look and sound like the natural human language the LLM was trained on. With this in mind, I pivoted to exploring neural networks and transformer models, which, in all of my testing, have not demonstrated a vulnerability to hallucination and more accurately reflect what's on the page, including illegible characters, crossed-out passages, and misspellings.

<div class="symbol-container">
    <p class="symbol">&#x1011A;</p>
</div>

<br>

The following is a list of models tested after the initial round with three distinct LLM models, along with brief notes on each one's performance. All of the tools here are text recognition models, except for Box Line and Layout Analysis (BLLA), which is a page segmentation model that helps cluster groups of text specifically for archival materials.

<div class="symbol-container">
    <p class="symbol">&#x1011B;</p>
</div>

<br>

Once BLLA and TrOCR emerged as the top candidates for Opticolumn, an endless period of debugging began. Denoising and confidence-level parameters boosted accuracy. A spell checker seemed like a promising addition until the acronym-laden scientific digital collections proved it would create more errors than it fixed. Setting a minimum character count per page segment helped filter out noise and misidentified characters potentially lurking in illustrations. Finally, adding XMP metadata, refining the OCR rendering method, and streamlining PDF assembly and compression resolved accessibility flags while keeping file sizes reasonable.

<br>
