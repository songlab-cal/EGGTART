# EGGTART
EGGTART (**E**xtensive **G**UI **g**ives **T**ASEP-realization in **r**eal-**t**ime) is a software package that provides a visualization of the dynamics associated with the generalized Totally Asymmetric Simple Exclusion Process (TASEP).

## Installation
EGGTART has been developed in Python 3.6. It uses the packages numpy and pyqtgraph, which require pyqt4 or pyqt5. For ease of installation, we provide an executable version of the software that does not require having Python and the required add-on packages installed. To launch EGGTART, simply download the version developed for your operating system, and double-click the corresponding executable file. A separate open-source version will be made available in the future. We provide different versions of EGGTART for Mac OS X, Linux (Ubuntu 18.04) and Windows, with most extensive testing conducted on Mac.

## Tutorial
Here is a simple tutorial to demonstrate the various features of EGGTART and the fundamental properties of the TASEP:

1. To begin with, let us visualize the original TASEP model. Load the input file called 
```
homogeneous_rates.csv
```
which should result in this setup:

![tutorial_1](figures/tutorial_1.png)

The <img src="https://render.githubusercontent.com/render/math?math=\lambda"> panel (bottom left) displays the hopping rates, while the top left panel visualizes the bulk density. Default parameters <img src="https://render.githubusercontent.com/render/math?math=\alpha"> (entrance rate), <img src="https://render.githubusercontent.com/render/math?math=\beta"> (exit rate) and <img src="https://render.githubusercontent.com/render/math?math=\ell"> (particle size) are displayed in the bottom middle panel, with a ball in the top middle panel indicating the current <img src="https://render.githubusercontent.com/render/math?math=(\alpha, \beta)"> value in the phase diagram. EGGTART informs us that for this particular configuration, the system follows dynamics of the MC (maximal current) regime, since both <img src="https://render.githubusercontent.com/render/math?math=\alpha"> and <img src="https://render.githubusercontent.com/render/math?math=\beta"> are above their respective critical values associated with phase transitions (shown by red lines in the right panels). The right panels display correctly that the current and average density are constant in this region.

2. We change the entrance rate <img src="https://render.githubusercontent.com/render/math?math=\alpha"> by typing a new value (0.2) in the left box located in the middle bottom panel (it is also possible to drag the ball located in the phase diagram):

![tutorial_2](figures/tutorial_2.png)

As a result, the ball in the phase diagram panel has now moved to the _LD_ region and in the top right panel, and the <img src="https://render.githubusercontent.com/render/math?math=\alpha"> flag has moved past the critical red line (representing a phase boundary) correspondingly. The single <img src="https://render.githubusercontent.com/render/math?math=\rho"> branch in the <img src="https://render.githubusercontent.com/render/math?math=\rho"> panel has split into a lower and upper one, of the solution of our hydrodynamic limit picks the lower (whence, low density).

3. To visualize the HD regime, we modify <img src="https://render.githubusercontent.com/render/math?math=\beta"> to 0.1 (proceeding as before, but adjusting values in the middle box instead of the left one):

![tutorial_3](figures/tutorial_3.png)

The density has now switched to the upper branch, with the relative roles of <img src="https://render.githubusercontent.com/render/math?math=\alpha"> and <img src="https://render.githubusercontent.com/render/math?math=\beta"> with respect to their critical values reversing in the top and bottom right panels.

4. We now introduce some _defect_ in the rates. Right click on any point of the <img src="https://render.githubusercontent.com/render/math?math=\lambda"> plot and decrease its value (e.g. 0.2):

![tutorial_4](figures/tutorial_4.png)

In the MC regime, one can now notice that two branches of solution co-exist, with <img src="https://render.githubusercontent.com/render/math?math=\rho"> starting from the upper one before switching to the lower one at the defect location.  Moreover, the range of _J_ has decreased significantly.

5. To visualize the impact of the rate heterogeneity, load the input file called\break 
```
heterogeneous_rates.csv
```
which will yield the following interface:

![tutorial_5](figures/tutorial_5.png)

At positions where the hopping rate function <img src="https://render.githubusercontent.com/render/math?math=\lambda"> achieves the minimum, the density switches between the two branches.  Therefore, changing these locations can drastically affect the density over the whole lattice:

![tutorial_6](figures/tutorial_6.png)

6. The phase transitions from LD to HD also depend on the value of <img src="https://render.githubusercontent.com/render/math?math=\lambda"> at the boundaries of the lattice. By changing <img src="https://render.githubusercontent.com/render/math?math=\lambda(0)"> or <img src="https://render.githubusercontent.com/render/math?math=\lambda(1)">, one can notice that the separation between LD and HD in the phase diagram gets non-linear.

![tutorial_7](figures/tutorial_8.png)

7. Finally, increase the value of the particle size <img src="https://render.githubusercontent.com/render/math?math=\ell"> to see how it decreases the density, current, and critical values of <img src="https://render.githubusercontent.com/render/math?math=\alpha"> and <img src="https://render.githubusercontent.com/render/math?math=\beta">, and also modifies the shape of the LD to HD phase separation:

![tutorial_8](figures/tutorial_9.png)

Please consult the user manual "EGGTART_User_Manual.pdf" for further details.
  
Dan D. Erdmann-Pham, UC Berkeley\
Wonjun Son, Columbia University\
Khanh Dao Duc, University of British Columbia\
Yun S. Song, UC Berkeley
