# PeriodicNet

PeriodicNet, A Gradient Descent Based Model for Predicting Periodic Time Series
## Introduction

Periodic time series data, characterized by recurring patterns over time, poses a unique challenge for traditional forecasting models. Addressing this challenge, we present "PeriodicNet," a novel model designed specifically to predict periodic time series data through the application of gradient descent optimization.

## Motivation

Periodic time series data is ubiquitous across numerous domains, including finance, climate science, and signal processing. Traditional forecasting methods often struggle to capture the nuanced periodic patterns present in such data. Inspired by the need for accurate and efficient periodic time series prediction, PeriodicNet aims to leverage the power of gradient descent optimization to effectively model and predict periodic trends.

## Explanation
<<<<<<< HEAD
<div style="text-align: center;">
  <img src="images/figure1.png" alt="Descriptive text" style="width: 100%;"/>
  <p style="font-style: italic;">Fig1 (A) The microbiome is regularly stimulated, assuming that microbiome changes periodically (B)The microbiome was identified by 16s sequencing (C)Calculate differences of the microbiome (D)Gradient descent was used to optimise the model and RMSE is the loss function (E)Gradient descent to fit parameters</p>
</div>
An application of the PeriodicNet to the prediction of trends in cyclically changing microbiomes Fig.1(A). We wanted to predict changes in the microbiome, and using Bray-Curtis Dissimilarity to measure distances between microbiomes. Considering the periodicity of microbiome variation
, we used a periodic function to predict microbiome variation
 Fig.1(E).RMSE is a common loss function used in regression problems, which measures the average magnitude of the errors between the predicted values and the actual values Fig.1(F). The model adopts the random initialization and the parameters were updated by gradient descent.

## Download
Download MicroGradient using git:
```shell
git clone https://github.com/2275836125/MicroGradient.git
```

## Usage
1. **Define the Objective Function**: The objective is to minimize the error between the actual periodic time series data and the predicted values generated by the model. Let's denote the time series data as $( Y = \{y_1, y_2, ..., y_n\} )$ and the predicted values as $( \hat{Y} = \{\hat{y}_1, \hat{y}_2, ..., \hat{y}_n\} )$. The error can be represented using a loss function such as Mean Squared Error (MSE):

   $$ \text{MSE} = \frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2 $$

2. **Model Architecture**: Let's use a simple model that consists of a periodic function. We'll use a sinusoidal function for this purpose:

   $$ \hat{y}_i = A \cdot \sin(\omega t_i + \phi) + b $$

   Where:
   - $( A )$ is the amplitude.
   - $( \omega )$ is the angular frequency (related to the period of the time series).
   - $( t_i )$ is the time index.
   - $( \phi )$ is the phase shift.
   - $( b )$ is the bias term.

3. **Initialize Parameters**: Initialize the parameters randomly or with some sensible initial values.

4. **Gradient Descent**: Update the parameters iteratively to minimize the objective function. Compute the gradients of the loss function with respect to each parameter and update the parameters accordingly. The update rule for each parameter can be formulated as follows:

   $$ \theta_{\text{new}} = \theta_{\text{old}} - \alpha \frac{\partial \text{MSE}}{\partial \theta_{\text{old}}} $$

   Where $( \theta )$ represents any of the parameters (amplitude, angular frequency, phase shift, or bias), and $( \alpha )$ is the learning rate.

5. **Repeat**: Repeat the gradient descent process until convergence (i.e., until the change in the loss function becomes negligible or after a fixed number of iterations).

6. **Prediction**: Once the parameters are optimized, use the model to predict future values of the time series.

7. **Evaluate Model Performance**: Evaluate the model's performance using metrics like Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), or other relevant metrics on a validation dataset.

8. **Fine-tuning**: If necessary, fine-tune hyperparameters such as learning rate, model architecture, or regularization strength to improve performance.


