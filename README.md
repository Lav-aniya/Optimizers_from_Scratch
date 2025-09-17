## Optimizers_from_Scratch

# SGD
$$ w_{t} = W_{t} - \eta \nabla L(w_{t}) $$
* $w_{t+1}$ is the updated weight
* $w_{t}$ is the current weight at time step $t$
* $\eta (eta)$ is the learning rate, which that controls the step size
* $\nabla L(w_{t})$ is the gradient of the loss function calculated with respect to just a single training example
     
# Adagrad
A cache, often called G or cache, is initialized to zeros for each parameter in the model.
In each training step, as the gradients are calculated, Adagrad squares each gradient element-wise and adds it to the corresponding entry in the cache.

$$
s_{t} = s_{t-1} + g_{t}^{2}
$$
* $s_{t}$ is the running cache at time step $t$
* $s_{t-1}$ is the ache from the previous time step
* $s_{t}$ is the current gradient

Parameter Update:
$$
w_{t} + 1 = w_{t} - \frac{\eta}{\sqrt{s_{t}}\epsilon} . g_{t}
$$
* $w_{t+1}$ is the updated weight at the next time step ($t + 1$)
* $w_{t}$ is the current weight at time step $t$
* $\eta (eta)$ is the learning rate, a hypermeter that controls the step size
* $g_{t}$ is the current gradient of the loss function with respect to the weights
* $\epsilon (9epsilon)$ is a small number to prevent division by zero

    
# RMSprop
$$ s_{t} = \beta s_{t-1} + (1 + \beta)g_{t}^2 $$
* $s_{t}$ is the new moving average of squared gradients
* $\beta (beta)$ is a decay rate hyperparameter (typically around 0.9) that controls how much of the old average to keep
* $g_{t}$ is the current gradient

Parameter Update:  
$$ w_{t + 1} = w_{t} - \frac{\eta}{\sqrt{s_{t}} + \epsilon} . g_{t} $$ 
* $w_{t+1}$ is the updated weight
* $w_{t}$ is the current weight
* $\eta (eta)$ is the learning rate
* $\epsilon (epsilon)$ is a small number to prevent division by zero


![visualization](images/output5.gif)
