# An evidence-based guide for recorder deployment
The programming and deployment of automated acoustic recorders can be confusing to new practitioners, with a bewildering array of decisions to make on machine settings and fieldwork approaches. Research studies have used a wide variety of methods, with little coordination or development of good-practice - the limited guidelines previously available have been scattered throughout the literature.

Below, we set out some recommendations for implementing an ecoacoustics study focussed on long-term monitoring and the use of Acoustic Indices. The recommendations are based, where possible, on evidence from the scientific literature. The recommendations advise on audio settings for the recorders, recording schedules, and how best to deploy detectors in the field spatially and temporally. The choices provided will not be optimal for every project, but this guide is intended to advise those who are starting with ecoacoustics, or who are seeking consistency in approach. The recommendations are not intended to constrain experienced researchers who fully understand the best options for their own field of study.

As part of the evidence gathered for these recommendations, a questionnaire was circulated to attendees at the UK Acoustics Network (UKAN+) ecoacoustics symposium held at Manchester Metropolitan University on 15-16th June 2022. This asked a series of questions related to the parameters of a recommended survey protocol for an ecoacoustics study, focussed on developing audio data for analysis with acoustic indices. The favoured choices of the 84 respondents to the survey are included below (referred to as ‘UKAN questionnaire’).


## Sample Rate
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


## Bit depth
The bit depth of an audio file refers to the number of bits used to represent each sample of the audio signal. A higher bit depth allows for a greater dynamic range, which means that the audio file can capture a wider range of amplitude levels. However, higher bit depths also result in larger file sizes.

> We recommend using a 16 bit depth encoding

### Research evidence
There has been little study of the effects of bit depth on ecoacoustic studies.

### Rationale
In ecoacoustic studies, it is common to use bit depths of 16 bits or 24 bits. These bit depths are sufficient for capturing a wide range of sound volumes. Higher bit depths, especially 32 bit recordings, reduce the potential for ‘clipping’ with loud sounds.

For the majority of automated acoustic recorders, the bit depth is set by the unit’s firmware and can not be changed. Hence, no decision on this parameter is normally necessary by the user. The majority of automated units, e.g. Wildlife Acoustics, Audiomoth, Frontier Labs and Swift all record 16 bit files. Handheld recorders from manufacturers such as Tascam and Zoom can also record at 24 or 32 bit depth, which provide a wider amplitude scale.


## File type
There are a number of different file types that can be used for audio files in ecoacoustic studies. Some common file types include WAV, AIFF, FLAC, and MP3.

>We recommend using .wav files

### Research evidence
The meta-analysis of acoustic index studies by Alcocer et al. (2022) revealed that 94% of the projects used WAV format audio files.
https://doi.org/10.1111/brv.12890

Heath et al (2021) describe how, with compressed recordings, the signal is altered in relation to the level of compression, with higher frequencies and quieter sounds most severely altered. Lossless compression should be preferred in ecoacoustic studies, but if data storage is an issue, then MP3 encoding can be used while potentially having minimal impact on most acoustic indices.
https://doi.org/10.1002/ece3.8042

For bird surveys, Darras et al. (2018) recommended recording all audible frequencies in uncompressed WAV or FLAC audio file format. https://doi.org/10.1111/1365-2664.13229

### Rationale
WAV (Waveform Audio File Format) is a ubiquitous file type that can be produced by most recorders, and processed by most software. Although file sizes can be larger than other file types, the files are uncompressed and lossless, preserving all the data from the original recording.

FLAC (Free Lossless Audio Codec) files are a lossless compressed format. The file sizes often being approximately half of an equivalent WAV file. Some researchers therefore use this format to archive recordings, saving space (and cost), while not reducing the information held within the audio recording.
AIFF (Audio Interchange File Format) is another lossless file format that is similar to WAV. It is also widely supported and is a good choice for preserving the quality of the original audio.

MP3 (MPEG Audio Layer 3) is a compressed file format that is widely used for storing audio data. It is a lossy format, which means that it removes some of the audio data in order to reduce the size of the file. While MP3 files are generally smaller in size compared to WAV and AIFF files, they may not be as suitable for preserving the quality of the original audio.

Zero-crossing audio files are simple representations of when the recorded audio signal crosses the zero line. They can be used to reconstruct a sound wave, and hence provide data on frequency, but not on amplitude. Zero-crossing audio files are typically created by applying a threshold to the original audio signal, such that only those samples that exceed the threshold are retained. The file sizes are very small compared to other types.

