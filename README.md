# n-gram-models

These databases (in the SQLite format) include n-grams models of abstracted Java sources. The input source codes are stored in an SQLite database named 'java-sources-abstracted_big-20170628'. The original codes (non-abstractised) have been extracted from thedatabase build in the following paper.


E. A. Santos, J. C. Campbell, D. Patel, A. Hindle and J. N. Amaral, "Syntax and sensibility: Using language models to detect and correct syntax errors," 2018 IEEE 25th International Conference on Software Analysis, Evolution and Reengineering (SANER), Campobasso, 2018, pp. 311-322, doi: 10.1109/SANER.2018.8330219.

The database with the abstactised codes includes just one table named 'abstracted_source_files' with two relevant fields: 'hash' and 'source'. In the abstracted version, all identifiers are treated as the same identifier token. The same abstraction is applied to numeric literals and string literals. Due to the size of this database (ca. 10GB), this file has not been added to the repository and is available on request.

The n-gram models from the abstracted souce codes are stored in the databases java-sources-2grams-20170628 to java-sources-6grams-20170628. The n-gram model is stored in the table named 'ngrams'. The subseqent (abstracised) tokens are stored in fields: 's1', 's2', ..., 'sn', whereas the number of occurrences of each n-gram is stored in field 'count', and its occurrence probability are stored in field 'probability'.  

The code abstraction and the n-gram model generation has been done with the tool available at https://github.com/pdziurzanski/code-naturalness-manatee.git.

The authors acknowledge the support of the EPSRC-funded MANATEE project. 
