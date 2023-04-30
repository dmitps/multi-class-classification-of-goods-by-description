<div id="header" align="center">
    <h1>Multi-class classification of goods by description</h1>
</div>

<div id="picture" align="center"
    <a href="https://github.com/dmitps/multi-class-classification-of-goods-by-description/blob/main/Marketplaces.png">
        <img src="https://github.com/dmitps/multi-class-classification-of-goods-by-description/blob/main/Marketplaces.png">
    </a>
</div>

Hundreds of new products appear on marketplaces every day. However, it is impossible to check the correctness of filling in the information about all the goods at once. An incorrectly defined category often leads to potentially lost profits from both the seller and marketplaces. We want to learn how to predict a category based on product descriptions.

____

Applied convolutional recurrent neural network (Convolutional Recurrent Neural Network, CRNN). It combines the properties of convolutional neural networks (CNNs) used to process sequences (in our case, texts) and recurrent neural networks (RNNs) that allow modeling long-term dependencies in sequences.

**Implementation features:**
 * the project is made on text signs
 * all nested dictionaries and lists are unpacked
 * lemmatization was not applied, since this method somewhat reduced the metric for our data
 * applied a number of callbacks to protect against retraining the model
 * model weights saved
 * applied stratification when dividing data
 * used TensorBoard extension for Jupyter Notebook