The choice of file type depends partly on the recorder used. For example, Audiomoths record only in WAV format, while Wildlife Acoustics can save files as WAV, a proprietary W4V compressed format, and as ZC zero-crossing files. The Frontier Lab’s BAR-LT supports WAV and FLAC files.


## File length
Acoustic recorders can be programmed to record file lengths ranging from seconds to hours. The choice of recording length normally depends on issues around practical file management and how the recorded data will be processed.

> We recommend using a 1-minute file length

### Research evidence
UKAN questionnaire: 31% of respondents selected a 1 minute file length, with 20% selecting 5 minutes.

The 35 acoustic index studies reviewed by Alcocer et al. (2022) used file lengths equal to (40%) or shorter than 1 minute (40%).
https://doi.org/10.1111/brv.12890

When manually processing birdsong recordings, Bayne et al. (2017) found that shorter duration (1 min) files increased detection rates for species and allowed for wider coverage of times of day and different dates. http://bioacoustic.abmi.ca/wp-content/uploads/2017/08/ARUs_and_Human_Listeners. pdf
A literature review by Minkova et al. (2020) found that a small number of studies have contrasted alternative file-length choices, indicating that short duration files (e.g. 15 s–1 min) are most effective and efficient for detecting species, particularly for species that are relatively common. Minkova et al. (2020) chose to use 1 min audio clips. https://www.dnr.wa.gov/publications/lm_oesf_pac_sp.pdf

For all species considered during the tundra breeding bird survey by Thompson et al. (2017), analysis indicated that for most species of birds, a single 10 min survey during times and dates of high availability (June, between 0500 hours and 2000 hours) is likely sufficient to establish occupancy status. However, in any single 10 min recording, the majority of species are detected within the first few minutes; thus shorter duration recordings are likely to be more efficient in detecting species occupancy https://wildlife.onlinelibrary.wiley.com/doi/abs/10.1002/jwmg.21285

Cook & Hartley (2018) used two different time-sampling methods to calculate species richness and acoustic prevalence of birds, comparing 5 min sections of recordings with the first 10 s of each minute to create a composite of 5min duration. The 10 s composite samples detected 26% more species and produced improved prevalence indices, requiring 60% less listening time to detect as many species as the 5 min sections. doi.org/10.5751/ACE-01221-130121

Metcalf et al. (2021) compared the results of sampling one-hour of data by using 240 15 s samples spread randomly across a survey window, with sampling of four 15 min samples. They found that the shorter files, providing a ‘higher temporal resolution’, outperformed the less frequent longer files in every metric considered, detecting 50% higher alpha diversity, and 10% higher gamma diversity.
https://doi.org/10.1111/2041-210X.13521

Cifuentes et al (2021) suggest that short recordings sampled throughout the survey period accurately represent acoustic patterns, with an optimal schedule of ten 1 minute samples per hour.
https://doi.org/10.21068/c2021.v22n01a02

Melo et al. (2021) employed a 2 minute file length (with a single recording per hour), and were able to detect a large number of anuran species with an appropriate level of sampling effort and temporal scale.
https://doi.org/10.1016/j.ecolind.2021.108305

The review by Sugai (2019) found that for studies with 24 h diel recordings, the most commonly used recording lengths were up to 3 min (59%), or between 3-10 min (31.8%). https://doi.org/10.1093/biosci/biy147

### Rationale
Analysis of data for ecoacoustic studies has commonly been undertaken using 1 min length files, such that this has become a de facto standard: https://research.ecosounds. org/2019/08/09/analyzing-data-in-one-minute-chunks.html
This relatively short file length enables a greater range of time periods to be covered for the same data volume, aids parallel computation with manageable file sizes, retains sufficient detail of vocalisation structures (e.g. birdsong sequences), and can be easily viewed in reasonable temporal detail on a standard computer screen. In addition, when calculating acoustic indices, this file length seems to achieve a compromise between introducing boundary effects from cropping sound sequences into short segments, and over-smoothing temporal variation to gross averages. Finally, one minute has been shown to be an efficient length for listening by analysts, without attention fading and signals being missed.


## Files per hour
A number of studies have found that a stratified ‘on-off ’ time sampling programme (e.g. recording 1 minute in every 10), can capture comparable data to continuous recording, with consequent benefits in terms of battery life, data storage and processing time.

> We recommend recording 12 files per hour

