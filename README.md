## Project Name 
ResNet Does Not Perform Intelligent Understanding of Picture in Image Recognition

## Summary
Found through experiments and theoretical considerations that ResNet recognizes local patterns, instead of global object shapes, and exploits spurious correlations.<br>

More on published paper: https://ieeexplore.ieee.org/document/9844486 <br>

## Contents of shared notebook
In the car-damage-locaction.ipynb notebook, given images of damaged cars with damage locations as labels ("side", "not side"), we train ResNet-50 to determine whether the damage is visible on the side of the car or on other locations of the car. We find through experiments that depending on the dataset, ResNet is not actually locating the damage, but may be taking in other factors such as the photo angle to determine the damage location (see Fig. 3 below). In fact, most photos with damage on the side, which we collected from the Internet, were taken from the side of the car as, naturally, this provides maximum visibility of the damage. We conclude that we should be mindful of the characteristics of our dataset and examine which factors are contributing to the model's predictions. 

<p float="left">
  <img src="images/fig3.png" width="500" />
</p>

## Acknowledgements
My code is largely based on the PyTorch tutorials below:<br>
https://pytorch.org/tutorials/beginner/transfer_learning_tutorial.html<br>
https://pytorch.org/tutorials/beginner/basics/data_tutorial.html<br>
It is a combination of lines directly from the above tutorials (or slightly modified) and my own. Also inspired by the fine_tune() method from fast.ai


