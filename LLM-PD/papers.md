# Large language models in Parkinson’s disease: emerging roles from diagnosis to data curation
## Key application areas
1. Diagnosis and digital phenotyping
Speech and language–based detection: LLMs and related NLP models classify PD from spontaneous speech transcripts with up to 78% accuracy and can predict disease severity, outperforming prior linguistic methods 919.
Linguistic features (e.g., action verb use, utterance errors, verbless utterances) distinguish PD from controls and between cognitive phenotypes (PD-MCI vs PD-nMCI) with AUC 75–85% 71019.
An LLM (Gemma-2 9B) using patients’ own words achieved 98% accuracy in distinguishing ON vs OFF medication states and tracked neuropsychiatric fluctuations (ρ≈0.81 with clinical scores) 5.
Speech audio models leveraging wav2vec 2.0 (a pre-trained language/audio model) reach ~98% cross‑validated accuracy for PD vs non‑PD from smartphone recordings 8.
2. Treatment personalization and clinical decision support:
An LLM-based framework that integrates patient narratives and guidelines, augmented with RAG, Chain-of-Thought, and Monte Carlo Tree Search, recommended medication regimens that reduced MDS‑UPDRS‑III motor scores by >1.4 points on average versus physician plans, and by 1.01 points versus RL methods 4.
A multimodal diagnostic system combined CNN imaging plus a fine‑tuned “Mini ChatGPT‑4.0” LLM to generate patient-specific summaries and treatment suggestions, improving usability and interpretability for clinicians 1.
3. Patient assessment, scales, and cohort/data infrastructure:
LLM-assisted frameworks can reconstruct structured MDS‑UPDRS item scores from free‑text self‑reports with ~95% accuracy 15.
Zero‑shot LLMs extracted UPDRS‑III information from drug‑induced parkinsonism case reports with 90% agreement with manual ratings 17.
Language-model embeddings harmonize variables across PD cohorts with >80–96% accuracy, supporting large‑scale data integration 11.
GPT‑3.5–based pipelines structured 822 neuropathology reports with ~74% accuracy, approaching manual curation 13.
4. Synthetic data and research support:
GPT‑4o can approximate symptom prevalence in synthetic PD diaries, but fails to capture realistic symptom correlations and narrative richness, limiting use to exploratory research unless domain‑tuned and carefully validated 14.
## Summary table: Where LLMs Are Used in PD

| Application Area | Example Outcome | Citations |
|---|---|---|
| Speech/language diagnosis & staging | 78–98% accuracy; severity prediction | 5891619 |
| Treatment recommendation | >1.4-point better motor scores than physicians | 14 |
| Scale automation & self-report parsing | ~90–95% accuracy compared with manual ratings | 1517 |
| Cohort harmonization & pathology extraction | 74–96% accurate mappings/extraction | 1113 |
| Synthetic diaries | Realistic prevalence, but poor correlations | 14 |

**Figure 1.** Major LLM use cases across Parkinson’s disease research and care.

Conclusion
Across Parkinson’s research, large language models are being used to detect disease and fluctuations from speech, personalize treatment, structure unstructured clinical and pathology data, automate rating scales, and generate synthetic data. Performance is often high but typically shown in retrospective or small‑scale studies; robust prospective clinical validation and attention to safety, bias, and explainability are still needed before routine clinical deployment.

