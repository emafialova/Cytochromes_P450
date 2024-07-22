# Cytochromes P450 

Cytochromes P450 are a superfamily of heme-containing enzymes that play essential roles in natural product and steroid biosynthesis. 

In this repository you can find a Cytochrome P450 database, that consists of reviewed entries from UniProt and Rhea databases. Each entry in a database is one reaction, you can find information regarding the Uniprot code of the enzyme, substrates, products and many more.

## Promiscuous enzymes and SMARTS
A considerbale amount of cytochromes P450 are promiscuous enzymes, meaning that they posses the ability to catalyze reactions of multiple substrates.
These enzymes are in the database represented by several entries for the same uniprot code. 

In the jupyter file called creating_SMARTS.ipynb you can find a way to generalize the reactions that these promiscuous enzymes catalyse. For every promiscuous enzyme, its reactions are split into groups based on the type of reaction, the groups are also studied in terms of similarity of structures. For each created group, a representative SMARTS is created. These SMARTS can be found in the database.

To run the file, you need to install rdkit library and pandas: 
```
pip install rdkit
pip install pandas
```
Here is a link for the rdkit documentation: https://www.rdkit.org/docs/GettingStartedInPython.html

Note: When splitting groups based on a similarity score, the default rdkit score is used (Johnson score). The similarity threshold can be adjusted, all the calculations were done with a 0.75 score. 

## Reactions in the database
A second jupyter file: identify_reactions.ipynb can be used on a dataset to identify the ongoing reactions, the identification process is based on finding the maximum common substructure of the substrate and product.

Not all types of reactions are easily identified (eg. double bond creation or ring synthesis) so some identification is manually added to the script. 

The necessary libraries are: rdkit, pandas and matplotlib.

There is an example output file for the Cytochrome P450 database called reactions_csv.