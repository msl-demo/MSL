## MSL
Code for our paper *Multi-sensor Learning Enables Information Transfer across CT and MRI and Augments Multi-modality Imaging*.

### Dataset processing
We use the dataset from [RIRE project](https://rire.insight-journal.org/). 
Data are downloaded from the [link](https://rire.insight-journal.org/download_data.html). 

After downloading the CT and MRI T1 files, we register all the paired modality data and save them as paired .nii files.

Raw .nii files are saved in PATH_TO_DATASET/raw_data/.

Then, run the command to obtain .npz files and .png files.

```
cd code
python ./prepare_data/processing_data.py PATH_TO_DATASET
```

### Training and Testing

Splitting the .npz files and .png files into training and testing splits according to the patient id (*i.e.*, the prefix of the files like p001). 

Save the data under PATH_TO_DATASET/train/ and PATH_TO_DATASET/test/. 

Run train.py to train the model and run test.py to get results.


