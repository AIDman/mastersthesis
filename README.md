# Speech-based identification of children's gender and age with neural networks
### Leo Kristopher Piel's Master's Thesis
This is a repository for Leo Kristopher Piel's Master's thesis. It contains code for the built models and conducted expoeriments. 
  
**NB!** The code cannot be run, because the training, validation and test data are not included in this repository. 
### Project structure
#### Folders
* **baseline:** contains files related to baseline system predictions analysis.
* **dnn:** contains all the saved feedforward dnn models. Also includes dnn.py predictions in file dnn_predicted_labels.npy that were used as labels for some of the trained RNN models.
* **history:** contains files with information about the training process of all the saved models.
* **models:** contains the saved state of the models. Models were mostly saved during the highest point of validation accuracy in training process. Two of the missing states can be found here:
  * gender_6.hdf5: https://drive.google.com/open?id=1qTjkdjSpG8GSOwSuHSb1wRH3p9twQcdK
  * model_22.hdf5: https://drive.google.com/open?id=1Gc_glXGtS-cmRvlO5e2sNtJaWggR0QE1
* **predictions:** contains models' predictions on validation and test data. Predictions ending with _males.py or _females.py are the ones of the models that were trained on gender specific data. Predictions ending with _males_original.py or _females_original.py are the ones of the models trained on the whole dataset.
* **rnn:** contains all the built RNN models
* **survey:** contains survey results in survey.csv and data analysis.
#### Files
* **History.ipynb:** Jupyter Notebook of the analysis of the training process of the models. Creation of confusion matrices.
* **Results.xlsx:**
  * **Sheet 1:** accuracies of different models on validation and test data.
  * **Sheet 2:** Analysis of data division into age groups.
  * **Sheet 3:** survey results. Same as survey.csv in survey folder.
* **combined_predictions_1.py:** ensemble model, where best models for males' or females' age group identifciation was used after predicting gender.
* **combined_predictions_2.py:** ensemble model, where combination of the best models for males' or females' age group identification was used after predicting gender.
* **merge_predictions.py:** brings out all the results of different models and includes the ensemble models created for boosting the accuracies.
