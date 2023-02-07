SoulVest Impact Scoring - Technical process

The objective of the SoulVest Impact Scoring tool (SVIS) is to provide [predictive] analytics that will allow finance companies and pre seeds projects to choose to fund the projects that are most likely to have a positive impact on the ecosystem.

>>> Install requirements with "pip install -r requirements.txt"

https://raw.githubusercontent.com/adeline-hub/SoulVest-Impact-Scoring-/main/requirements.txt The code is written in python, saved in .ipynb file. to open .ipynb file you should set up Jupyter Lab environment: https://jupyter.org/install. So you may check if you have all for running this code thanks to the requirements.txt

>>> Training data SISanalysis.py with a sentiment analysis, scrapes profile information and comment threads from:

project pages on SoulVest's website,
investee candidates’ forms,
investee’s website or presentation. then it creates a CSV file [trainingset.csv] containing the information obtained
>>> Building a model and scoring SIS_page.py

interrogates the SoulVest selected metrics and sources for Impact, ESG and extra financial criteria,
collects basic profile information from the first several currently funding projects on SIS_page.py,
trains a Gaussian GLM on the training data in trainingset.csv,
and assigns predicted impact scores to the new entity based on the model. Output is a csv with the Entity information and scores.
