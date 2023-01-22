# cfxr

This is a stripped down version of sfxr without any win32 or SDL dependencies.

It receives a parameters file (*.sfs) exported from sfxr and generates an fx sound with the given parameters and saves it as WAV file.

TODO:
1. Read parameters from the command line 
   - only category: generates a sound given the category (coin, jump, hit, etc)
   - Without parameters it should generate a random fx sound
   - default sound file should be named aout.* 
   - If the sound input parameters file (*.sfs) is not provided, one should be created after sound generation

