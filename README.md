# HiFi_iQ_NDSP
NatureDSP Library for HiFi iQ DSP cores
Note: This is the NDSP early access release for HiFi iQ DSP using RJ-2026.6 toolchain.

# The repo is organized as follows.

## xws:
  * This reease of the NDSP contains two xws files.

  * An xws each, for the library-kernels and the test-driver.
    Ex : HiFi_iQ_VFPU_library_v0_8_0.xws & HiFi_iQ_VFPU_demo_v0_8_0.xws

  * Building and executing the xws in Xtensa Xplorer is described in the API Reference Document. 
  * Detailed release documentation can be extracted from lib.xws/doc folder.

### Release v0.8.0 Brief: 
  * Release Date : Jun-2026.  
  * This release is targeted for xt-clang compiler
  * All testing and performance measurements have been done on xt-clang using RJ-2026.6 version of the Xtensa Xplorer and tools.  
  * four different core configurations are used to build and verify this package
	hifiiq_ao_so7_BM:    Speed Optimized core with All options enabled 
	hifiiq_ao_co7_BM:    Cycle Optimized core with All options enabled 
	hifiiqBase_so7_BM:   Speed Optimized Base Core (doesnot contain Half Precision, Single Precision or Double precision floating point unit and AI Unit) 
	hifiiq_dspai_so7_BM: Speed Optmized core without double precision floating point unit.
  *	The library is tested with sanity test vectors shared along with this package
  * Although many APIs are described in the reference document/User Guide, only certain APIs are available in this release. Remaining APIs will be made available in the subsequent releases.
  * In this release there is limited support for fixed point FFTs / IFFTs. Only powers of 2 sizes are supported. Non powers of 2 sizes and improved memory efficiency (_ie) variants will be supported in subsequent releases


## NDSP_HiFi_iQ
This contains the source code along with make files that will build in linux environment.  
## doc folder
This contains help documentation on how to build the source code in linux and run the performance and functional regressions. 
