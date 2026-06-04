# How to Build and Run the Source Code in Linux environment
  * Get the latest or required version of HiFi iQ NDSP Code from GitHub 
  * https://github.com/foss-xtensa/ndsplib-HiFi_iQ/NDSP_HiFi_iQ

## The source code is organized as follows.
  * **build** - contains the make file 
  * **library** - contains the optimized kernel functions for the HiFi iQ core 
  * **testdriver** - contains the demo driver code to tun the library   

### It is assumed that the required HiFi core configurations and the Xtensa toolchain are installed in the Linux environment.
 An example .cshrc file  that sets up the build environment accordingly is provided for reference 

## Setting up the environment 
  * A typical way is to place this .cshrc file in your home directory and execute the following from the command line terminal... 
  * source ~/.cshrc 
  * rj6
  * setenv XTENSA_CORE CORE_NAME     
    Ex: setenv XTENSA_CORE hifiiq_ao_co7_BM

## Compiling the Source Code: 
  * Navigate to the testdriver directory:   …/NDSP_REL_V0_8/build/project/xtclang/testdriver
  * **CLEAN:**  make clean -j  
  * **BUILD:**
  *  make all -j
  *  make all -j MEM_MODEL=X    //Where X = 1 or 2 
  * Ex : make all -j MEM_MODEL=1  //for performance tests 


## Running the executable: 
  ### Navigate to the bin directory: …/NDSP_REL_V0_8/build/bin
  ### Performance tests:
  * xt-run testdriver-hifiiq_ao_co7_BM____mm1_release_clang-Xtensa-release-mips -sanity         
  * xt-run testdriver-hifiiq_ao_co7_BM____mm1_release_clang-Xtensa-release-mips -brief 
  * xt-run testdriver-hifiiq_ao_co7_BM____mm1_release_clang-Xtensa-release-mips -full   
  ###	Functional tests:
  * xt-run --turbo testdriver-hifiiq_ao_co7_BM____mm1_release_clang-Xtensa-release-func -sanity
  * xt-run --turbo testdriver-hifiiq_ao_co7_BM____mm1_release_clang-Xtensa-release-func -brief
  * xt-run --turbo testdriver-hifiiq_ao_co7_BM____mm1_release_clang-Xtensa-release-func -full
  * xt-run --turbo testdriver-hifiiq_ao_co7_BM____mm1_release_clang-Xtensa-release-func -sanity -verbose 
  * xt-run --turbo testdriver-hifiiq_ao_co7_BM____mm1_release_clang-Xtensa-release-func -sanity -fir -verbose 
  * xt-run --turbo testdriver-hifiiq_ao_co7_BM____mm1_release_clang-Xtensa-release-func -brief -fir -iir -fft
