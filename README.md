# Cytochromes P450 

Cytochromes P450 are a superfamily of heme-containing enzymes that play essential roles in natural product and steroid biosynthesis. 

Part of this repository is our Cytochrome P450 database, that consists of reviewed entries from UniProt and Rhea databases.

## Promiscuous enzymes and SMARTS
A considerbale amount of cytochromes P450 are promiscuous enzymes, meaning that they posses the ability to catalyze reactions of multiple substrates.
These enzymes are in our database represented with several entries. 

In the jupyter file called creating_SMARTS.ipynb you can find a way to generalize the reactions that these promiscuous enzymes catalyse. The results are SMARTS (extension of SMILES).

Note: When creating groups based on a similarity score, the default rdkit score is used (Johnson), the similarity threshold is set to 0.75 and all calculations were done with this score. 

The generalization is done using the rdkit library, here is a link for the library documentation: https://www.rdkit.org/docs/GettingStartedInPython.html

## Reactions in the database
A second jupyter file: final_reactions.ipynb can be used on a dataset to identify the ongoing reactions, the rdkit library is again used for the identification.
Not all types of reactions are easily identified (eg. double bond creation or ring synthesis) so some identification is manually added.
