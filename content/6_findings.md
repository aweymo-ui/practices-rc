---
title: Findings and Future Work
nav: Findings and Future Work
permalink: /6_findings/
gallery: true
---

<br>

{% include gallery-figure.html img="practice_25.png" alt="A black-and-white photograph of a smiling man with glasses and a beard, wearing a suit and tie, is on the left side of the image. To the right, there is a handwritten document with diagrams and notes, including sections labeled Opticolumn output and various technical terms and equations." caption="25." %}

<br>


After the fourth iteration of the model, Rebecca and I happened to be working on the Dr. Richard B. Wells Collection, a digital collection that turned out to be an excellent test subject for the tool. Richard B. Wells taught electrical engineering at the University of Idaho from 1983 to 2013. His family donated his notebooks, lab work, manuscripts, and monographs to the archives after his death in 2024. Most of the collection is handwritten and spans disciplines including coding and information theory, computational neuroscience, cognitive computing, and philosophy, especially Immanuel Kant's work.

{% include gallery-figure.html img="practice_26.png" alt="ACROBAT VERSUS OPTICOLUMN ACCURACY SURVEY WELL'S COLLECTION MATERIALS. It compares the first 100 word accuracy of OCR tools, with the Acrobat tool achieving 7.6% and the Opticolumn tool achieving 85.5%." caption="26." %}

<br>

These statistics compare OCR accuracy between Adobe Acrobat's most up-to-date version and our in-house "Opticolumn" tool across thirty handwritten documents in the Wells collection. Inaccurate words are identified as those misspelled or missing from the first 100 words of each document.

{% include gallery-figure.html img="practice_27.png" alt="OPTICOLUMN PROGRESS with a section on PDFs w/o OCR showing a bar graph. The report highlights that OCR was added to over 2,000 previously unreadable documents, processed and replaced for more than 14,000 documents across digital collections, and an additional 7 million words made accessible for keyword searching." caption="27." %}

<br>

In Spring 2026, I received approval to reprocess all of the PDF files in our digital collections with Opticolumn. To approach the remediation strategically, I developed another Python tool that scans all of the folders on our archive drive and tallies how many PDF files in each folder are missing an OCR layer. I used this as a guide to prioritize which collections to process first. Working with Digital Labs Manager Kevin Dobbins, we have now processed and replaced OCR for more than 14,000 documents across our digital collections and added OCR to more than 2,000 previously unsearchable documents. Based on combined post-processing reports, this has made an additional 7 million words accessible for keyword searching.

<br>

To evaluate the collections that have been processed, a randomized sample of documents from 32 digital collections was used to compare existing and newly generated OCR. The first 100 words of each document were evaluated for accuracy. Collections lacking an existing OCR layer were excluded from the sample. In this survey, Opticolumn achieved 85.25% accuracy, compared with 43.59% for the previous OCR.

{% include gallery-figure.html img="practice_28.png" alt="A person stands in front of a row of old, bulky machines, each with a screen, as they work on a task. The woman appears to be handling or organizing documents." caption="28." %}

<br>

There are a few challenges surrounding this project that I want to acknowledge in bullet points here, as they may be a bit niche to spend much time on in this talk, but happy to discuss further afterward. In short, the diversity of our digital collections led me to build an auditing workflow combining manual and automated checks: 

<br>

- Review script – generates the side-by-side comparison images you've seen throughout this presentation, letting me quickly check a document's first page against its OCR output.
- Report script – uses text mining libraries and regular expressions to tally the number of "true words" in the original folder versus the processed folder.

<br>

These batch methods are less precise than the human-directed sample surveys also used in this project, but they're helpful for confirming your large-scale remediation project is on the right track.

{% include gallery-figure.html img="practice_29.png" alt="Three identical newspaper spreads from The Idaho Argonaut presented in different ways under the title Future Work." caption="29." %}

<br>

Now that all of the collections that contained documents missing OCR have been reprocessed, I’m going to start working on our newspaper collections, which are notoriously difficult to order accurately. These will be processed using another version of the tool, which uses a more advanced pattern recognition and page segmentation model that can identify all of the various elements in a newspaper page.

<br>

Working with Head of Special Collections Dulce Kersting-Lark to create accessible versions of some of the items you've seen in this presentation has also opened up another opportunity. To help make some of this difficult, antiquated cursive material more accessible, I'll be working on another function that creates an intermediate CSV of the OCR output, which can be spot-checked and edited for accuracy, then the files can be processed a second time to incorporate these revisions into the embedded OCR layer.

<br>

What follows are practical takeaways for institutions considering a similar path, drawn from the successes and stumbling blocks of our own implementation.

<br>
