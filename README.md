<h2>TensorFlow-FlexUNet-Image-Segmentation-FracAtlas-Fracture (2026/10/15)</h2>
Sarah T. Arai<br>
Software Laboratory antillia.com<br><br>

This is the first experiment of Image Segmentation for <b>FracAtlas-Fracture </b>
 based on
our <a href="https://github.com/sarah-antillia/TensorFlow-FlexUNet-Image-Segmentation-Model">TensorFlowFlexUNet Model</a>
 (<b>TensorFlow Flexible UNet Image Segmentation Model for Multiclass</b>) and a 512x512-pixel cropped PNG
 <a href="https://drive.google.com/file/d/1iOIJBXknScpadLazpjVnEFaz9qoupuxD/view?usp=sharing">
Augmented-FracAtlas-Fracture-ImageMask-Dataset.zip</a> 
(<a href="https://creativecommons.org/licenses/by-nc-sa/4.0/">CC BY-NC-SA 4.0</a>
), 
which was derived by us from the Kaggle  
<br><br>
<a href="https://www.kaggle.com/datasets/shyamgupta196/fracatlas/data">
<b>FracAtlas Annotated Fracture Imagesn</b>
</a> by SHYAM GUPTA.
<br><br>
<hr>
<b>Actual Image Segmentation for FracAtlas-Fracture Images of 512x512 pixels</b><br>
As shown below, the inferred masks resemble the ground-truth masks exceot for the third case. <br>
<br>
<table>
<tr>
<th width="320" height="auto">Input: image</th>
<th width="320" height="auto">Mask (ground_truth)</th>
<th width="320" height="auto">Prediction: inferred_mask</th>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/mini_test/images/hflipped_IMG0001640.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/mini_test/masks/hflipped_IMG0001640.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/mini_test_output/hflipped_IMG0001640.png" width="320" height="auto"></td>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/mini_test/images/hflipped_IMG0004067.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/mini_test/masks/hflipped_IMG0004067.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/mini_test_output/hflipped_IMG0004067.png" width="320" height="auto"></td>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/mini_test/images/IMG0002454.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/mini_test/masks/IMG0002454.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/mini_test_output/IMG0002454.png" width="320" height="auto"></td>
</tr>
</table>
<hr>
<br>
<h3>1. Dataset Citation</h3>
The dataset used here was derived from the following Kaggle:<br><br>
<a href="https://www.kaggle.com/datasets/shyamgupta196/fracatlas/data">
<b>FracAtlas Annotated Fracture Imagesn</b>
</a> <br>
Comprehensive Collection of Fracture Images for Medical Research and Analysis
<br>
by SHYAM GUPTA.
<br><br>
The following explanation was taken from the website above<br><br>
<b>About Dataset</b><br>
The majority of the existing X-Ray datasets are either very small in size to be used in training machine 
learning models or lack proper annotation to be used in localization and segmentation. 
This creates a limitation while comparing different state-of-the-art (SOTA) methods as each study uses 
its own set of data that is not made public. It also hinders the development of machine-learning algorithms 
for classification, localization and segmentation. In this work, we introduce a new dataset of more than 
14,000 X-Ray scans which was collected from 3 major hospitals in Bangladesh. <br>
From this raw data, we isolated 4,083 images which have been manually annotated for classification, 
localization and segmentation of bone fractures with the help of 2 expert radiologists and later validated 
by a medical officer. Each scan in the dataset was independently labeled by both radiologists and later 
confirmed by the medical officer. <br>
The annotation was done with the help of makesense.ai, an open-source labeling platform. 
All the scans are available in JPG format along with proper annotations.
<br><br>
<b>Citation</b><br>
<pre>
@article { Abedeen_2023,
  title = {{FracAtlas}: A Dataset for Fracture Classification, Localization and Segmentation 
            of Musculoskeletal Radiographs},
  author = {Iftekharul Abedeen and Md. Ashiqur Rahman and Fatema Zohra Prottyasha and Tasnim Ahmed and 
             Tareque Mohmud Chowdhury and Swakkhar Shatabda},
  year = 2023,
  month = {aug},
  journal = {Scientific Data},
  publisher = {Springer Science and Business Media {LLC}},
  volume = 10,
  number = 1,
  doi = {10.1038/s41597-023-02432-4},
  url = {https://doi.org/10.1038%2Fs41597-023-02432-4}
}
</pre>
<br>
<b>License</b><br>
<a href="https://creativecommons.org/licenses/by-nc-sa/4.0/">CC BY-NC-SA 4.0</a>
<br>
<br>
<h3>
2 FracAtlas-Fracture Ultrasound ImageMask Dataset
</h3>
<h3>2.1 Download ImageMask Dataset</h3>
 If you would like to train this FracAtlas-Fracture Segmentation model,
 please download the dataset from Google Drive  
 <a href="https://drive.google.com/file/d/1iOIJBXknScpadLazpjVnEFaz9qoupuxD/view?usp=sharing">
Augmented-FracAtlas-Fracture-ImageMask-Subset.zip</a>. 
Expand the downloaded ImageMaskDataset and put it under the <b>./dataset</b> folder.
<br>
<pre>
./dataset
└─FracAtlas-Fracture
    ├─test
    │   ├─images
    │   └─masks
    ├─train
    │   ├─images
    │   └─masks
    └─valid
         ├─images
         └─masks
</pre>
<br>
<b>FracAtlas-Fracture Statistics</b><br>
<img src ="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/FracAtlas-Fracture_Statistics.png" width="512" height="auto"><br>
<br>
As shown above, the number of images in the training and valid datasets is large enough to use for the
 training set of our segmentation model.
<br>
<h3>2.2 Derivation of ImageMask Dataset</h3>
The folder structure of the original facture dataset  
</a> is as follows.
<pre>
./facture
 ├─test
 │   ├─ann  ( 61 JSON files)
 │   │
 │   └─img  ( 61 JPG files)
 ├─train
 │   ├─ann  (574 JSON files)
 │   │
 │   └─img  (574 JPG files)
 │ 
 └─val   
      ├─ann  ( 82 JSON files)
      │
      └─img  ( 82 JPG files)
</pre>
<b>Step 1</b><br>
We geneated a 512x512-pixel cropped ImageMask dataset from the original JPG files and <b>polygon points exterior data</b> 
in corresponding JSON annotation files in test, train and val subfolders.
<br><br>
<b>Step 2</b><br>
As shown above, the number of JPG and the corresponding JSON annotation files is small to use as a training dataset
of our segmentation model. Therefore, we generated our own augmented dataset from the cropped ImageMask dataset
by applying classic flipping and rotating operations to the cropped one.
<br><br>
<b>Step 3</b><br>
We generated a pretrained FlexUNet model by using the augmented dataset obtained in <b>Step 2</b>.
<br><br>
<b>Step 4</b><br>
We generated the second masks from the cropped images by applying a segmentation method of the 
pretrained FlexUNet model.
<br><br>
<b>Step 5</b><br>
We finally generated the second <a href="https://drive.google.com/file/d/1iOIJBXknScpadLazpjVnEFaz9qoupuxD/view?usp=sharing">Augmented-FracAtlas-Faction-ImageMaskDataset</a>
from all pairs of the cropped images and the corresponding second masks by applying 
flipping and rotating augmentation tools to the pairs.
<br><br>

<h3>2.3 Train Sample Images and Masks</h3>
<b>Train_sample_images</b><br>
<img src="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/asset/train_images_sample.png" width="1024" height="auto">
<br>
<b>Train_sample_masks</b><br>
<img src="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/asset/train_masks_sample.png" width="1024" height="auto">
<br>

<h3>
3 Train TensorFlowFlexUNet Model
</h3>
 We trained the FracAtlas-Fracture TensorFlowFlexUNet model using the following
<a href="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/train_eval_infer.config"> <b>train_eval_infer.config</b></a> file. <br>
Please move to ./projects/TensorFlowFlexUNet/FracAtlas-Fracture and run the following bat file.<br>
<pre>
>1.train.bat
</pre>
This runs the following command.<br>
<pre>
>python ../../../src/TensorFlowFlexUNetTrainer.py ./train_eval_infer.config
</pre>
<hr>

<b>Model parameters</b><br>
Defined a small <b>base_filters=16 </b> and large <b>base_kernels=(11,11)</b> for the first Conv Layer of Encoder Block of 
<a href="./src/TensorFlowFlexUNet.py">TensorFlowFlexUNet.py</a> 
and a large <b>num_layers=8</b> (including a bridge between Encoder and Decoder Blocks).
<pre>
[model]
; You may specify your own UNet class derived from our TensorFlowFlexModel
model         = "TensorFlowFlexUNet"
generator     =  False
image_width    = 512
image_height   = 512
image_channels = 3
num_classes    = 2
base_filters   = 16
base_kernels   = (11,11)
num_layers     = 8
dropout_rate   = 0.04
; Specified a large dilation.
dilation       = (3,3)
</pre>
<b>Learning rate</b><br>
Defined a small learning rate.  
<pre>
[model]
learning_rate  = 0.00007
</pre>
<b>Loss and metrics functions</b><br>
Specified "categorical_focal_dice_loss" and <a href="./src/dice_coef_multiclass.py">"dice_coef_hybrid"</a>.<br>
<pre>
[model]
loss           = "categorical_focal_dice_loss"
metrics        = ["dice_coef_hybrid"]
hybrid_alpha   = 1.6
hybrid_beta    = 0.4
</pre>
<b>Dataset class</b><br>
Specifed <a href="./src/ImageCategorizedMaskDataset.py">ImageCategorizedMaskDataset</a> class.<br>
<pre>
[dataset]
class_name    = "ImageCategorizedMaskDataset"
</pre>
<br>
<b>Learning rate reducer callback</b><br>
Enabled the learning_rate_reducer callback and a small reducer_patience.
<pre> 
[train]
learning_rate_reducer = True
reducer_factor     = 0.4
reducer_patience   = 4
</pre>
<b>Early stopping callback</b><br>
Enabled early stopping callback with the patience parameter.
<pre>
[train]
patience      = 10
</pre>

<b>RGB Color map</b><br>
Specified RGB color map dict for FracAtlas-Fracture 2 classes.<br>
<pre>
[mask]
mask_datatype= "categorized"
mask_file_format = ".png"
; FracAtlas-Fracture RGB color map dict for 1+1 classes.
;      Background: black, Fracture: green
rgb_map = {(0,0,0):0,(0,255,0):1,}
</pre>

<b>Epoch change inference callback</b><br>
Enabled <a href="./src/EpochChangeInferencer.py">epoch_change_infer callback</a></b>.<br>
<pre>
[train]
epoch_change_infer       = True
epoch_change_infer_dir   =  "./epoch_change_infer"
num_infer_images         = 6
</pre>

By using this callback, on every epoch change, the inference procedure can be called
 for 6 images in the <b>mini_test</b> folder. This will help you confirm how the predicted mask changes 
 at each epoch during your training process.<br> 
<br> 
As shown below, early in the model training, the predicted masks from our FlexUNet segmentation model showed 
discouraging results.
 However, as training progressed through the epochs, the predictions gradually improved. 
 <br> 
<br>
<b>Epoch_change_inference output at starting (epoch 1,2,3)</b><br>
<img src="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/asset/epoch_change_infer_at_start.png" width="1024" height="auto"><br>
<br>
<b>Epoch_change_inference output at middlepoint (epoch 16,17,18)</b><br>
<img src="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/asset/epoch_change_infer_at_middle.png" width="1024" height="auto"><br>
<br>
<b>Epoch_change_inference output at ending (epoch 34,35,36)</b><br>
<img src="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/asset/epoch_change_infer_at_end.png" width="1024" height="auto"><br>
<br>
In this experiment, the training process was stopped at epoch 31 by EarlyStoppingCallback.<br>
<img src="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/asset/train_console_output_at_epoch36.png" width="1024" height="auto"><br>
<br>
<a href="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/eval/train_metrics.csv">train_metrics.csv</a><br>
<img src="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/eval/train_metrics.png" width="520" height="auto"><br>
<br>
<a href="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/eval/train_losses.csv">train_losses.csv</a><br>
<img src="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/eval/train_losses.png" width="520" height="auto"><br>
<br>
<h3>
4 Evaluation
</h3>
Please move to <b>./projects/TensorFlowFlexUNet/FracAtlas-Fracture</b> folder,<br>
and run the following bat file to evaluate the TensorFlowUNet model for FracAtlas-Fracture.<br>
<pre>
./2.evaluate.bat
</pre>
This runs the following command.
<pre>
python ../../../src/TensorFlowFlexUNetEvaluator.py ./train_eval_infer.config
</pre>

Evaluation console output:<br>
<img src="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/asset/evaluate_console_output_at_epoch36.png" width="1024" height="auto">
<br><br>Image-Segmentation-FracAtlas-Fracture

<a href="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/evaluation.csv">evaluation.csv</a><br>
The loss (categorical_focal_dice_loss) on this FracAtlas-Fracture/test was low, but dice_coef_hybrid was not high, as shown below.
<br>
<pre>
categorical_focal_dice_loss,0.0105
dice_coef_hybrid,0.8761</pre>
<br>

<h3>
5 Inference
</h3>
Please move to <b>./projects/TensorFlowFlexUNet/FracAtlas-Fracture</b> folder
and run the following bat file to infer segmentation regions for images using the trained TensorFlowUNet model for FracAtlas-Fracture.<br>
<pre>
./3.infer.bat
</pre>
This runs the following command.
<pre>
python ../../../src/TensorFlowFlexUNetInferencer.py ./train_eval_infer.config
</pre>
<hr>
<b>mini_test_images</b><br>
<img src="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/asset/mini_test_images.png" width="1024" height="auto"><br>
<b>mini_test_mask(ground_truth)</b><br>
<img src="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/asset/mini_test_masks.png" width="1024" height="auto"><br>

<hr>
<b>Inferred test masks</b><br>
<img src="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/asset/mini_test_output.png" width="1024" height="auto"><br>
<br>
<hr>
<b>Enlarged images and masks for FracAtlas-Fracture Images of 512x512 pixels</b><br>
As shown below, the inferred masks look similar to the ground truth masks except for the first and second cases.<br>
<br>
<table>
<tr>
<th width="320" height="auto">Image</th>
<th width="320" height="auto">Mask (ground_truth)</th>
<th width="320" height="auto">Inferred-mask</th>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/mini_test/images/hflipped_IMG0002338.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/mini_test/masks/hflipped_IMG0002338.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/mini_test_output/hflipped_IMG0002338.png" width="320" height="auto"></td>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/mini_test/images/IMG0001365.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/mini_test/masks/IMG0001365.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/mini_test_output/IMG0001365.png" width="320" height="auto"></td>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/mini_test/images/hflipped_IMG0003182.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/mini_test/masks/hflipped_IMG0003182.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/mini_test_output/hflipped_IMG0003182.png" width="320" height="auto"></td>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/mini_test/images/IMG0002323.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/mini_test/masks/IMG0002323.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/mini_test_output/IMG0002323.png" width="320" height="auto"></td>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/mini_test/images/IMG0002520.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/mini_test/masks/IMG0002520.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/mini_test_output/IMG0002520.png" width="320" height="auto"></td>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/mini_test/images/rotated_180_IMG0002020.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/mini_test/masks/rotated_180_IMG0002020.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/FracAtlas-Fracture/mini_test_output/rotated_180_IMG0002020.png" width="320" height="auto"></td>
</tr>
</table>
<hr>
<br>
<h3>
References
</h3>
<b>1. FracAtlas: A Dataset for Fracture Classification, Localization and Segmentation of Musculoskeletal 
Radiographs</b><br>
Iftekharul Abedeen, Md. Ashiqur Rahman, Fatema Zohra Prottyasha, Tasnim Ahmed, <br>
 Tareque Mohmud Chowdhury & Swakkhar Shatabda <br>
<a href="https://www.nature.com/articles/s41597-023-02432-4">https://www.nature.com/articles/s41597-023-02432-4</a>
<br><br>
<b>2. The impact of implementing backbone architectures on fracture segmentation in X-ray images</b><br>
Salih Turk, Ozkan Bingol, Ahmet Coskuncay, Tolga Aydin<br>
<a href="https://www.sciencedirect.com/science/article/pii/S2215098624002696">
https://www.sciencedirect.com/science/article/pii/S2215098624002696</a>
<br><br>
<b>3. WCAY object detection of fractures for X-ray images of multiple sites</b><br>
Peng Chen, Songyan Liu, Wenbin Lu, Fangpeng Lu, Boyang Ding<br>
<a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC11535499/">https://pmc.ncbi.nlm.nih.gov/articles/PMC11535499/</a>
<br><br>
<b>4. TensorFlow-FlexUNet-Image-Segmentation-Model</b><br>
Toshiyuki Arai<br>
<a href="https://github.com/sarah-antillia/TensorFlow-FlexUNet-Image-Segmentation-Model">
https://github.com/sarah-antillia/TensorFlow-FlexUNet-Image-Segmentation-Model
</a>
<br><br>
