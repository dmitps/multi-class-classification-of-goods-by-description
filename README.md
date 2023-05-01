<div align="center">
    <h1>Multiclass classification of goods by description</h1>
</div>

<div align="center">
  <img src="./images/Marketplaces.png" alt="Marketplaces">
</div>

Hundreds of new products appear on marketplaces every day. However, it is impossible to check the correctness of filling in the information about all the goods at once. An incorrectly defined category often leads to potentially lost profits from both the seller and marketplaces. We want to learn how to predict a category based on product descriptions.

____

Applied convolutional recurrent neural network (Convolutional Recurrent Neural Network, CRNN). It combines the properties of convolutional neural networks (CNNs) used to process sequences (in our case, texts) and recurrent neural networks (RNNs) that allow modeling long-term dependencies in sequences.

<table align="center" border="1" cellpadding="5">
  <tr>
    <td colspan="3" align="center"><b>CRNN Architecture</b></td>
  </tr>
  <tr>
    <td align="center"><b>Layer Type</b></td>
    <td align="center"><b>Parameters</b></td>
    <td align="center"><b>Output Shape</b></td>
  </tr>
  <tr>
    <td align="center">Input</td>
    <td align="center">shape=input_shape, name='text'</td>
    <td align="center">-</td>
  </tr>
  <tr>
    <td align="center">Embedding</td>
    <td align="center">input_dim=10000, output_dim=128</td>
    <td align="center">-</td>
  </tr>
  <tr>
    <td align="center">Conv1D</td>
    <td align="center">filters=64, kernel_size=3, padding='valid', activation='relu'</td>
    <td align="center">-</td>
  </tr>
  <tr>
    <td align="center">MaxPooling1D</td>
    <td align="center">pool_size=2</td>
    <td align="center">-</td>
  </tr>
  <tr>
    <td align="center">Bidirectional LSTM</td>
    <td align="center">units=64, dropout=0.2, recurrent_dropout=0.2</td>
    <td align="center">-</td>
  </tr>
  <tr>
    <td align="center">Dense</td>
    <td align="center">units=64, activation='relu'</td>
    <td align="center">-</td>
  </tr>
  <tr>
    <td align="center">Dense</td>
    <td align="center">units=num_classes, activation='softmax'</td>
    <td align="center">-</td>
  </tr>
  <tr>
    <td colspan="3" align="center"><i>Output</i></td>
  </tr>
</table>

#### Implementation features:
 * The project is made on text signs
 * All nested dictionaries and lists are unpacked
 * Lemmatization was not applied, since this method somewhat reduced the metric for our data
 * Applied a number of callbacks to protect against retraining the model
 * Model weights saved
 * Applied stratification when dividing data
 * Used TensorBoard extension for Jupyter Notebook