### Research evidence
UKAN questionnaire: 27% of respondents selected 6 files per hour, with 17% selecting 12 files per hour.
Bradfer-Lawrence et al. (2020) assessed the length of time required to generate stable acoustic index values at a location, and concluded that continuous recordings are more effective for rapidly capturing soundscape character, while sparse time-sampling delayed this process. As a result, their recommendation was to sample continuously to minimise the required deployment period.
https://doi.org/10.1111/2041-210X.13254

Pieretti et al. (2015) simulated five different recording schedules from continuous sound files: (i) one minute every five; (ii) one minute every 10; (iii) one minute every 20; (iv) one minute every 30; and (v) one minute every 60. For each schedule they calculated the Acoustic Complexity Index. The 1 min in five schedule closely correlated with the soundscape captured by continuous recordings (r>0.90; p<0.01), while providing an 80% storage space and battery power reduction compared to the continuous sampling. https:///doi.org/10.1111/2041-210X.13254#mee313254-bib-0035

Shaw et al. (2022) investigated the effort required to estimate bird species richness and composition in European forests. They compared sampling intensity for 1 min files,
in intervals from 1-in-3 (n = 20 per hour) to 1-in-60 min (n = 1 per hour). The highest species richness was with recordings at the highest intensity of one every 3 mins. https://doi.org/10.1002/ece3.9491

The studies in the literature review by Minkova et al. (2020) recorded a daily total of recordings ranging from 10-240 min per 24-hour period (equal to 0.4-10 minutes per hour). However, the sampling protocol was often influenced by study limitations such as availability of personnel, hardware and data storage capacity. Minkova et al. (2020) used two sampling densities: four 1 min clips from each hour 0400-1000 , and two 1 min clips from each hour 1000-2200.
https://www.dnr.wa.gov/publications/lm_oesf_pac_sp.pd

The review by Sugai (2019) found that for studies with 24 h diel recordings, most used a single recording per hour (47%), with the remaining studies using 2, 4, or 6 recordings per hour.
https://doi.org/10.1093/biosci/biy147

### Rationale
In combination with file lengths of one minute, as recommended above, 12 recordings per hour provide a 20% time-sampling coverage. This level of sampling effort has been shown to adequately capture soundscape characteristics or species directions, while balancing data storage and processing requirements.


## Daily programme
Detection probability for bird and other taxa normally varies with time of the day, so recording times distributed throughout the day will sample the entire community most effectively.

> We recommend recording for the full 24 hour cycle

### Research evidence
UKAN questionnaire: 67% of respondents selected the full 24 hr daily cycle

Bradfer-Lawrence et al. (2019) found that characteristic diel patterns are important for determining differences between habitat types. Acoustic indices may be highly similar between habitats at some times of the day, while differing widely at other times. A wide range of recording times is therefore useful in characterising habitat types. https://doi.org/10.1111/2041-210X.13254

The bird study by La & Nudds (2016) found that morning-only acoustic recordings underestimated species richness, and that the greatest number of species per unit of sampling effort was detected with on-the-hour samples between 07:00 and 12:00, and at 21:00.
https://doi.org/10.1002/ecs2.1294

Shaw et al. (2022) investigated the effort to estimate bird species richness and composition in European forests. They compared recording in a dawn period (1 hr before sunrise), a morning period (1 hr beginning 3 hr after sunrise), and a combined period including both day phases. Species richness was significantly higher when including both day phases compared to dawn alone, and was slightly higher in the morning compared to dawn (yielding 80% of recorded species). However, certain nocturnal/ crepuscular species could only be observed in the dawn period. https://doi.org/10.1002/ece3.9491

Thompson et al. (2017) deployed recorders to assess how avian detection at different times of day, and dates. In their subarctic tundra sites, without a distinct dawn or dusk, most species displayed circadian patterns, with detection peaking at 0800-1200 hours, but remaining high through the day for some species. Between 2200 hours and 0500 hours, detection rates dropped to near zero, signaling a rest period for most species. The peak time of detection for most species took place in the late morning (0900–1000hours) doi/abs/10.1002/jwmg.21285

Sugai et al (2019) reviewed the recording periods for 460 studies that used passive acoustic monitoring. Due to a concentration on bat and anuran studies, sampling effort was mostly concentrated during the night. However, soundscape studies, not targeted at particular taxa, recorded through more of the diel cycle, with most effort at dawn and dusk.
https://doi.org/10.1093/biosci/biy147

Froidevuax et al. (2014) showed that sampling the full night was essential to fully capture the maximum number of bat species in forest habitats - covering the dusk and dawn peaks in bat activity only, did not record the rarer species with low detection probabilities.
https://doi.org/10.1002/ece3.1296

