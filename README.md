# HiFi_iQ_NDSP
NatureDSP Library for HiFi iQ DSP cores
Note: This is the NDSP Beta release for HiFi iQ DSP using RJ-2026.6 toolchain.

# The repo is organized as follows.

## xws:
  * This release of the NDSP contains two xws files.

  * An xws each, for the library-kernels and the test-driver.
    Ex : HiFi_iQ_VFPU_library_v0_9_0.xws & HiFi_iQ_VFPU_demo_v0_9_0.xws

  * Building and executing the xws in Xtensa Xplorer is described in the API Reference Document. 
  * Detailed release documentation is available inside the doc folder of the imported HiFi_iQ_VFPU_library_v0_9_0.xws.

### Release v0.9.0 Brief: 
  * Release Date : Oct-2026.  
  * This release is targeted for xt-clang compiler
  * All testing and performance measurements have been done on xt-clang using RJ-2026.6 version of the Xtensa Xplorer and tools.  
  * Twenty different core configurations are used to build and verify this package
	hifiiqBase_so7_BM (Regular Latency Base core without HP, SP, DP, AI support, with 4 wide vec, with Big Memory)
	hifiiq_ao_co7_BM (Low Latency core with Big Memory)
	hifiiq_ao_so7_BM (Regular Latency Core with Big Memory)
	hifiiq_ao_so7_8sp_16hp (Regular Latency Core with 1X FMA)
	hifiiq_ao_so7_dram64kb (Regular Latency Core with 64 KB DRAM)
	hifiiq_ao_so7_noflt (Regular Latency Base core without HP, SP, DP, AI support with 8 wide vec)
	hifiiq_ao_so7_noai (Regular Latency core without AI support with 4 wide vec)
	hifiiq_ao_so7_newlib (Regular Latency Core with newlib Support)
	hifiiq_ao_so7_l2_pref_big (Regular Latency Core with L2 cache)
	hifiiq_ao_so7_ar32_newLib (Regular Latency Core with newlib Support with 32 AR registers)
	AE_HiFi_iQ_LE7_AO_FP_XC  (XC lib Big Memory core with All options, 32 AR reg and 8 Wide vec)
	AE_HiFi_iQ_LE7_FP_NwLib64 (newlib Big Memory core with 64 AR registers and 4 wide vec)
	hifiiq_ao_so7_ar32_xc (Regular Latency Core with 32 AR Registers, 8 Wide vec)
	hifiiq_ao_so7_sp (Regular Latency Core with only Single precision float support, 8 wide vec)
	AE_HiFi_iQ_LE7_AFP_XC (Regular Latency Core with 32 AR Registers, no AI support, 4 Wide vec, With Big Memory)
	hifiiq_ao_so5 (Regular Latency 5 stage core, 64 AR registers, 8 Wide vec)
	hifi_iq_rochester_BM_v2 (Regular Latency core with only Single Precision Float support with Big Memory)
	hifiiq_ao_co7_l2 (Low Latency core with L2 cache support with 64 AR and 4 Wide vec)
	hifiiq_dspai_so7_2c_l2 (Two core Regular Latency configuration with L2 cache support with 64 AR and 4 Wide vec)
	AE_HiFi_iQ_LE7_FP_XC64AR (XC lib core with 64 AR, 4 Wide vec, without AI support)

## NDSP_HiFi_iQ
This contains the source code along with make files that will build in linux environment.  

## doc folder
This contains help documentation on how to build the source code in linux and run the performance and functional regressions. 