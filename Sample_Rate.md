---
title: Sample Rate
layout: template
filename: Sample_Rate.md
---

Sample rate is the number of sound samples recorded per second. It affects the temporal resolution of acoustic data, and sets the highest frequency of the sound that will be recorded. The sample rate is programmed within the recording device settings.

> We recommend using a 48 kHz sample rate

### Research evidence
UKAN questionnaire: 55% of respondents selected a sample rate of 44.1/48 kHz for ecoacoustic studies.

Within the Global Soundscapes Project database (Darras, 2022), 183 of the 325 projects listed used a 48 kHz sample rate.
https://doi.org/10.5281/zenodo.6486836

The Silent Cities project used a 48 kHz sample rate in its global scale study of soundscapes during the Covid-19 lockdown.
DOI: 10.17605/OSF.IO/H285U

The most common (37%) sampling rate used in the 35 acoustic index studies reviewed by Alcocer et al. (2022) was 44.1 kHz.
https://doi.org/10.1111/brv.12890

Burivalova et al (2017) used a 44 kHz sample rate when using soundscapes to detect the effects of human influence on tropical forests.
https://doi.org/10.1111/cobi.12968

For bird surveys, Darras et al. (2018) recommended recording all frequencies in the audible range - with a sampling frequency of 44.1 kHz.
DOI: 10.1111/1365-2664.13229

### Rationale
A 48 kHz sample rate will record the full range of human hearing, and be able to capture a wide range of biological and environmental sounds in high resolution.
The sample rate you should use for audio files in ecoacoustic studies depends on the specific requirements of your study and the types of sounds you are trying to capture. In general, a higher sample rate will result in a greater temporal resolution and allow for more accurate representation of the original sound. However, higher sample rates also result in larger file sizes, which can be an issue with large datasets.

The sample rate needs to be twice the highest frequency of sound that is to be recorded. For example, the upper range of human hearing is ~20kHz, so needs a sample rate of 40kHz to be recorded (as defined in the Nyquist theorem). Similarly, lesser horseshoe bats have a call at 110 kHz, and so a sample rate of 256 kHz is normally used to ensure these calls are captured.

In ecoacoustic studies, it is common to use sample rates in the range of 44.1 kHz to 48 kHz. These sample rates are sufficient for capturing a wide range of sounds, including most vocalizations and other biological sounds. Some studies may require higher sample rates if they are focused on capturing very high frequency sounds or if they are trying to capture very fine temporal detail. In these cases, sample rates of 96 kHz or higher may be necessary.

The large Silent Cities citizen-science project used a 48 kHz sample rate, and the widely used BirdNET algorithm for birdsong classification is designed to work with a 48 kHz sample rate.

Most audio recorders have a number of potential sample rate options, with rates such as 16, 24, 32, 44.1, 48, 64, 96, 128 and 256 being fairly standard.
Sample rate determines the size of audio files, with high sample rates having a correspondingly high file size. A mono .wav file at 256 kHz sample rate of 8 seconds length may be around 4 MB in size, while a file of the same length at 44.1 kHz might only be 640 KB.

High sample rates can be ‘downsampled’ to reduce file size if necessary - the opposite is not possible.