Linke et al. (2020) demonstrated that acoustic activity is highly sensitive to diurnal variation, with only 25-50% of sound types in tropical freshwaters detectable in any 4 hr period. A comprehensive sampling strategy therefore needs to include a 24 hr recording schedule to capture soundscape patterns.
https://doi.org/10.1111/fwb.13227

### Rationale
Recording through the full 24 hour period will capture all time events during the day, including the avian dawn and evening choruses, and nocturnal animals. It also allows the soundscape to be characterised evenly through the diel cycle.

Recording sound through the 24 hour diel cycle can be important in ecoacoustic studies to capture the full range of sounds produced in an ecosystem, and to study the effects
of diel patterns on sound production. Many ecosystems are characterised by changes in the soundscape produced over the course of a day in response to the natural history and behaviour of different species. By recording sound over a full diel cycle, it is possible to study these effects.


## Deployment period
Automated recorders are able to be powered for extended periods, particularly if using extended battery packs or even solar power. The storage capacity of SD cards has also expanded to the extent that days or weeks of sound data can be recorded on single deployments.

>We recommend that deployments should last for a minimum of one week

### Research evidence
UKAN questionnaire: 22% of respondents considered that a one week deployment was appropriate for ecoacoustic studies, with 20% selecting two weeks.
The 35 acoustic index studies reviewed by Alcocer et al. (2022) recorded for an average of 44 days (range 1–282 days).
https://doi.org/10.1111/brv.12890

Bayne et al. (2017) state that, for singing birds, deployment over several days results
in higher detection and occupancy rates than using a single day. However, there are diminishing returns - with fewer benefits from month-long deployments in comparison to covering more locations. http://bioacoustic.abmi.ca/wp-content/uploads/2017/08/ARUs_and_Human_Listeners. pdf

Bradfer-Lawrence et al. (2019) recommend collecting at least 120 hr of continuous recordings per site, to fully describe the soundscape in tropical habitats. These soundscapes are often more complex than those of temperate systems, and so less time may be required in (e.g.) European contexts.
https://doi.org/10.1111/2041-210X.13254

Minkova et al. (2020) studied breeding forest birds and recorded for a 10 day period, before extracting four discrete 24 hour periods from this total. https://www.dnr.wa.gov/publications/lm_oesf_pac_sp.pdf

The acoustic bird survey by Franklin et al. (2020) recorded for 15hrs/site and resulted in an average of 88% completeness of the assemblage, 73% completeness could be achieved with 5hrs of recordings. https://www.researchgate.net/publication/339665372_Establishing_the_adequacy_of_ recorded_acoustic_surveys_of_forest_bird_assemblages

Shaw et al. (2022) investigated the effort to estimate bird species richness and composition in European forests. They compared durations of 1–4 recording days for each recorder. Bird richness significantly increased with each added day up to 3 days, with no difference from adding the 4th day.
https://doi.org/10.1002/ece3.9491

The bird study by La & Nudds (2016) found that a survey period of at least 3 days was required to maximise species richness.
https://doi.org/10.1002/ecs2.1294

Furnas & Bowie (2020) stated the importance of adopting a temporal schedule that represents the range of conditions likely to effect detection probabilities (e.g. changes in weather, phenology and movement of animals). In most cases, this requires sampling over several days, with appropriate environmental covariates being recorded as part of the study protocol.
https://doi.org/10.2989/00306525.2020.1788829

Melo et al (2021) considered that species detection in monitoring programs is strongly associated with both sampling effort and temporal range of monitoring. Their study compared six potential sampling scenarios: single hour/day, five night/full-day, thirty night/full-day using recordings of 2 mins every hour. The greatest species richness was recorded with the thirty full day scenario. https://doi.org/10.1016/j.ecolind.2021.108305

### Rationale
Automated passive acoustic methods enable long-term deployments that can not normally be matched by observers. They thus enable a higher sampling effort and wider temporal range of sampling than traditional approaches, and consequently produce higher probabilities of species detection.


## Number of deployments per year
While many studies focus on particular times of year, such as the spring bird breeding period, for long-term ecoacoustics studies there will be considerable value in recording audio data throughout the annual cycle.

>We recommend that deployments should take place a minimum of four times per year, once per season

### Research evidence
UKAN questionnaire: 51% of respondents selected 4 deployments per year (one per season).

Bradfer-Lawrence et al., (2019) considered that short deployments during distinct seasons may be as suitable as a single long deployment (e.g. to total 120+ hours). https://doi.org/10.1111/2041-210X.13254

