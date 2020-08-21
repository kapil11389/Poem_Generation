<p><span style="font-size: 12pt;"><strong><span style="font-family: helvetica;"><span style="text-decoration: underline;">Poem Generation</span><br /></span></strong></span></p>
<p><span style="font-size: 10pt;">This project utilizes the concept of Recurrent Neural Networks and the uses the benefits of LSTM over Recurrent Neural Networks(RNN).</span><br /><span style="font-size: 10pt;">The reason behind using LSTM is because while generating text, context is important. Which word comes after whom differentiates the sentence from being deep or profound to downright non-sensical.</span></p>
<p><span style="font-size: 10pt;">Steps involved in the procedure:</span></p>
<p><span style="font-size: 10pt;">1. <strong> Importing Dependencies</strong><br />Required: Keras, Pandas, Numpy<br /></span></p>
<p><span style="font-size: 10pt;">2. <strong>Importing Data</strong><br />Here the data contained in 'sonnets.txt' is the full compilation of Shakespeare's literary works containing poems.</span></p>
<p><span style="font-size: 10pt;">3. <strong>Character Mapping</strong><br />This step is required as the RNN's work much better with numbers than with text. And moreover text is anyway converted to numerical representation anyway.</span></p>
<p><span style="font-size: 10pt;">4. <strong>Data Preprocessing</strong><br />The data that is input to the network must be reshaped such that training data and testing data can be created. Further, how context would be stored would be decided.</span></p>
<p><span style="font-size: 10pt;">5. <strong>Modelling</strong><br />Due to limitations of my current machine and the complete absence of GPU has limited the amount of neurons that can be trained. I am using 3 LSTM layers with 400 neurons each and 3 dropout layers each having a drop ratio of 20%.&nbsp;<br />Finally, the output goes through a Dense layer which finally gives out the output.<br />The activation function can be experimented with to give out better or equal results.</span></p>
<p><span style="font-size: 10pt;">Epochs: 100<br />Batch_size: 100</span></p>
<p><span style="font-size: 10pt;">6. <strong>Generating text</strong><br />We finally use the generated model to predict one character at a time. We use this characters and generate another character and the cycle goes on.</span></p>
<p>&nbsp;</p>
<p><strong><span style="font-size: 10pt;">Observations:<br /><br /></span></strong><span style="font-size: 10pt;">Due to the limitations of the machine I am using and no GPU support, the model currently is able to :</span></p>
<ul>
<li><span style="font-size: 10pt;">create words with proper spelling (most of time)</span></li>
<li><span style="font-size: 10pt;">understands rhyming and tries to incorporate a rhyme scheme</span></li>
<li><span style="font-size: 10pt;">understands the spaces and newlines such that it doesn't create very long sentences.</span></li>
</ul>
<p>I am sure better results can be expected by tinkering around with the number of neurons and number of layers while thinking about the vanishing gradient problem.</p>
