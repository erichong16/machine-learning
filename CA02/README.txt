README - CA02
This code utilizes the Naive Bayes Theorem through the GaussianNB method
to determine whether the testing mails are spam or not.

Prior to using this algorithm, two functions have been created.

The first function, make_dictionary, gets fed all the mails from the 
training directory. These mails will have all their words split by white spaces
and saved in a list. Items with 1 letter or non alphabetical symbol will be removed.
The dictionary would only take in the 3000 most frequent words used out of all the files.


The second function, extract_features, takes will be taking in mails from 
both the training and testing directories. First, it will be trained using the 
training directory and the features matrix will consist of rows made up of
the number of files and columns made up of the 3000 most common words that were
found in the previous make_dictionary function. 

Each file will be indexed by docID and if any word exists in the dictionary,
the occurences of that specified word will be recorded on the feature matrix
based on doc and wordID.

After that, as the function iterates through each file, filenames that starts 
with 'spmsg' will be labeled as spam and others as nonspam.

This feature matrix and label will be used down below with the GaussianNB method to
determine whether a mail is spam or not for the mails in the testing directory.

Prior to testing, I mounted my google drive to the specified directories before
passing them in to train and test the model.