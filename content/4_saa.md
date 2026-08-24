---
title: SAA Core Values and Code of Ethics
nav: SAA Core Values and Code of Ethics
permalink: /4_saa/
gallery: true
---

<br>

<div class="symbol-container">
    <p class="symbol">&#x1011C;</p>
</div>

<br>

In the decades that archivists have been using OCR, they have consistently valued it for two main reasons: OCR can offer access to archival documents for people with visual impairments or who otherwise cannot directly access original sources, and it makes archival materials more discoverable through keyword searching, subject tagging, and other similar content recognition methods. But the technology has never been perfect, and as with all new and changing technologies, archivists have continually had to assess how OCR technologies fit with our longstanding professional values and code of ethics. The archival profession has existed since at least the early 19th century; people have been trying to keep historical documents safe for a lot longer than that, but the development of this formal profession in which we acquire records as a matter of course, store them according to specific methods, set up certain legal agreements for stewardship and so on - that has roots in the era following the French Revolution. Archival practices and values have changed quite a lot over the past 200-plus years, but the technologies available to us have changed much more, and it's always up to us to decide how or whether to adopt new technologies so that we are staying true to what we consider ethical archival work. 

Archivists have a few different values statements and codes of ethics to look to, but a good solid reference for archivists in the US is the Society of American Archivists' Core Values Statement and Code of Ethics. The Society of American Archivists is the largest and oldest professional association for archivists in the US, and it does a lot to guide the work of archivists, including developing and maintaining this values statement and code of ethics, which is based on the collective wisdom and experience of generations of archivists, but is also meant to reflect our current values, priorities, pressures, and so on. So if we're thinking about how different OCR technologies fit with archival values and ethics, then the SAA Core Values Statement and Code of Ethics can serve as sort of evaluation criteria for different kinds of OCR tools.

From this bigger set of values and ethics, I distilled out four core sets of values that we could focus on as assessment criteria for OCR tools: authenticity and integrity, transparency and accountability, access and equity, and responsible stewardship and sustainability. These are simplified versions of more complex standards and guidelines from the SAA, but they work well as a shorthand for things that are important to archivists.

<div class="symbol-container">
    <p class="symbol">&#x1011D;</p>
</div>

<br>

The first set is authenticity and integrity, which in archival work refer to the archivist's responsibility to maintain the trustworthiness of the historical record. When possible, materials that we hold in our collections have to retain their original content, some sense of context, and their value as evidence of past activities. If we're using OCR to recognize text in our archival materials, then the OCR's output should reflect the true content of the documents, including any errors or imperfections that the original documents might have. If the OCR reads something erroneously, then it should be clear that that is an error. The OCR tool should not be trying to make corrections to original materials, making up words when it's not sure, covering up errors, making the documents "better", or otherwise fabricating text that isn't there. 

Transparency and accountability mean that archivists should clearly document their processes, make decisions visible, promote professional accountability, and maintain trust and understanding with non-archivists. Aside from some historical materials that we are legally obligated to keep away from the public, everything we hold and everything we do should be clear and understandable and accessible. Archivists have no trade secrets. When it comes to using OCR, we want to be able to explain and document exactly how OCR was performed: the tool we used, how we decided to use that tool, what the tool does and does not do, where errors might arise, what errors look like, and so on.

<div class="symbol-container">
    <p class="symbol">&#x1011E;</p>
</div>

<br>

Access and equity refer to our work making archival materials discoverable and accessible, trying to overcome technical and economic barriers when possible. We want the public to find the documents they're interested in and then have access to that content, even if they can't travel to us, even if they can't directly view or visually interpret the item for one reason or another - that's the ideal, anyway. One goal with using OCR is to allow for full-text keyword searching of archival documents, and that full text can also be used with assistive technologies, such as screen readers. Accurate OCR, without fabrications or other big errors, can support equitable access to the historical record. But also a large volume of OCRed materials helps support access, so speed and ease of use are important considerations as well.

Finally, archivists have to make decisions about technology options with sustainability and stewardship in mind. Sustainability in this context can mean choosing options that are less environmentally harmful than others, but it also means using financial, technical, and human resources in a way that will be sustainable for the institution over the long term, on the archival timescale of decades or centuries. Unsustainable practices threaten proper stewardship of the historical record. When it comes to OCR tools, archivists need to consider whether the tool and its outputs are supportable with resources available both now and in the future. Digital tools are modified or discontinued all the time, and we have to plan for that. 

<div class="symbol-container">
    <p class="symbol">&#x1011F;</p>
</div>

<br>

The sustainability question gets at a bigger issue in the archival world, which is that archivists are usually dependent on some kind of service from vendors or proprietary technologies - we usually don't have the resources to do or create absolutely everything in-house. And sometimes those services prove to be unsustainable, which puts archival materials or projects at risk. Cloud storage is one example - many archival institutions choose to keep their digital records in the cloud, using companies such as Amazon Web Services. Once you become reliant on a service, you have given over some degree of power and control to that company. AWS seems pretty reliable now, but in the past it has had issues with unpredictable pricing and confusing mechanisms to actually retrieve your digital records. Just recently, a PBS station lost access to 70 years' worth of its archival materials because its cloud storage provider went out of business, and they found that it had been backed up elsewhere, but they had to go through a bunch of legal nonsense in order to regain access to it. Other institutions have had a lot of trouble migrating their content out of proprietary digital collections services when they don't want to work with that platform anymore. All of this is to say that becoming dependent on proprietary technology can lead to these "rug pulls" that affect archivists and archival collections negatively. 

This matters for OCR because plenty of OCR tools are proprietary technology. If we build our accessibility workflow entirely around a particular vendor's model, we're exposed to risks such as pricing changes, service discontinuation, or simply losing the ability to understand or reproduce the OCR results we're getting. So when we evaluate OCR tools, we're not just thinking about whether they're accurate, transparent, and documentable, but we're also thinking about whether investing in them is setting us up for sustainable workflows over the long term, or whether we're unnecessarily developing new dependencies.

As Andrew has talked about and will go into greater detail about shortly, archivists and librarians have choices about which OCR tools to use, including choices between LLM-based tools and non-LLM-based tools. Each kind of tool has its own advantages and drawbacks and quirks, and each one will fit differently against archival ethics as expressed in the SAA's values statement and code of ethics. Our case study gets into the construction of an OCR tool that is an alternative to commercial and proprietary LLM OCR tools, and why we chose this direction. 

<br>
