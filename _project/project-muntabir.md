---
permalink: /project/
author_profile: true
redirect_from: 
  - /project
---

Metadata Extraction from scanned ETDs
======
by **Muntabir Hasan Choudhury**

Extracting metadata from scholarly papers is an important text mining problem. Widely used open-source tools such as GROBID are designed for born-digital scholarly papers but often fail for scanned documents, such as Electronic Theses and Dissertations (ETDs). We have implemented heuristic model to extract seven metadata fields from the cover pages of scanned ETDs. We are also conducting research on learning based classification method such as Conditional Random Field (CRF) to extract the metadata. The process generally starts with converting scanned pages into images and then text files by applying Optical Character Recognition (OCR) tools. However, extracting metadata and full text segmentation from scanned ETDs are challenging due to poor image resolution, imperfection of OCR techniques, and typewritten text. Thus, another part of this research invloves in experimentation of various open-source and commercial based OCR tools including tesseract-OCR, Google Cloud API, and Clova.

**Heuristic Approach to Extract Metadata**

Although many complicated learning-based models could be built (e.g., CRF or Support Vector Machine (SVM)), to the best of our knowledge we could not find any dedicated effort and evaluation of heuristic methods with the ETD task. Heuristic methods are generally faster, suitable for capturing evident patterns. For this task, we carefully analyzed 100 scanned ETDs from MIT and Vtech libraries, and designed regular expressions (RegEx) for extracting seven metadata fields: titles, authors, years, degrees, academic programs, institutions, and advisors. Our model achieved an accuracy up to 97% and posed a strong baseline for further study on learning based methods. The following figure (Figure 1) is illustrating an example of extracting the degree field using RegEx. We submitted this work to ACM/IEEE Joint Conference on Digital Libraries 2020 (JCDL 2020). The paper can be download from <a href="https://lamps-lab.github.io/files/poster-ps316-002.pdf" target="_blank">here</a>. A detailed description of the implementation can also be found in the blog post on <a href="https://ws-dl.blogspot.com/2020/06/2020-06-07-regular-expression-powerful.html" target="_blank">RegEx to Parse Text from scanned ETDs</a>.
<div style="text-align: justify;">
<br /></div>
<table align="center" cellpadding="0" cellspacing="0" class="tr-caption-container" style="margin-left: auto; margin-right: auto; text-align: center;"><tbody>
<tr><td style="text-align: center;"><a href="/images/degree_regex.png" style="margin-left: auto; margin-right: auto;"><img border="0" data-original-height="833" data-original-width="949" height="560" src="/images/degree_regex.png" width="640" /></a></td></tr>
<tr><td class="tr-caption" style="text-align: center;"><span style="font-size: 12.8px;">Figure 1: Example of degree field extraction using RegEx from MIT and Virginia Tech ETDs</span></td></tr>
</tbody></table>

**Learning Based Approach to Extract Metadata**

Currently, this research is on-going. We made a significant progress on this task and implemented CRF model with 13 features.

OCR
======
Many state-of-the-art open access tools exhibit satisfactory performance with certain types of documents, experiments indicate that they tend to produce unacceptable errors or fail for scanned ETDs. Due to imperfection of OCR technique, it produces noisy data and lots of misspellings. Therefore, we compared three OCR tools based on how much clean data they generated with less misspellings.

**Tesseract-OCR**

We applied <a href="https://github.com/tesseract-ocr/tesseract" target="_blank">tesseract-OCR</a> while implementing the hueristic approach for extracting metadata from the cover pages of scanned ETDs. We chose tesseract-OCR because it is a widely adopted open source tool that takes any printed or scanned fonts, supports more than 100 languages, and returns output in text, hOCR, PDF, and other formats. Intially, we compared tesseract-OCR with OpenCV OCR with EAST detector. However, OpenCV OCR failed to recognize text from scanned ETDs, produced lots of errors, and did not provide the expected result. On the contrary, our experiemnts shows that tesseract-OCR perfomed a better job over OpenCV OCR since it produced less errors and misspellings. Figure 2 is illustrating the result of the tessearct-OCR on the cover pages of scanned ETDs. More information can be found on <a href="https://ws-dl.blogspot.com/2020/05/2020-xx-xx-ocr-tools-experiment-on.html" target="_blank">OCR Tools Experiments</a> in the blog post written by Muntabir Choudhury.
<div style="text-align: justify;">
<br /></div>
<table align="center" cellpadding="0" cellspacing="0" class="tr-caption-container" style="margin-left: auto; margin-right: auto; text-align: center;"><tbody>
<tr><td style="text-align: center;"><a href="/images/tesseract-text.png" style="margin-left: auto; margin-right: auto;"><img border="0" data-original-height="833" data-original-width="949" height="560" src="/images/tesseract-text.png" width="640" /></a></td></tr>
<tr><td class="tr-caption" style="text-align: center;"><span style="font-size: 12.8px;">Figure 2: Tesseract OCR result on the cover page of scanned ETDs</span></td></tr>
</tbody></table>
<div style="text-align: justify;">
<br /></div>
<table align="center" cellpadding="0" cellspacing="0" class="tr-caption-container" style="margin-left: auto; margin-right: auto; text-align: center;"><tbody>
<tr><td style="text-align: center;"><a href="/images/google-text.png" style="margin-left: auto; margin-right: auto;"><img border="0" data-original-height="833" data-original-width="949" height="560" src="/images/google-text.png" width="640" /></a></td></tr>
<tr><td class="tr-caption" style="text-align: center;"><span style="font-size: 12.8px;">Figure 3: Google Cloud API OCR result on the cover page of scanned ETDs</span></td></tr>
</tbody></table>

**Google Cloud API OCR**

Although tesseract peformed better than OpenCV OCR, it produced noisy data and misspellings. We experimented commercial based tools such as <a href="https://cloud.google.com/functions/docs/tutorials/ocr" target="_blank">Google Cloud API OCR</a> to see if it outperforms tesseract-OCR. Google Cloud API OCR provides free trial for 12 months and we took the advantage of it. Figure 3 is illustrating the result of the Google Cloud API OCR. We could see that it performed better than tesseract-OCR, however, it still generated misspellings and few noisy data. 

**Clova OCR**

Currently, we are experimenting Clova OCR. It's an open source tool and it utilized <a href="https://github.com/clovaai/deep-text-recognition-benchmark" target="_blank">deep text recognition</a> and <a href="https://github.com/clovaai/CRAFT-pytorch" target="_blank">detection (CRAFT)</a> to extract the text from a scanned image. For further investigation, we used <a href="https://clova.ai/ocr" target="_blank">clova ai (demo tool)</a> which is a GUI (graphical user interface) and allows user to perform OCR on scanned image. Figure 4 is illustrating the result of the Clova OCR. The result seemed promising and outperformed both Google Cloud API OCR and tesseract-OCR. 
<table align="center" cellpadding="0" cellspacing="0" class="tr-caption-container" style="margin-left: auto; margin-right: auto; text-align: center;"><tbody>
<tr><td style="text-align: center;"><a href="/images/clova-gui.png" style="margin-left: auto; margin-right: auto;"><img border="0" data-original-height="833" data-original-width="949" height="560" src="/images/clova-gui.png" width="640" /></a></td></tr>
<tr><td class="tr-caption" style="text-align: center;"><span style="font-size: 12.8px;">Figure 4: Clova OCR result on the cover page of scanned ETDs</span></td></tr>
</tbody></table>