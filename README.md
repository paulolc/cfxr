# cfxr - utility to synthetize an 8bit game effect into a WAV file.

This is a stripped down version of Dr. Pepper's [sfxr](http://www.drpetter.se/project_sfxr.html) without any win32 or SDL dependencies.

It receives a parameters file (*.sts) exported from sfxr and generates an fx sound with the given parameters and saves it as WAV file.


## Build

Run make.

```
make
```

## Run

```
./cfxr <SFXR_PARAMETERS_FILE>
```

## Usage

```
    USAGE: cfxr [ [coin|laser|explosion|powerup|hit|jump|blip|mutate] | -s <SFXR_PARAMETERS_FILE> | -h ]

    EXAMPLES:

       cfxr -s fxparameters.sts

       # synthetize a sound effect based on the parameters loaded from fxparameters.sts settings file and ouput the sound to cfxr.wav file


       cfxr coin

       # synthetize a coin sound fx based on random parameters, save the parameters in cfxr.sts OVERWRITING it and ouput the sound to cfxr.wav file

```

## Sound

To hear the sound effect generated you'll need some other program or app to play the generated WAV file.

### Example using Windows (WSL)

```
./cfxr coin -s cfxr.sts && /mnt/c/Program\ Files\ \(x86\)/VideoLAN/VLC/vlc.exe cfxr.wav --play-and-exit

```

### Example using Linux

```
./cfxr coin -s cfxr.sts && alsaplay cfxr.wav 

```


# TODO:
- Optionally read output WAV file from the command line

