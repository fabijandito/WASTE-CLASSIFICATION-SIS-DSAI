# WASTE-CLASSIFICATION-SIS-DSAI
Deep Learning for Intelligent Waste Classification

Group Members
-Fabianus Jandito Anung Pragitama - 2702248931
-Rafhel Pangestu - 2702257715
**Dataset**
The models utilize the Recyclable and Household Waste Classification dataset from Kaggle, which contains various waste images mapped into six primary classes: Plastic, Paper, Glass, Metal, Organic, and Textile. Dataset Link: 
https://www.kaggle.com/datasets/alistairking/recyclable-and-household-waste-classification

This research explores how Deep Learning specifically CNN can push intelligent waste classification forward and back up the global Zero Waste movement. We put ResNet50 and EfficientNetB0 head to head, comparing how well they pick out six main types of waste: Plastic, Paper, Glass, Metal, Organic, and Textile. To keep things clear, the project unfolds across two notebooks. The first tracks our starting benchmarks, while the second captures how optimization efforts evolve. This split spells out our technical progress, especially when it comes to using Early Stopping to tame overfitting. In practice, these tweaks help the models generalize better, so they work out in the real world not just in the lab.

**1.Initial Benchmark (Without Early Stopping)**


This notebook marks where our research began. Here, we set up the models ResNet50 and EfficientNetB0 with a fixed routine each trained for exactly 10 epochs using a heavy batch size of 422. We did this to get a clear baseline for performance. The schedule was non negotiable. Once the computer hit the tenth round, it stopped training, no matter if the model was still learning or even starting to fall apart. That rigidity gave us consistency, but it didn’t let the models reach their best or adapt if things went sideways.


**2. Performance Optimization (With Early Stopping)**
This notebook is our smart upgrade from the first experiment. This time, we built in an Early Stopping mechanism. Now the computer checks its own learning as it trains if it goes 15 rounds without getting any better, it just stops. No point wasting time and resources if it’s hit a wall. We also lowered the processing load to 256 so the whole system runs smoothly while learning.What really matters here: we want to avoid overfitting. That happens when the model does nothing but memorize the training images instead of learning patterns it can actually use. With these changes, we make sure the saved model stays sharp, adaptable, and ready to spot different types of waste in real-world situations, not just the stuff we've already shown it.
