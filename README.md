# Run TreeQSM in Octave

Some notes on how to run TreeQSM in Octave, I needed to do this as the HPC facility did not have a matlab licence. Hoping this will help people in a similar situation :)

## 1. Create a conda environment
`conda create -n octave`

Then activate the enviroment

`conda activate octave`

## 2. Install Octave and other prerequisites
`conda install -c conda-forge octave cmake cxx-compiler`

## 3. Open Octave and install prerequisites
`pkg install -forge io`

`pkg install -forge statistics`

Then load the statistics package

`pkg load statistics`

## 4. Update treeqsm.m to save as binary format

`save([inputs.out, '/', str], 'qsm', '-v7')`

## 5. Run as normal!
