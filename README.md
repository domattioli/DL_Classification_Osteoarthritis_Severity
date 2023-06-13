# DL_Classification_Osteoarthritis_Severity
Training a deep learning (DL) classification model to accurately differentiate OA severity in AP knee radiographs using labled and unlabeled pools of data.
Goal: Leverage self-supervised methods to train a more powerful supervised model.

### Data: 2 Pools.
##### 9,786 total images.
1. Labeled images.
  - 2,352 (~24%) radiographs (1/patient)
  - Expert labels for OA severity according to KL (Kellgren and Lawrence) classification system.
  - Severity ranges from 0:1:4
2. Unlabeled images.
  - 7,434 (~76%) radiographs (1/patient).
  - Unlabeled.

## Solution Approach: 6 Steps.
1. Train self-supervised DL model for inpainting unlabeled images in Pool 2.
   - Want to train an inpainting model to fill in blank patches of an input image.
2. Perform inpainting using model from (1).
   - Demonstrate performance ability of (1).
   - Use metrics and visualizations for comparing generated images v. ground truth images.
3. Train classification model using encoder from (1).
   - Fine tune weights of encoder using images in Pool 1.
   - Train classifier using weights.
4. Report on performance of (3).
   - Use metrics and visualizations.
5. Compare performance of (3) to a naive classifier trained on Pool 1.
   - No transfer learning.
   - Use metrics and visualizations.
   - TBD naive classifier.
6. Writeup
   - Explanations of methods, results.
   - Use well-formatted figures, tables, and markdown text.
   - Include intro and conclusion paragraphs.
   - Include assumptions.
