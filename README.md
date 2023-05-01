<div align="center">
    <h1>Multiclass classification of goods by description</h1>
</div>

<div align="center">
  <img src="./images/Marketplaces.png" alt="Marketplaces">
</div>

Hundreds of new products appear on marketplaces every day. However, it is impossible to check the correctness of filling in the information about all the goods at once. An incorrectly defined category often leads to potentially lost profits from both the seller and marketplaces. We want to learn how to predict a category based on product descriptions.

____

Applied convolutional recurrent neural network (Convolutional Recurrent Neural Network, CRNN). It combines the properties of convolutional neural networks (CNNs) used to process sequences (in our case, texts) and recurrent neural networks (RNNs) that allow modeling long-term dependencies in sequences.

**Implementation features:**
 * The project is made on text signs
 * All nested dictionaries and lists are unpacked
 * Lemmatization was not applied, since this method somewhat reduced the metric for our data
 * Applied a number of callbacks to protect against retraining the model
 * Model weights saved
 * Applied stratification when dividing data
 * Used TensorBoard extension for Jupyter Notebook
