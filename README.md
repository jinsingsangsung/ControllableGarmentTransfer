# Controllable Garment Transfer

This is a repository of **Controllable Garment Transfer**, a project from Intro to Deep Learning (11685), CMU.
Our project preliminary report can be found [here](https://piazza.com/redirect/s3?bucket=uploads&prefix=paste%2Fjj4ivcv0tvk379%2F6e53b51ac6423b5821abafe166fabb1cdc1ae3cd590933d28b9af99797325d0a%2FNIPS_Template___11785__Copy__%284%29.pdf), so we recommend you to read the report first before implementing our code.


![collar2_debug](https://user-images.githubusercontent.com/76904126/167062152-32327fca-ef8d-4f09-9773-c63e6b497540.gif)
<!-- ![flower1_debug](https://user-images.githubusercontent.com/76904126/167062160-4977f252-0708-4c3e-a231-f1b7cd462390.gif) -->

Our Garment Tweaking module, is named InterClothGAN, and has been assigned a new [repository](https://github.com/tcabezon/InterClothGAN).

<img width="568" alt="Inversion_network" src="https://user-images.githubusercontent.com/76904126/167064469-7ab8a698-c123-4a15-b450-5d76d8bbb5e3.png">


## Before you start,
### Downloading the Dataset
There are datasets you need to download, one for *inversion network* and the other for *dressing in order*.
You can go download CP-Vton dataset [here](https://drive.google.com/drive/folders/1NxESTHGMPpUMCFsvX27N5gDwkYj7ZhoT?usp=sharing) and put the cp-vton folder under the `gan-inversion/` directory. You need to split those data into two sets, `train/` and `test/` and place each folder under the created `cp-vton/` directory.

Also, download the dataset from [here](http://mmlab.ie.cuhk.edu.hk/projects/DeepFashion/InShopRetrieval.html) and place it under the data directory of `dressing-in-order`. There is an empty folder with differnet names that indicate where to place dataset at.

### Environment setup (optional) and Pretrained Weights
**Gan Inversion**
Under `gan-inversion/` directory, you will see `environment.yaml` file. Use conda to install environments used for the experiment. We have trained an inversion network for Stylegan for garments, whose weights can be downloaded [here](https://drive.google.com/drive/folders/13GPKKRMcBbOfDOaVDrYAs9s2GQIvr71Q?usp=sharing). 
Unzip `weights.zip`. `stylegan1/` has the weights for the stylegan 1 network trained on garment images, which should be placed in the `pretrained_models` folder inside the inversion repo. The pretrained weights for the inversion network can be found in `inversion/`.

## Run the code
**1. Garment Transfer**

For garment transfer, follow the instructions from [DiOR](https://github.com/cuiaiyu/dressing-in-order.git) to set up the environment and the download the pretrained weights. The actual transfer process will be identical to the process in *DiOR*. Pre-processing of all images (Pose extraction, Human Parsing) is required before putting into DiOR. We have used [Yet-Another-Openpose-Implementation](https://github.com/MikeOfZen/Yet-Another-Openpose-Implementation.git) and [Self-correction-Human-Parsing](https://github.com/GoGoDuck912/Self-Correction-Human-Parsing.git) to work well for these tasks.

**2. Gan Inversion (Optional)**

If you want to try editing with custom images (rather than StyleGAN generated images), you must first project them into StyleGAN space to find the closest embedding that???ll yield a similar garment image. Run `scripts/inference.py` to get the reconstructed StyleGAN image and its latent vector.

**3. Garment Tweaking**

For tweaking, we provide you with a [colab notebook](https://drive.google.com/drive/folders/13GPKKRMcBbOfDOaVDrYAs9s2GQIvr71Q?usp=sharing). Head over to [InterClothGAN](https://github.com/tcabezon/InterClothGAN/tree/ec271c773e03d9da465523a503402d28c7001752) for the full repo.

## Result

We have gathered our result images in a [google drive](https://drive.google.com/drive/folders/13GPKKRMcBbOfDOaVDrYAs9s2GQIvr71Q?usp=sharing).
Also, please check out the [colab demo](https://drive.google.com/drive/folders/13GPKKRMcBbOfDOaVDrYAs9s2GQIvr71Q?usp=sharing) for garment tweaking!

