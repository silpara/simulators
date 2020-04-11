# Simulators for different purposes

The repo currently has the following models implemented in jupyter notebooks:
* [Compartmental models](https://en.wikipedia.org/wiki/Compartmental_models_in_epidemiology "Compartmental models in epidemiology") namely SEIR and SEIRD which are elaborations of the basic SIR model. These models are used in epidemiology to predict the spread of a disease. E.g. variations of these basic models are being used in prediction of spread of COVID-19.

## Compartmental Models

For completeness the models are produced below:

### SEIR Model
<img src="compartmental_models/images/seir_model.png">

<img src="https://latex.codecogs.com/svg.latex?\displaystyle \frac{dS}{dt} = -\frac{\beta S I}{N}" />
$\displaystyle \frac{dE}{dt} = \frac{\beta S I}{N} - \sigma E$<br><br>
$\displaystyle \frac{dI}{dt} = \sigma E -  \gamma I$<br><br>
$\displaystyle \frac{dR}{dt} = \gamma I$<br><br>
$N = S + E + I + R$<br><br>


### SEIRD Model
<img src="compartmental_models/images/seird_model.png">

$\displaystyle \frac{dS}{dt} = -\frac{\beta S I}{N}$<br><br>
$\displaystyle \frac{dE}{dt} = \frac{\beta S I}{N} - \sigma E$<br><br>
$\displaystyle \frac{dI}{dt} = \sigma E -  \gamma I - \mu I$<br><br>
$\displaystyle \frac{dR}{dt} = \gamma I$<br><br>
$\displaystyle \frac{dD}{dt} = \mu I$<br><br>
$N = S + E + I + R + D$<br><br><br>
Where,<br><br>
$\beta$ is infection rate or the rate of spread<br><br>
$\sigma$ is the incubation rate or the rate of latent individuals becoming infectious (average duration of incubation is $1/\sigma$)<br><br>
$\gamma$ is the recovery rate or mortality rate. If the duration of indection is D then $\gamma$ = 1/D<br><br>
$\mu$ is the mortality rate due to the disease


## Organization
```
compartmental_models
--[SEIR](https://github.com/silpara/simulators/blob/master/compartmental_models/SEIR%20Simulator%20in%20Python.ipynb "SEIR Simulator in Python")
--[SEIRD](https://github.com/silpara/simulators/blob/master/compartmental_models/SEIRD%20Simulator%20in%20Python.ipynb  "SEIRD Simulator in Python")
```

