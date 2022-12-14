# Literature_summary
An attempt to summarize a filed of study through meta analysis.

used Scopus from elsevier and downlaoded ~3700 abstracts about bark and abrosia beetles

Used the followign as a guides:
- https://towardsdatascience.com/from-text-to-knowledge-the-information-extraction-pipeline-b65e7e30273e
- https://towardsdatascience.com/extract-knowledge-from-text-end-to-end-information-extraction-pipeline-with-spacy-and-neo4j-502b2b1e0754

# Steps:
- Extract entities and relationships 
- Extract topics
- construct edgelsit of for topic and keyword relationships
- 

## Steps for entity extraction:
1. coreference resolution (crosslingual-coreference)
2. Named entity recognition (built in models)
3. Entity labelling (spacyfishing)
4. Entity linking (Rebel*)
5. Graph Creation

# Graphs:
- Graph of entities in field (nodes = entities, relationships = in text relations, metadata=relation strength == mention count)
- Graph of articles and people in field (nodes=[papers, people], relationships = citations, metadata=date, node weight = reference count)
- Graph of keywords and topics  (nodes=[keywords, topics], relationships = freqeuncy of nodes found in same paper, node weight = reference count)

# Timeseries:
- All graphs over time*
- Topics over time (bertopic)

# environments:

#### Install packages in following order for entity edge list:
- pip install pandas
- pip install spacy
- python -m spacy download en_core_web_trf
- python -m spacy download en_core_web_sm
- pip install crosslingual-coreference
- pip install ipywidgets
- pip uninstall torch
- conda install pytorch torchvision torchaudio cudatoolkit=11.6 -c pytorch -c conda-forge
- pip install spacyfishing
- pip install matplotlib
- Add rebel component https://github.com/Babelscape/rebel/blob/main/spacy_component.py
- pip install wikipedia

#### Install packages in following order for topic modelling:
- conda install pytorch torchvision torchaudio cudatoolkit=11.6 -c pytorch -c conda-forge
- pip install bertopic
- pip install bertopic[visualization]
- pip install joblib==1.1.0
- conda install -c conda-forge ipywidgets
- conda install -c anaconda scikit-learn
- pip install pandas

#### Install packages in following order for graph construction:
- networkx??
- neo4j??

- port networkx graphs into neo4j
- add multigraph with wiki labels of entities
- combine search results from multipel searches
- enrich with other text
- apply to SDG data
- collapse terms with lemmatization
- add papers that support each edge to graph
- 