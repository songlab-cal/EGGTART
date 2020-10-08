# EGGTART
EGGTART (**E**xtensive **G**UI **g**ives **T**ASEP-realization in **r**eal-**t**ime) is a software package that provides a visualization of the dynamics associated with the generalized Totally Asymmetric Simple Exclusion Process (TASEP).

## Installation
EGGTART has been developed in Python 3.6. and uses the numpy and pyqtgraph packages, which require pyqt4 or pyqt5. For ease of installation, we provide an executable version of the software that does not require Python or the required add-on packages to be installed. To launch EGGTART, simply download the version developed for your operating system, and double-click the corresponding executable file. Currently, we provide distributions of EGGTART for Mac OS X, Linux (Ubuntu 18.04) and Windows, with most extensive testing conducted on Mac. A separate open-source version will be made available in the near future. 

## Tutorial
Here is a simple tutorial to demonstrate the various features of EGGTART and the fundamental properties of the TASEP:

1. To begin with, let us visualize the original homogeneous 1-TASEP model. Load the input file called 
```
homogeneous_rates.csv
```
which should result in this setup:

![tutorial_1](figures/tutorial_1.png)

The <img src="https://render.githubusercontent.com/render/math?math=\lambda"> panel (bottom left) displays the hopping rates, while the top left panel visualizes the bulk density. Default parameters <img src="https://render.githubusercontent.com/render/math?math=\alpha"> (entrance rate), <img src="https://render.githubusercontent.com/render/math?math=\beta"> (exit rate) and <img src="https://render.githubusercontent.com/render/math?math=\ell"> (particle size) are displayed in the bottom middle panel, with a ball in the top middle panel indicating the current <img src="https://render.githubusercontent.com/render/math?math=(\alpha, \beta)"> value in the phase diagram. EGGTART informs us that for this particular configuration, the system follows dynamics of the MC (maximal current) regime, since both <img src="https://render.githubusercontent.com/render/math?math=\alpha"> and <img src="https://render.githubusercontent.com/render/math?math=\beta"> are above their respective critical values associated with phase transitions (shown by red lines in the right panels). The right panels display correctly that the current and average density are constant in this region.

2. We change the entrance rate <img src="https://render.githubusercontent.com/render/math?math=\alpha"> by typing a new value (0.2) in the left box located in the middle bottom panel (it is also possible to drag the ball located in the phase diagram):

![tutorial_2](figures/tutorial_2.png)

As a result, the ball in the phase diagram panel has now moved to the LD region and in the top right panel, and the <img src="https://render.githubusercontent.com/render/math?math=\alpha"> flag has moved past the critical red line (representing a phase boundary) correspondingly. The single <img src="https://render.githubusercontent.com/render/math?math=\rho"> branch in the <img src="https://render.githubusercontent.com/render/math?math=\rho"> panel has split into a lower and upper one, the fomer of which is picked by the solution to our hydrodynamic limit (whence, low density).

3. To visualize the HD regime, we modify <img src="https://render.githubusercontent.com/render/math?math=\beta"> to 0.1 (proceeding as before, but adjusting values in the middle box instead of the left one):

![tutorial_3](figures/tutorial_3.png)

The density has now switched to the upper branch, with the relative roles of <img src="https://render.githubusercontent.com/render/math?math=\alpha"> and <img src="https://render.githubusercontent.com/render/math?math=\beta"> with respect to their critical values reversing in the top and bottom right panels.

4. We now introduce _defects_ or _slow bonds_ into our jump rates. To do so, we right-click on any point of the <img src="https://render.githubusercontent.com/render/math?math=\lambda"> plot and decrease its value (to, say, 0.2):

![tutorial_4](figures/tutorial_4.png)

This reveals the branch switching phenomenon visible in MC: both solution branches now co-exists, with <img src="https://render.githubusercontent.com/render/math?math=\rho"> transitioning from high to low density precisely at the defect location.  Moreover, the reduction in the dynamical range of _J_ is clearly visible.

5. To visualize the impact of more extensive rate heterogeneity, we load the input file
```
heterogeneous_rates.csv
```
which will yield the following interface:

![tutorial_5](figures/tutorial_5.png)

The role of the defect location in our previous example is now taken on by the site of minimal elongation rate: it acts as bottleneck to the global current and forms the separator between high and low densities. Consequently, changes of its location can have dramatic effects on transport efficiency and thus deserve careful study:

![tutorial_6](figures/tutorial_6.png)

6. In addition to the role of <img src="https://render.githubusercontent.com/render/math?math=\lambda_{\min}">, EGGTART transparantly illustrates a dependence of the system's summary statistics on <img src="https://render.githubusercontent.com/render/math?math=\lambda(0)"> and <img src="https://render.githubusercontent.com/render/math?math=\lambda(1)"> that was not discernible in the homogeneous or slow-bond settings: Transitions in the phase diagram critically depend on <img src="https://render.githubusercontent.com/render/math?math=\lambda(0)"> and <img src="https://render.githubusercontent.com/render/math?math=\lambda(1)"> to the extent that <img src="https://render.githubusercontent.com/render/math?math=\alpha^{\ast}"> and <img src="https://render.githubusercontent.com/render/math?math=\beta^{\ast}"> are no longer symmetric, and the previously linear HD-LD separtion has turned non-linear.

![tutorial_7](figures/tutorial_8.png)

7. Finally, we increase the value of the particle size <img src="https://render.githubusercontent.com/render/math?math=\ell"> to see how it modifies the shape of the LD-HD phase boundary and decreases densities, currents, and critical values of <img src="https://render.githubusercontent.com/render/math?math=\alpha"> and <img src="https://render.githubusercontent.com/render/math?math=\beta">:

![tutorial_8](figures/tutorial_9.png)

Please consult the user manual "EGGTART_User_Manual.pdf" for further details.
  
Dan D. Erdmann-Pham, UC Berkeley\
Wonjun Son, Columbia University\
Khanh Dao Duc, University of British Columbia\
Yun S. Song, UC Berkeley
