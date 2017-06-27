
# Code
The assignment code is split up into 3 folders, Task1 Task2 and Task3. Inside each folder are the relevant models needed for the tasks. 

To run the model simply restart and run the kernal for all scripts.


## Task 1: Classification
Contains the 8 notebooks, each for a specific model. To check the reults are as in the report simply run all the cells.

One thing to note is that since the time take to run all the training set is so long, I have set it to run on only $\textbf{10,000}$ images rather than the full 55,000. The results in the report is over the whole data set. If you would like to run over the whole data set simply comment out $\textbf{num_train = len(mnist.train.labels[:10000,:])}$ in the $\textit{print_acc}$ function at the end of each scrpit. I was not sure if you would have time to wait 5 mins to see if it is ok for the 128 models.

Note that the optimizer function has been commented out, otherwise the model would start runnning again.

## Task2: Pixel Prediction
### a) Many_to_many_loss
Simply run all cells. Simlar to the case for the whole train set in Task 1, in part a) the training cost output will be over 10,000 images. Comment out num_train = len(mnist.train.labels[:10000,:]) to get the train cost in the report.

### b) predictions: pixel_in_paint
Simply run all cells. Each model is set up to run different predicted sequence lengths. The GRU 32 will predict 10, GRU 64 will predict 28 and both the 128 and 3 layer will predict 300. If you want to check the other sequence lengths are correct, just change seq_len variable in the code. Note that the outputs of the losses will be silghtly different due to sampling.

## Task 3: Fill in the missing pixels
Simply run the two notebooks to get the losses and accuracies in the report. The two npy files contain the predicted images, appended onto to the original file. 

Both notebooks produce the images of the correct predictions and incorrect predictions in the report.



