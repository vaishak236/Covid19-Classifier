NOTE : Each of these folders below also contains README files to describe the contents of each folder.

The unet models in  the hw5_layer, 4_layer, 6_layers and 5_layer_stride_4 folders use the DiceLoss function

The unet models in  the BCE folder use the BCELogitLoss function

The best model is present in the "best_model" folder

|-----------------------------------------------------------------------------------------------------------------------------------------------|
|Folder Name        |  Folder Description																            |
|-------------------|---------------------------------------------------------------------------------------------------------------------------|
|hw5_layer	        |  This folder contains the code for 5 layer Monai model used in Homework 5. This unet model                                |
|		        |  has channels = (32, 64, 128, 256, 512) and strides = (2, 2, 2,2). Loss function used = DiceLoss The results and	      |
|		        |  graphs of this model are saved as png files										                  |
|-------------------|---------------------------------------------------------------------------------------------------------------------------|
|4_layer            |  This folder contains the code for 4 layer Monai model. This unet model has channels = (64, 128, 256, 512)                |
|		        |  and strides = (2, 2, 2). Loss function used = DiceLoss The results and graphs of this model are saved as png files.      |                         
|-------------------|---------------------------------------------------------------------------------------------------------------------------|
|6_layers           |  This folder contains the code for 6 layer Monai model. This unet model has channels = (32, 64, 64, 128, 256, 512)        | 
|		        |  and strides = (2, 2, 2,2,2). Loss function used = DiceLoss The results and graphs of this model are saved as png files   |                             
|-------------------|---------------------------------------------------------------------------------------------------------------------------|
|5_layer_stride_4	  |  This folder contains the code for 5 layer Monai model where value of the strides are inccreased. This unet               |
|			  |  model has channels = (32, 64, 128, 256, 512) and strides = (4, 4, 4,4). Loss function used = DiceLoss.                   |
|			  |  The results and graphs of this model are saved as png files.                                            	            |                                                                                              
|-------------------|---------------------------------------------------------------------------------------------------------------------------|
|BCE (this has sub- |  This folder contains the code of pytorch model (in the "pytorch" subfolder) and Monai model (in the "monai" subfolder)   |
|folders "pytorch"  |  Both the models have to same number of layers, however the pytorch model is created using the convolutional layers using |
|and "monai"        |  pytorch library and the monai unet model is created using the convolutional blocks provided by monai.                    |
|                   |  These models use the BCE loss function insstead of dice loss											|
|-------------------|---------------------------------------------------------------------------------------------------------------------------|
|best_model         |  This folder contains the model files of the best performing models and also the ipymb files of the specific unet models  |
|                   |  being tested. the ipymb files are:															|
|			  |																					|
|			  |  1) testing-monai-ADN-70-epochs : contains the monai unet model created using ADN Blocks trained for 70 epochs		|
|                   |  2) testing-monai-ADN-200-epochs : contains the monai unet  created using ADN Blocks trained for 200 epochs			|
|			  |  3) testing-monai-replicate-noADN : contains the monai unet model created Conv2d blocks						|
|                   |  4) testing-monai-2 : contains the imported monai unet model											|
|                   |  5) testing-pytorch -best model val : This is a model created using pytorch modules and gave the best dice score and this |
|			  |     best performing model is applied on the testing dataset for  visualization								|
|-------------------|---------------------------------------------------------------------------------------------------------------------------|
|miscellaneous      |  This folder contains the ipymb file(Preprocessing.ipymb) used to preprocess the data and tar_extractor.ipymb used to     |
|                   |  extract the data. 																		|
|-------------------|---------------------------------------------------------------------------------------------------------------------------|