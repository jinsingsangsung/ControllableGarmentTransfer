# Controllable Garment Transfer

This is a repository of **Controllable Garment Transfer**, a project from Intro to Deep Learning (11685), CMU.
Our project preliminary report can be found [here](https://piazza.com/redirect/s3?bucket=uploads&prefix=paste%2Fjj4ivcv0tvk379%2F6e53b51ac6423b5821abafe166fabb1cdc1ae3cd590933d28b9af99797325d0a%2FNIPS_Template___11785__Copy__%284%29.pdf), so we recommend you to read the report first before implementing our code.


![collar2_debug](https://user-images.githubusercontent.com/76904126/167062152-32327fca-ef8d-4f09-9773-c63e6b497540.gif)
![flower1_debug](https://user-images.githubusercontent.com/76904126/167062160-4977f252-0708-4c3e-a231-f1b7cd462390.gif)

Our Garment Tweaking module, is named InterClothGAN, and has been assigned a new [repository](https://github.com/tcabezon/InterClothGAN).

<img width="568" alt="Inversion_network" src="https://user-images.githubusercontent.com/76904126/167064469-7ab8a698-c123-4a15-b450-5d76d8bbb5e3.png">


## Before you start,

There are datasets you need to download, one for *inversion network* and the other for *dressing in order*.
You can go download CP-Vton dataset [here](https://drive.google.com/drive/folders/1NxESTHGMPpUMCFsvX27N5gDwkYj7ZhoT?usp=sharing) and put the cp-vton folder under the *gan-inversion* directory. You need to split those data into two sets, *train* and *test* and place each folder under the created *cp-vton* directory.

Also, download the dataset from [here](http://mmlab.ie.cuhk.edu.hk/projects/DeepFashion/InShopRetrieval.html) and place it under the data directory of *dressing-in-order*. There is an empty folder with differnet names that indicate where to place dataset at.

### Environment setup (optional)
Under gan-inversion directory, you will see environment.yaml file. Use conda to install environments used for the experiment.

## Run the code


## Result

Our demonstration result can be found [here](https://drive.google.com/drive/folders/13GPKKRMcBbOfDOaVDrYAs9s2GQIvr71Q?usp=sharing).

Garment Tweaking [demo](https://colab.research.google.com/drive/1-QHc6oF_Xthj1Po558gd7dQLZyD9oDuh?usp=sharing) is also available on Google Colab, so please check it out!