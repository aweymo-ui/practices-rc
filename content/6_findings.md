---
title: Findings and Future Work
nav: Findings and Future Work
permalink: /6_findings/
gallery: true
---

<br>

<div class="symbol-container">
    <p class="symbol">&#x1011C;</p>
</div>

<br>


After the fourth iteration of the BLLA/TrOCR model that eventually became Opticolumn, we happened to be working on the Dr. Richard B. Wells Collection, a digital collection that turned out to be an excellent test subject for the tool. Richard B. Wells taught electrical engineering at the University of Idaho from 1983 to 2013. His family donated his notebooks, lab work, manuscripts, and monographs to the archives after his death in 2024. Most of the collection is handwritten and spans disciplines including coding and information theory, computational neuroscience, cognitive computing, and philosophy, especially Immanuel Kant's work.

<div class="symbol-container">
    <p class="symbol">&#x1011D;</p>
</div>

<br>

The following statistics compare the accuracy of Adobe Acrobat's most up-to-date OCR output against our in-house "Opticolumn" tool on the thirty documents in the Dr. Richard B. Wells digital collection, material that is completely handwritten. Inaccurate words are defined as words that are misspelled or missed completely from the first 100 words in each document.

<div class="symbol-container">
    <p class="symbol">&#x1011E;</p>
</div>

<br>

In Spring 2026, I received approval to reprocess all of the PDF files in our digital collections with Opticolumn. To approach the remediation strategically, I worked on another Python tool that scans all of the folders on our archive drive and tallies how many of the PDF files in each folder are missing a layer of OCR. I used this as a guide to prioritize which collections to process first, and collaborating with Digital Labs Manager Kevin Dobbins, we have now updated more than 15,000 documents that have increased the searchability of a hand sampled word count by [updated survey] percent and ensuring that all of our materials we are hosting on our digital collections are accessible to patrons.

<div class="symbol-container">
    <p class="symbol">&#x1011F;</p>
</div>

<br>

There are a few challenges surrounding this project that I want to acknowledge in bullet points here, as they may be a bit niche to spend much time on in this talk, but happy to discuss further afterward. In short, the diversity of our digital collections led me to build an auditing workflow combining manual and automated checks: 

<br>

- Review script – generates the side-by-side comparison images you've seen throughout this presentation, letting me quickly check a document's first page against its OCR output.
- Report script – uses text mining libraries and regular expressions to tally the number of "true words" in the original folder versus the processed folder.

<br>

These batch methods are less precise than the human-directed sample surveys also used in this project, but they're helpful for confirming your large-scale remediation project is on the right track.

<div class="symbol-container">
    <p class="symbol">&#x10120;</p>
</div>

<br>

Now that all of the collections that contained documents missing OCR have been reprocessed, I’m going to start reprocessing our newspaper collections, which are notoriously difficult to transcribe and order accurately. These will be processed using another version of the tool, very creatively named Opticolumn(s), which uses the same neural network text recognition model but pairs it with a more advanced pattern recognition and page segmentation model named Surya. Surya specializes in identifying all of the different elements that make up a dense newspaper page and assigning each section its correct reading order.

Working with Head of Special Collections and Assistant Professor Dulce Kersting-Lark to create accessible versions of some of the items in this presentation has also opened up another opportunity. To help make some of this difficult, antiquated cursive material more accessible, I'll be drafting another function that creates an intermediate CSV of the OCR output after processing PDF files. This CSV can be easily spot-checked and edited for accuracy, and then the files can be processed a second time to incorporate these revisions into the final embedded layer.

What follows are practical takeaways for institutions considering a similar path, drawn from the successes and stumbling blocks of our own implementation.

<br>