## References
Paper	Answer	Population	Methods	Results	Outcomes	Sample Size	Study Count	Duration	Country
1. Web based AI-driven framework combining multi-modal data with CNN and LLM for Parkinson’s disease diagnosis, 2025, Ramkumar K et al., Scientific Reports.
__Summary:__ This AI-driven diagnostic framework improves diagnostic accuracy and enables personalized reporting in Parkinson's disease diagnosis, with a 93.7% classification accuracy and a cloud-based interface for real-time MRI uploads.	
People with Parkinson's disease from the PPMI dataset	Model development and evaluation using multimodal data and AI techniques.
The AI framework diagnosed Parkinson's disease with 93.7% accuracy using multimodal data.	
Diagnostic accuracy, interpretability of AI model outputs, quality of patient-specific diagnostic summaries.
2. A Comparative Analysis of Parkinson's Disease Diagnosis Approaches Using Drawing-Based Datasets: Utilizing Large Language Models, Machine Learning, and Fuzzy Ontologies, 2025, Adam Koletis et al.
__Summary:__ Combining symbolic and statistical AI may improve drawing-based Parkinson's disease diagnosis, with fuzzy ontology-based methods showing the strongest performance on complex tasks.	People with Parkinson’s disease and healthy controls	Comparative computational study of AI methods for Parkinson’s diagnosis	The fuzzy ontology method achieved the highest F1-score on complex drawing-based Parkinson’s diagnosis tasks.	Classification accuracy, interpretability, and generalization of PD diagnosis methods	—	—	—	—
3. Machine Learning Applications for Diagnosing Parkinson’s Disease via Speech, Language, and Voice Changes: A Systematic Review, 2025, Mohammad Amran Hossain et al.
__Summary:__ Machine learning techniques show high classification performance in diagnosing Parkinson's disease through speech and voice changes, but require further research to overcome comparability and integration challenges.	People with Parkinson’s disease studied via voice analysis	Systematic Review	Machine learning on voice data showed high accuracy in detecting Parkinson’s disease.	Accuracy of Parkinson's disease diagnosis using voice and speech analysis.
4. Leveraging Large Language Models for Personalized Parkinson's Disease Treatment., 2025, Rongqian Zhang et al., IEEE journal of biomedical and h...
5. Detecting neuropsychiatric fluctuations in Parkinson’s Disease using patients’ own words: the potential of large language models, 2025, M. Castelli et al., NPJ Parkinson's Disease
6. AI-driven precision diagnosis and treatment in Parkinson’s disease: a comprehensive review and experimental analysis, 2025, Bhekisipho Twala, Frontiers in Aging Neuroscience
7. Digital phenotyping of Parkinson’s disease via natural language processing, 2025, Simona Aresta et al., NPJ Parkinson's Disease
8. Parkinson's disease diagnostics using AI and natural language knowledge transfer, 2022, Maurycy Chronowski et al.
9. Linguistic changes in spontaneous speech for detecting Parkinson’s disease using large language models, 2025, Jonathan L Crawford, PLOS Digital Health
10. Digital Phenotyping of Parkinson’s Disease via Natural Language Processing, 2025, Simona Aresta et al., Research Square
11. Evaluating language model embeddings for Parkinson’s disease cohort harmonization using a novel manually curated variable mapping schema, 2025, Y. Salimi et al., Scientific Reports
12. Unveiling the Diagnostic Potential of Linguistic Markers in Identifying Individuals with Parkinson’s Disease through Artificial Intelligence: A Systematic Review, 2024, C. Palmirotta et al., Brain Sciences
13. Unpacking unstructured data: A pilot study on extracting insights from neuropathological reports of Parkinson’s Disease patients using large language models, 2024, Oleg Stroganov et al., Biology Methods & Protocols
14. Evaluating the Potential of AI-Generated Synthetic Diaries in Parkinson's Disease Research, 2025, Farhan Raza¹ et al.
15. A LLMs-Assisted Framework for Parkinson's Disease Assessment Based on PPMI Dataset, 2024, Zhenyu Gao et al., 2024 7th International Conferenc...
16. Analysis of spontaneous speech in Parkinson's disease by natural language processing., 2023, Katsunori Yokoi et al., Parkinsonism & related disorders
17. Validating large language models against manual information extraction from case reports of drug-induced parkinsonism in patients with schizophrenia spectrum and mood disorders: a proof of concept study, 2025, S. Volkmer et al., Schizophrenia
18. Exploring the Impact of Large Language Models on Disease Diagnosis, 2025, Ibrahim Almubark, IEEE Access
19. Deep Learning and Artificial Intelligence Applied to Model Speech and Language in Parkinson’s Disease, 2023, D. Escobar-Grisales et al., Diagnostics
20. Application of large language models in disease diagnosis and treatment, 2024, Xintian Yang et al., Chinese Medical Journal

