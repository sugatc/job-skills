# Using Domain-Specific Word Embeddings to examine the Demand for Skills
**Authors**: Sugat Chaturvedi, Kanika Mahajan, Zahra Siddique
(Last updated: October 4, 2023)

This repository provides code to train domain specific embeddings using fastText on online job ads data to obtain relative gender association of skills and to visualize and categorize them into skill groups using the HDBSCAN clustering algorithm. Secondly, it provides the code to obtain sentence embeddings and to cluster job ads into occupation groups using job titles and descriptions. The repository also provides the model trained on over 250,000 unique job descriptions posted on the National Career Services (NCS) portal (https://www.ncs.gov.in/) in India. For complete details refer to Chaturvedi, S., Mahajan K., & Siddique, Z. (2023). "Using Domain-Specific Word Embeddings to examine the Demand for Skills". The files are divided into: code, data, and model folders.

Please direct any questions to Sugat Chaturvedi at sugat.chaturvedi@gmail.com.

The Jupyter notebooks (containing the Python code) are run on Google Colab with Intel(R) Xeon(R) CPU @ 2.20GHz CPU on Ubuntu 22.04.2 LTS operating system with 12.68 GB RAM. Software version: Python 3.10.12.

**Dependencies**:
pandas==1.3.5
fasttext==0.9.2
gensim==4.2.0
scikit-learn==1.0.2
adjustText==0.8
scipy==1.7.3
umap-learn==0.5.4
hdbscan==0.8.33
numpy==1.21.6
matplotlib==3.2.2

-	The file for the model trained on the NCS data is contained within "model/jobs_fasttext.zip" file. To run the code first unzip this file and upload the all files along with your data file containing job titles, descriptions, and a column containing comma separated list of skills in the data folder. A small sample data file "data/skills_jd.csv" with 100 randomly chosen unique titles-descriptions-skills combinations is provided for reference. Simply follow the directory structure as given.

-	The code can be executed on Google Colab by first uploading the data on Google drive. In both the Colab notebooks replace the filename "skills_jd.csv" with the name of your input data file. Then mount the drive on Colab and run the first code block to install the dependencies. Thereafter, comment this code snippet and execute the "Restart and run all" option from the runtime menu. For running specific components follow the comments inside the code files.

**Code files**:
-	The file "code/domain_specific_embeddings.ipynb" trains a fastText model and uses these to obtain domain specific embeddings, find relative gender association of skills, and cluster and visualize them.
-	The file "code/fasttext_occupation_classification.ipynb" uses the trained model to cluster job ads into occupation groups using k-means clustering and obtains their labels using job titles.
