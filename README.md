# masterthesis-showcase
Repo to show results of my thesis experiments: The influence of pruning on gradient-based attribution methods

## VGG-16 trained from Scratch on Imagenette
NB-Viewer: https://nbviewer.jupyter.org/github/weberdavid/masterthesis-showcase/blob/main/Grad-CAM-pruning%20comparison.ipynb
For this notebook, a VGG-16 was randomly initialized and then trained on the Imagenette dataset. The convolutional layer of this trained model were then pruned iteratively with two different methods and finetuned again until convergence. The notebook shows the visualizations of GradCAM for a particular prediction, for 15 models in total.

The first row shows the original image, the non-pruned model and then the VGG-16 pruned for every compression rate based on local-magnitude-unstructured pruning. The second row shows the original image, the non-pruned model (as in first row) and then the VGG-16 pruned for every compression rate based on local-random-unstructured pruning as a comparison. It is interesting to see differences of the GradCAM heatmap among the different model compression rates and pruning methods, as the image-row of the french horn shows below.

![Alt text](images/vgg16_scratch_french-horn.png)

Includes:
- Training Details
- Pruning Results (local magnitude unstructured and local random unstructured)
- Pruning Compression Rated (2, 4, 8, 16, 32, 64)
- GradCAM Visualizations


## VGG-16 finetuned for Imagenette (pretrained on Imagenet)
NB-Viewer: TBA
