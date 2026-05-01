# Long-term_prediction_of_sea_ice_concentration_with_ConvLSTM
This repository contains the neural networks trained in the paper.

The models expect a (batch, 22, 200, 200, 3) input.
Channel 0 is cf, 1: sic, 2: sal of the same hemisphere.

a stands for attention-based architecture, r stands for residual architecture.

The inputs should be same month of the year sequence. 
Eq: May 2003, May 2004 ... May 2024.

The model predicts one year shifted output from the given input
Eq: Input: May 2003 ... May 2024, Output: May 2004 ... May 2025.

Input images should have the same cover area with the training images, 
some of which are available in the sample images folder. 
Otherwise is not tested.

I recommend to use only the last frame of the outputs to minimize accumulation of errors.
