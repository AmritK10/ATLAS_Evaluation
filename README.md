# ATLAS_Evaluation

## Task
To prepare an autoencoder to compress the four-momentum of a sample of simulated particles from 4 to 3 variables.

## Mean Squared Error(MSE) Achieved
The Mean Squared Error(MSE) is a metric used to calculate the error in the fit.<br>
The lower the error the better the fit. <br>
The MSE of 1.03e-05 was achieved by the model. <br>
Such a low error depicts the goodness of fit of the model.

## Files

### Data_pre-processing.ipynb
This Jupyter notebook performs the data pre-processing and manipulation on the extracted jet objects data. <br>
The file prepares the data to be input to the autoencoder. The broad steps followed in the file are:
<ul>
  <li>Extracting relevant data by reading the csv file</li>
  <li>Splitting the data into train and test data on 80:20 ratio</li>
  <li>Forming dataframes from the data</li>
  <li>Visualising and analysing the data as histograms and on the basis of general statistics</li>
  <li>Normalising the data due to the huge difference in the ranges of the variables</li>
  <li>Variables E and pt undergo log base 10 transformations</li>
  <li>Variables eta and phi undergo division by 3</li>
  <li>Visualising and analysing the normalised data as histograms and on the basis of general statistics</li>
  <li>Pickling and storing the normalised dataframes</li>
</ul>

#### Plots depicting the original and normalised data:
The plots have the value of the variable on the x axis and the number of events possessing a particular value on the y axis.
##### Plot for variable E
<p align="center">
  <img src="https://user-images.githubusercontent.com/31596604/111080493-b95b0900-8524-11eb-8bd5-29eef9c1a856.png" width="500" title="fourmomentum_E">
</p>

##### Plot for normalised variable E
<p align="center">
  <img src="https://user-images.githubusercontent.com/31596604/111080661-82d1be00-8525-11eb-8f20-9cbf564fc8c5.png" width="500" title="normalized_fourmomentum_E">
</p>

##### Plot for variable eta
<p align="center">
  <img src="https://user-images.githubusercontent.com/31596604/111080495-bbbd6300-8524-11eb-90c0-52d22cd65a14.png" width="500" title="fourmomentum_eta">
</p>

##### Plot for normalised variable eta
<p align="center">
  <img src="https://user-images.githubusercontent.com/31596604/111080663-85341800-8525-11eb-8b8b-3fb223c91c5b.png" width="500" title="normalized_fourmomentum_eta">
</p>

##### Plot for variable phi
<p align="center">
  <img src="https://user-images.githubusercontent.com/31596604/111080496-bcee9000-8524-11eb-93b6-11debb2322cd.png" width="500" title="fourmomentum_phi">
</p>

##### Plot for normalised variable phi
<p align="center">
  <img src="https://user-images.githubusercontent.com/31596604/111080664-86654500-8525-11eb-9297-082f734256b9.png" width="500" title="normalized_fourmomentum_phi">
</p>

##### Plot for variable pt
<p align="center">
  <img src="https://user-images.githubusercontent.com/31596604/111080497-bcee9000-8524-11eb-8139-b40b119ea25a.png" width="500" title="fourmomentum_pt">
</p>

##### Plot for normalised variable pt
<p align="center">
  <img src="https://user-images.githubusercontent.com/31596604/111080665-86fddb80-8525-11eb-81c1-639be78a9761.png" width="500" title="normalized_fourmomentum_pt">
</p>

### TLA_4D_Example.ipynb
This Jupyter notebook runs the autoencoder on the pre-processed jet objects data. <br>
The file trains and tests the autoencoder and produces histograms to depict the fit. 

#### Plots depicting the fit:
The plots depict the input and output plotted on the same space. Blue depicts the input and yellow depicts the output. <br>
The input refers to the 4 variables sent to the network.<br>
The output refers to the 4 variables being compressed to 3 and then decompressed back to 4. <br>
The network was trained and tested on the normalised data. <br>
To view the results on the original data, we unnormalise the input and output. <br>
One can see that the input (blue) and output (yellow) are very close in simliarity, depicting the goodness of the fit. <br>

##### Plot for fit of variable E
<p align="center" background-color="white">
  <img src="https://user-images.githubusercontent.com/31596604/111082064-58373380-852c-11eb-90a4-c5e1c65ee811.png" width="500" title="fourmomentum_E">
</p>

##### Plot for fit of normalised variable E
<p align="center">
  <img src="https://user-images.githubusercontent.com/31596604/111082062-553c4300-852c-11eb-9623-5745eb84595a.png" width="500" title="normalized_fourmomentum_E">
</p>

##### Plot for fit of variable eta
<p align="center">
  <img src="https://user-images.githubusercontent.com/31596604/111082068-59686080-852c-11eb-8a64-7b3cedbb57f4.png" width="500" title="fourmomentum_eta">
</p>

##### Plot for fit of normalised variable eta
<p align="center">
  <img src="https://user-images.githubusercontent.com/31596604/111082066-58cfca00-852c-11eb-9b14-c5a375bac8ea.png" width="500" title="normalized_fourmomentum_eta">
</p>

##### Plot for fit of variable phi
<p align="center">
  <img src="https://user-images.githubusercontent.com/31596604/111082073-5b322400-852c-11eb-8991-a1d714c2b306.png" width="500" title="fourmomentum_phi">
</p>

##### Plot for fit of normalised variable phi
<p align="center">
  <img src="https://user-images.githubusercontent.com/31596604/111082069-5a00f700-852c-11eb-8426-cf4083910061.png" width="500" title="normalized_fourmomentum_phi">
</p>

##### Plot for fit of variable pt
<p align="center">
  <img src="https://user-images.githubusercontent.com/31596604/111082077-5c635100-852c-11eb-95bf-41c833a1bc8b.png" width="500" title="fourmomentum_pt">
</p>

##### Plot for fit of normalised variable pt
<p align="center">
  <img src="https://user-images.githubusercontent.com/31596604/111082075-5bcaba80-852c-11eb-8971-97a9f9398910.png" width="500" title="normalized_fourmomentum_pt">
</p>
