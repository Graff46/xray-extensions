How to patch:
  1) install masm32 (www.masm32.com)
  2) change path to masm in make_src_dll.bat to one where you installed masm
  3) launch make_src_dll.bat
  4) put xrRender_R1.dll in R1 folder
  5) rename dll in xrRender_R1_orig.dll
  6) launch patch_diff.bat
  7) launch patch.bat

Fixes description:
;=====EXTENDED TUNING OF DETAILS DISTANCE=======
   this fix allows to increase distance of details rendering and adds 
   a console command (r__detail_radius) to tune it.
   Default details radius - 49, this fix change limit to 250.
   If you want more, you can change limit in console_comm.asm (0F0h number)

;========NEW CONSOLE COMMANDS=========
   Allow to add new console commands. Already defined commands:
   r__detail_radius

;==EXTENDED TUNING OF DETAILS DENSITY=
   Change upper limit of detail density option to 0.02,
   so you can get more dense grass

;======RESTORING OF SUN DETAILS=======
   This fix restores sun details, which were broken.
   It is not good looking in CoP.

;=====LOD SWITCH EXTENDED TUNING======
   Fix extends lod switch upper limit (r__geometry_lod) to 3,0

;===MIPMAPS SWITCH EXTENDED TUNING====
   Fix extends mipmaps switch limits (r1_tf_mipbias) to [-3.0;3,0]

;=========SUN MOVEMENT FIX============
   With this fix you can control sun movement by config files.

;=========SKY RENDERING FIX===========
   SOC-style sky, no stretching.