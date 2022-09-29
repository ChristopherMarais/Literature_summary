# Literature_summary
An attempt to make a knowledge graph from research papers.

used Scopus from elsevier and downlaoded ~3700 abstracts about bark and abrosia beetles

Used the followign as a guide https://towardsdatascience.com/from-text-to-knowledge-the-information-extraction-pipeline-b65e7e30273e


1. coreference resolution
2. Named entity recognition
3. Entity linking/labelling
4. Relationship extraction

# graph of entities in field
# graph of articles and people in field
# topics and keywords in field over time (phronesis, lime, bert-package-summary)

#### for crosslingual-coreference:
pip install pandas
pip install spacy
python -m spacy download en_core_web_trf
python -m spacy download en_core_web_sm
pip install crosslingual-coreference
pip install ipywidgets
pip uninstall torch
conda install pytorch torchvision torchaudio cudatoolkit=11.6 -c pytorch -c conda-forge
pip install spacyfishing
