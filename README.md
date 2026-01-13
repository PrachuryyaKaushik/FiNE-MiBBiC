# FiNE-MiBBiC: Fine-grained Named Entity Recognition Dataset for Mizo, Bhojpuri, Bishnupriya Manipuri and Chhattisgarhi

## Abstract

We introduce **Fine-MiBBiC**, a fine-grained named entity recognition (FgNER) dataset encompassing **four low-resource Indian languages**. To address the scarcity of FgNER resources for Indian languages, we have utilized the **Entity-anchored Machine Translation (EaMaTa)** framework. By leveraging the manually annotated English dataset *FewNERD*, we created a large-scale resource comprising an average of 153k sentences and 354k entities per language.

***Note: 50 samples from each dataset file are included for reference. The entire dataset will be uploaded to HuggingFace upon acceptance of the paper.***

## 🛠 The EaMaTa Framework

The **[Entity-anchored Machine Translation](https://github.com/PrachuryyaKaushik/SampurNER/blob/main/SampurNER_AAAI_extended.pdf)** framework ensures high-quality translation by:

1. **Preprocessing:** Converting BIO format to entity-anchored text (e.g., using  tags).
2. **Translation:** Translating both plain and anchored versions.
3. **Cleaning:** A three-stage pipeline to discard sentences with mismatches in structure, anchor boundaries, or entity counts.

---

<img src="https://github.com/PrachuryyaKaushik/SampurNER/blob/main/EaMaTa_framework_final_poster-1.png" alt="Entity-anchored Machine Translation: The source dataset is translated both as `Plain sentence' and `Entity-anchored sentence' to the target languages. The cleaning process includes the removal of sentences with sentence mismatch, entity-anchor boundaries mismatch (both start and end), and total entity counts mismatch between the source and translated sentences." width="500">


## 📊 Dataset Statistics

Statistics for the generated datasets across 22 languages along with the source FewNERD (English) dataset. Sent, Ent Tok means number of Sentences, Entities and Tokens respectively.

<table>
  <thead>
    <tr>
      <th rowspan="2">Language</th>
      <th colspan="3">Train Set</th>
      <th colspan="3">Development Set</th>
      <th colspan="3">Silver Test Set</th>
    </tr>
    <tr>
      <th>Sentences</th>
      <th>Entities</th>
      <th>Tokens</th>
      <th>Sentences</th>
      <th>Entities</th>
      <th>Tokens</th>
      <th>Sentences</th>
      <th>Entities</th>
      <th>Tokens</th>
    </tr>
  </thead>
  <tbody>
    <tr><td><b>Mizo</b></td><td>78,762</td><td>183,595</td><td>1,983,240</td><td>12,232</td><td>29,004</td><td>313,115</td><td>27,826</td><td>67,254</td><td>717,052</td></tr>
    <tr><td><b>Bhojpuri</b></td><td>111,276</td><td>268,709</td><td>2,819,109</td><td>15,909</td><td>38,518</td><td>405,276</td><td>31,831</td><td>76,469</td><td>805,066</td></tr>
    <tr><td><b>Bishnupriya</b></td><td>79,349</td><td>161,191</td><td>1,646,195</td><td>11,700</td><td>23,987</td><td>244,318</td><td>25,296</td><td>42,842</td><td>517,433</td></tr>
    <tr><td><b>Chhattisgarhi</b></td><td>108,979</td><td>242,460</td><td>4,422,373</td><td>15,633</td><td>35,048</td><td>484,212</td><td>31,108</td><td>68,743</td><td>751,897</td></tr>
  </tbody>
</table>

---

## 📈 Experimental Results (F1-Scores)

Performance of **mBERT** and **IndicBERTv2** models fine-tuned on SampurNER.
<table>
  <thead>
    <tr>
      <th rowspan="2">Language</th>
      <th colspan="3">mBERT (Micro)</th>
      <th colspan="3">IndicBERTv2 (Micro)</th>
    </tr>
    <tr>
      <th>P</th>
      <th>R</th>
      <th>F1</th>
      <th>P</th>
      <th>R</th>
      <th>F1</th>
    </tr>
  </thead>
  <tbody>
    <tr><td><b>FewNERD (en)</b></td><td>65.2</td><td>69.1</td><td>67.1</td><td>64.0</td><td>68.2</td><td>66.0</td></tr>
    <tr><td><b>Mizo</b></td><td>58.3</td><td>63.1</td><td>60.5</td><td>56.9</td><td>62.4</td><td>59.5</td></tr>
    <tr><td><b>Bhojpuri</b></td><td>53.9</td><td>56.9</td><td>55.2</td><td>56.4</td><td>60.4</td><td>58.2</td></tr>
    <tr><td><b>Bishnupriya</b></td><td>48.7</td><td>53.7</td><td>51.6</td><td>48.7</td><td>51.1</td><td>50.1</td></tr>
    <tr><td><b>Chhattisgarhi</b></td><td>55.8</td><td>57.1</td><td>56.5</td><td>55.9</td><td>59.9</td><td>58.1</td></tr>
  </tbody>
</table>

---

## 🚀 More resources
* [SampurNER paper](https://github.com/PrachuryyaKaushik/SampurNER/blob/main/SampurNER_AAAI_extended.pdf)
* [Fine-tuned models](https://huggingface.co/collections/prachuryyaIITG/sampurner)
* [Interactive Demo](https://huggingface.co/spaces/prachuryyaIITG/SampurNER-Demo)
* [Agentic tool: AWED-FiNER](https://github.com/PrachuryyaKaushik/AWED-FiNER)

### Citation

```bibtex
@inproceedings{kaushik2026sampurner,
  title={SampurNER: Fine-grained Named Entity Recognition dataset for 22 Indian Languages},
  author={Kaushik, Prachuryya and Anand, Ashish},
  booktitle={Proceedings of the AAAI Conference on Artificial Intelligence},
  volume={40},
  year={2026}
}


```

---

**Maintained by:** [Prachuryya Kaushik](https://huggingface.co/prachuryyaIITG)

---
