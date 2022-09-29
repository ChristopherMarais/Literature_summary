# Literature_summary
An attempt to make a knowledge graph from research papers.

used Scopus from elsevier and downlaoded ~3700 abstracts about bark and abrosia beetles

Used the followign as a guides:
- https://towardsdatascience.com/from-text-to-knowledge-the-information-extraction-pipeline-b65e7e30273e
- https://towardsdatascience.com/extract-knowledge-from-text-end-to-end-information-extraction-pipeline-with-spacy-and-neo4j-502b2b1e0754

# Steps
1. coreference resolution (crosslingual-coreference)
2. Named entity recognition (built in models)
3. Entity labelling (spacyfishing)
4. Entity linking (Rebel*)
5. Graph Creation

# To do:
- Graph of entities in field (nodes = entities, relationships = in text relations, metadata=relation strength == mention count)
- Graph of articles and people in field (nodes=[papers, people], relationships = citations, metadata=date)
- Topics and keywords in field over time (timeseries)(phronesis, lime, bert-package-summary)

#### Install packages in following order:
pip install pandas
pip install spacy
python -m spacy download en_core_web_trf
python -m spacy download en_core_web_sm
pip install crosslingual-coreference
pip install ipywidgets
pip uninstall torch
conda install pytorch torchvision torchaudio cudatoolkit=11.6 -c pytorch -c conda-forge
pip install spacyfishing
