# 3DEC Scripts for Stability Assessment of Masonry Structures

Scripts to model a semicircular unreinforced masonry arch under gravitational acceleration. Originally written for and run on *3DEC 5.0* (Itasca Consulting Group, Inc.). Do not use without crediting Demi Fang.

## Using the Scripts

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

Installation of 3DEC (http://www.itascacg.com/software/3dec).

### Running the Scripts in *3DEC*

Make a new *3DEC* project.

Download the .3dec and .3ddat files in the repo, save where desired (recommended same location as *3DEC* project), and add them to the project.

First, run 0_2_arch.3dec. This script sets up the geometry for a semicircular arch with a fixed base. It also records the support faces. See comments within the script for more details.

Next, run boundary.3ddat. This script defines and assigns the material properties of the blocks and the joints between blocks. It also hides the fixed base block and saves the model’s state into the saved state bc.3dsav.

The remaining scripts, grav.3dec and grav_normal_and_shear.3dec, are identical with the exception that the latter contains extra code for recording the normal and shear force at the support faces (lines 6-34). Run either script to apply gravitational acceleration to the arch. It should be stable.

For an unstable arch, repeat the above steps but with 0_106_arch.3dec instead of 0_2_arch.3dec.


## Contributing

Not currently accepting contributions. To ask questions or report problems, contact Demi Fang.


## Authors

* **Demi Fang** - *Initial work* - senior thesis at Princeton University, 2017 - “Assessing the Stability of Unreinforced Masonry Arches and Vaults: A Comparison of Analytical and Numerical Strategies”


## Acknowledgments

Created with the help of Anjali Mehrohtra, Rebecca Napolitano, and Jim Hazzard (Itasca). Thanks [Spencer](https://github.com/839083) for helping me set up my first repo!
