# Data Analysis

## Recommendations

The minimum standard for a bird acoustic survey will commonly be a verified species list for the study site, with associated levels of vocal activity. This may be broken down into data for different recorder locations, and across sampling dates.

There are two simple approaches that can be taken to analyse and present the data from surveys – either: (i) report the number of detections identified for each species, or (ii) identify the presence/absence of each species in one minute audio samples and calculate the proportion of samples in which each species is recorded. Both of these outputs can be used to provide a summary of species observations per day or deployment period at each recorder location.

If using any automated recogniser or clustering process to identify species vocalizations, then a degree of manual verification is required, so that error rates can be checked and the quality of the recogniser can be properly assessed. This quality assurance process need not review all detections, but can use a suitable sub-sample of the complete dataset, or may focus on rare/unusual species in the context of the site or habitat being surveyed. This verification process, and its results, should be fully set out in the survey report.

When using BirdNET specifically, we recommend configuring the software with prediction segment overlaps of 1–2 seconds. Clear recommendations for sensitivity are not yet established, and may depend on study context. A confidence threshold of ~0.5 is suggested for assemblage-level analyses to balance precision and recall, while reducing false positives. Additionally, requiring a species to be detected a minimum number of times (e.g., ten detections) before including it in results can further reduce spurious misidentifications.

## Rationale

The analysis of data gained from acoustic recorders is perhaps the most difficult area in which to make standardised recommendations. A range of software is available to manipulate, view and analyse acoustic recordings, e.g. Kaleidoscope Pro, Raven, Audacity, BirdNET, BTO Acoustic Pipeline and packages in R (with use subject to licence as necessary). Some software options allow the clustering or automated recognition of bird calls. However, much scientific research has also relied upon ornithologists listening to audio files and viewing spectrograms. At present, a human-supervised semi-automated process probably offers the best balance between accuracy of call classification and time required for analysis. Whichever method is used, the data analysis protocol should be fully described, and identification error rates calculated, providing metrics such as precision and recall if a recogniser has been used.

The recommended BirdNET settings are based on recent evaluations of algorithm performance across large-scale datasets. Increasing overlap between classification windows will improve the likelihood of capturing complete vocalisations within each prediction segment, enhancing detection recall. However, this can have a sigbnificant impact on the processing time required - increasing overlap to 2s nearly doubles processing time (Perez-Granados 2025), potentially bcoming a constraint for larger datasets. Confidence thresholds around 0.5 provide a balance between precision and recall at the assemblage level, while requiring a minimum number of detections per species reduces false positives from sporadic misidentifications. Performance is generally higher for species with more available recordings and for longer-duration datasets, whereas overlapping vocalisations, with more than one species in a classification segment, can reduce precision. The settings recommended represent good-practice starting points, but optimal values may vary with regional species composition, recording conditions, and study objectives, so preliminary testing is recommended for new survey sites.

Data collected through acoustic monitoring techniques should be checked by experienced taxon-specialists, familiar with the relevant vocalisations and species distribution/behaviour.

Following survey completion, audio recordings, particular those of rare and priority species, should be stored to allow review at a later date. They should also be archived with county recorders/research organisations, or with online, open-source bird call repositories such as Xeno-Canto – unless the client or funder explicitly requires that this is not done.

## Research evidence

Pérez-Granados et al. (2025) conducted an evaluation of BirdNET parameter settings, assessing performance at vocalisation-level (classifying individual calls), and at dataset-level (to generate species lists). Across both analytical scales, increasing overlap to two seconds produced gains in recall and overall performance. Sensitivity settings had the strongest influence - for species-list outputs the optimal value was consistently 0.5, whereas for vocalisation-level detections the optimal value varied regionally. Confidence thresholds also showed task-specific optima, with low thresholds (0.1–0.3) best for detecting individual vocalisations and higher thresholds (around 0.5) improving species-level accuracy by reducing false positives.
  https://doi.org/10.1111/ibi.70013

Funosas et al. (2024) assessed BirdNET for European bird community monitoring. Increasing overlap improved recall, with 2-second overlaps performing best, while a detection sensitivity of 1.5 maximized overall performance. Confidence thresholds influenced precision–recall trade-offs: low thresholds (0.3) maximized recall, whereas higher thresholds (0.55–0.65) reduced false positives and improved precision at the dataset level. Performance was higher for species that are well representde in the training dataset and for longer-duration field datasets, while overlapping species vocalisations reduced precision but not recall. 
  https://doi.org/10.1016/j.ecolind.2024.112146

Pérez-Granados (2023) reviewed a number of published studies that used BirdNET to detect and classify bird sounds.  Amongst these, average precision (% detections correctly identified) usually ranged around 72–85%, and recall rate (% target species vocalizations detected) ranged around 33–84%. The review showed that the use of confidence score thresholds for classifications increased the percentage of detections correctly identified to species, but lowered the proportion of calls and bird species detected.
  https://doi.org/10.1111/ibi.13193

Symes et al. (2022) recognise that bird acoustic data are currently often analyzed by humans who review  spectrograms on screen, however this is not efficient, and automated machine-learning approaches are being developed to replace this process for large datasets.
  https://doi.org/10.1002/ece3.8797

Cole et al. (2022) assessed the performance of BirdNET by comparing automated and manual classifications of 13 breeding bird species. They found that BirdNET correctly identified most bird species detected during manual bird identification, and concluded that BirdNET is suitable for annotating multispecies recordings for extended recording periods.
  https://doi.org/10.1093/ornithapp/duac003

Shaw et al. (2022) compared species richness values in forest habitats derived from point counts and bioacoustic monitoring methods, with manual analysis of recordings being employed. Species richness was significantly higher from acoustic recordings than point counts, although only when the time spent analysing acoustic data exceeded the time spent conducting point counts. However, the bioacoustic method enabled additional metrics of bird activity, enabling insights not provided by point count data. For example, increased acoustic activity was related significantly with habitat structural complexity, indicating that automated recording is more effective in identifying high quality habitat patches than point count methods.
  https://doi.org/10.1002/ece3.9491

Toenies & Rich (2021) assessed the ability of BirdNET to correctly identify species, when employed with a data subsetting process for quality control. This process achieved a high rate of true positive species identifications and a misidentification rate of less than 4%, which compares well to misidentification rates of 6-22% recorded in studies of human analysts.
  https://doi.org/10.51492/cfwj.107.5

Perez-Granados & Traba (2021) reviewed studies that used acoustic recorders for estimating bird densities or bird abundance. The most common approach was to estimate the relationship between the number of vocalizations per recording time with bird density or bird abundance estimated in the field, with the result that 79% of studies showed agreement between estimates obtained by human surveyors and those by acoustic methods.
  https://doi.org/10.1111/ibi.12944