Siddagangaiah et al. (2022) studied the annual variation in underwater soundscapes, finding a phenology of fish chorusing that changed between seasons, reflecting species behaviour.
https://doi.org/10.1038/s43247-022-00442-5

### Rationale
Species occupancy and vocal activity levels will vary throughout the year, as will the overall soundscape of an ecosystem. To adequately capture this annual variation, it is recommended that ecoacoustic studies should cover all seasons: summer, autumn, winter and spring.


## Spatial layout
When using multiple recorders, a decision needs to be made on how to arrange these spatially. Random, transect, grid or fractal patterns can be used, or the location of recorders can be selected based on target features such as habitat types or nesting locations.

>We recommend that recorder locations should be selected based on parameters such as habitat type

### Research evidence
UKAN questionnaire: 58% of respondents would use a selected/optimised spatial distribution of sensors (e.g. by habitat type), with 17% choosing a grid-based arrangement.

Wood & Peery (2022) discuss two different sampling frameworks for acoustic studies. Recorders may be deployed preferentially in areas known to be important to a
species, such as nest sites, implying an ‘area of occupancy’ concept of a species range, Alternatively, recording locations may be randomly determined without relation to any knowledge of species use, e.g. in a survey grid, within a wider ‘extent of occurrence’. Preferential sampling requires substantial pre-survey information, but leads to intuitive parameter interpretation and greater precision due to its finer spatial scale; while greater survey coverage is attainable with random sampling.
https://doi.org/10.1111/ibi.13092

Piña-Covarrubias et al. (2018) tested how the placement of acoustic sensors could be optimized, as an alternative to the use of standard grids. They found that, on hilly terrain, selected placements on higher ground could halve the required number of sensors to cover an area, compared to a square grid.
https://doi.org/10.1002/rse2.97

In their study on bats, Froidevuax et al. (2014) showed that the three-dimensional structure of forests, including all microhabitats, must be sampled to adequately record the full species complement of bat communities.
https://doi.org/10.1002/ece3.1296

### Rationale
The spatial layout of recorders in a study will largely depend on the aims of the project. Investigations of environmental gradients will promote the use of linear, i.e. transect, layouts, while studies examining differences between habitat types will likely employ a selected or stratified grid layout. Projects to determine occupancy of particular habitat features, such as amphibian presence in ponds, will clearly make use of closely targeted locations. Many studies have used survey designs where detectors are rotated across a number of locations to increase geographical coverage. This reduces comparability between sites in terms of the dates when sampling occurs, but can be effective in maximising limited hardware resources.


## Spatial density
Unless simultaneous recordings are specifically required across an array of recorders (for the purposes of localization), then spacing between units is normally set to prevent any replication of sounds between sites. When undertaking species-specific studies, the spatial density of recording sites may usefully correspond to typical territory size of the target species.

>We recommend that recorder locations should be a minimum of 250m apart

### Research evidence
UKAN questionnaire: 30% of respondents selected a 500m separation distance between recorders (equal to 4 recorders/km2), with 23% choosing a 250m distance (equal to 16 recorders/km2).

Minkova et al. (2020) aimed to evaluate bird habitat use in forest stands of different ages and management types. Their preliminary field tests (in Kuehne et al. 2019) showed that the effective detection range of their Songmeter units was unlikely to exceed 125m for their species of interest, and so they spaced sampling locations ≥250m apart. https://www.dnr.wa.gov/publications/lm_oesf_pac_sp.pdf

The Yip et al. (2017) study on bird sounds confirmed that, for all species calls and broadcast tones, detection probability declined with increasing distance and decreasing sound amplitude, and was higher in open vegetation than in closed vegetation.

Furnas & Bowie (2020) state the recommendation, following traditional pointcounts, that independent sampling locations at least 250m apart should be used for autonomous sound recorders. This separation distance will address the potential for double counting and spatial autocorrelation, with their resulting biases on results and precision. https://doi.org/10.2989/00306525.2020.1788829ttps://doi.org/10.2989/00306525.2020.1 788829

### Rationale
For coverage of a site, the aim is normally to sample across the range of the habitats and species of interest, with recorders placed to limit overlap of detection radii so that counts are independent. The effective radius of most recorders is in the region of 50m, so a minimum separation distance of at least 100m should be used. As a recommended standard, a larger 250m spacing between recorder locations would provide 16 sampling locations/km2. This is dense enough to provide a good level of survey data, and is also likely to be relevant to the territory sizes of many species of interest within ecological assessments.
