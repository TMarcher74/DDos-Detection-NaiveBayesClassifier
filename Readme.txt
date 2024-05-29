The size of the Dataset is 10GB (ordered being 6 and unordered being 4), you can find them in the link attached below.
https://www.kaggle.com/datasets/devendra416/ddos-datasets

Trying to train the model on your laptop is a very "Naive" thing to do, it needs more than 32GB RAM, and hence why we had to cutdown our dataset while looking for online services like Kaggle and Google Collab.

We had decided to use the ordered dataset and tried training the model on kaggle where we ran into problems like shortage of memory (>30GB) and slow processing speeds.

We then decided to use the first 25% of the dataset but the dataset is ordered in such a way that, DDoS makes up for the first 50% and benign the other 50%. Dividing the dataset into chunks and training the model on these chunks did not work either (for obvious reasons in hindsight).

Finally deciding to use the first 12.5% of the dataset and the last 12.5% did the trick, so as to include equal number of both DDoS and Benign connections. Giving us a satisfying accuracy of > 80%.