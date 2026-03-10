# Hardware Selection, Calibration, and Maintenance

## Introduction

The hardware used in an ecoacoustic study is not simply a data-collection tool: it is a measuring instrument whose characteristics directly shape the data it produces. Microphone sensitivity, frequency response, noise floor, housing design, and recorder firmware all influence which sounds are detected, how acoustic indices are calculated, and whether results are comparable across sites, seasons, or years. Hardware decisions therefore need to be treated with the same care as analytical decisions.

Choosing between recorders involves balancing acoustic performance, weatherproofing, battery and storage logistics, and the practical feasibility of maintaining consistent, well-documented deployments. Several small autonomous recording units (ARUs) now perform comparably for many common applications — particularly species detection in the human-audible range — but non-trivial differences emerge at higher frequencies, between microphone types, and as a result of housing and mounting choices. The practical implication is that no recorder is universally "best": the right choice depends on study objectives, target taxa, sampling scale, and the maintenance regime that can realistically be sustained.

Microphone sensitivity is not a fixed property. It varies between units when new, changes with field exposure through ageing, water ingress, membrane fouling, and thermal cycling, and can degrade to a degree that meaningfully reduces effective detection area and biases acoustic indices. Recent research has demonstrated that even modest sensitivity loss can shrink detection space substantially, and that these effects can be mistaken for genuine ecological change if hardware state is not tracked. Treating microphone condition as a measured variable — not a fixed assumption — is therefore a core requirement for defensible long-term monitoring.

This page covers three topics: selecting a recorder appropriate to study objectives; implementing a calibration and sensitivity-checking workflow; and a practical maintenance regime to keep recorders performing consistently throughout a project.

## Table of Contents

- [Device selection](#device-selection)
- [Microphone calibration](#microphone-calibration)
- [Recorder maintenance](#recorder-maintenance)

---

## Device selection

Choosing a recorder involves trade-offs across acoustic performance, cost, weatherproofing, battery life, storage capacity, and the availability of calibration and diagnostic tools. For terrestrial audible-range ecoacoustics, several small ARUs can support bird detection and acoustic index work, but differences emerge at higher frequencies and through the way housings and mounting substrates alter directionality and frequency response.

> We recommend selecting a recorder that meets your target frequency range and provides adequate signal-to-noise ratio, and deploying it consistently throughout the project using the same model, housing, and settings. Consistency across units and deployments matters more than marginal performance differences between models.

**Rationale**

Device selection shapes ecological inference in ways that are not always obvious from specification sheets. For bird survey applications, recorder performance is strongly influenced by microphone signal-to-noise ratio and deployment geometry; once detection ranges are standardised, ARU-based species richness can match traditional point counts. However, this comparability depends on hardware consistency: even within the same recorder model, protective housings, tree-mounting, and orientation can measurably alter sensitivity and frequency response, creating directionality effects that distort detections and acoustic indices if not standardised across deployments.

Cost is a genuine ecological variable because it determines achievable replication. A cost-effectiveness study found large differences in detection performance between recording systems when recorders were tested under realistic field conditions, including variation in singing direction and recording distance — highlighting that laboratory specifications do not always predict field performance. For monitoring programmes where spatial coverage is important, deploying more lower-cost units over longer periods may recover equivalent inventories to fewer higher-cost devices, although this trade-off is application- and taxon-specific.

For acoustic index work, hardware heterogeneity carries particular risk. Studies have shown that even co-located recorders of different models or firmware versions produce different index values for the same soundscape, and that cross-device variability can be large enough to generate contradictory ecological conclusions. Where mixing of recorder models is unavoidable — for instance when replacing equipment mid-programme — planned overlap deployments and equalisation pipelines can reduce but not eliminate these biases. Standardising on a single model throughout a project is strongly preferable.

Recorders also differ in the practicality of their calibration and quality-assurance pathways. Some models include built-in microphone sensitivity testing utilities; others are explicitly not suitable for applications requiring consistent, known absolute sound levels. This distinction is a legitimate basis for model selection in studies where acoustic indices or detection probability are used to infer ecological change, and should be considered alongside battery life and cost in any procurement decision.

**Research evidence**

Perks et al. (2025) compared bat monitoring data from commercial and open-source detectors. Commercial detectors outperformed open-source devices for species richness and accumulation speed in most habitats, but deploying multiple open-source units over longer periods recovered equivalent inventories in three of four habitats, illustrating an explicit replication-versus-quality trade-off.
https://doi.org/10.1002/2688-8319.70103

Mennill (2024) compared several small ARUs — including AudioMoth in IPX7 case, Song Meter Mini, Song Meter Micro, and SwiftOne — in recorder-based point count applications. Performance was broadly similar across devices for audible-range bird detection, with more notable differences above approximately 12 kHz. Housing and mounting configurations influenced frequency response and directionality.
https://doi.org/10.1080/09524622.2024.2315054

Zhang et al. (2024) showed that all six acoustic indices tested were affected by the recording device used, and that a signal-to-noise ratio threshold exists above which device noise effects become negligible. They recommended that recorders used for acoustic index work should have an omnidirectional microphone with a flat amplitude frequency response.
https://doi.org/10.1016/j.ecolind.2024.111759

Starbuck et al. (2024) compared passive acoustic devices for bat monitoring and found meaningful trade-offs between sound quality and cost, with lower-cost devices differing from traditional ultrasonic recorders in call quality in ways that could affect downstream analysis.
https://doi.org/10.1080/09524622.2023.2290715

Teixeira et al. (2024) reviewed passive acoustic monitoring practice for ecological monitoring and emphasised that effective PAM requires appropriate study planning, consistent field procedures, and rigorous quality assurance. They noted that equipment constraints and sensor capabilities must be explicitly matched to study aims.
https://doi.org/10.1111/csp2.13132

Lapp et al. (2023) conducted a quantitative evaluation of the AudioMoth, reporting a generally flat frequency response with a slight increase above 3 kHz and explicitly quantifying battery life across sample rates and temperatures. At higher sample rates (≥96 kHz), SD cards filled before batteries depleted — an important operational consideration for high-frequency work. At freezing temperatures, alkaline battery runtime fell substantially while lithium cells remained comparatively consistent.
https://doi.org/10.3390/s23115254

Osborne et al. (2023) tested the effect of protective coverings on AudioMoth recordings. Protective coverings altered spectral characteristics and acoustic metric values in ways that would be ecologically meaningful, underscoring the need to standardise enclosure type across deployments and to treat enclosure changes as hardware changes requiring overlap tests.
https://doi.org/10.3390/s23167287

Pérez-Granados et al. (2019) assessed the cost-effectiveness of five audio recording systems under realistic field conditions. They found large differences in detection performance between recorders, and demonstrated that detection rates decreased with distance and when sound sources were directed away from the recorder. They recommended evaluating several devices under site-specific conditions before committing to a recorder model.
https://doi.org/10.13157/arla.66.2.2019.ra4

Darras et al. (2018) conducted a meta-analysis comparing ARU performance to point counts for bird surveys. They found that after standardising detection ranges, species richness estimates from recorders and point counts were statistically indistinguishable, and that microphone signal-to-noise ratio, height, and number of microphones positively affected detection performance by increasing the effective detection range.
https://doi.org/10.1111/1365-2664.13229

[Back to top](#introduction)
---

## Microphone calibration

Microphone sensitivity is not a fixed property. It varies between units at manufacture and changes with field exposure through ageing, UV and thermal cycling, membrane fouling, and water ingress. These changes directly reduce effective detection area and alter acoustic index values, creating the risk that hardware degradation is interpreted as ecological change if microphone condition is not tracked over time.

> We recommend treating microphone sensitivity as a measured variable rather than a fixed assumption: carry out routine sensitivity spot-checks using a consistent reference source, log microphone identifiers and deployment history, and replace microphones on the basis of measured drift rather than subjective assessment of recording quality.

**Rationale**

Microphone sensitivity degrades with field use in ways that are not always perceptible through casual listening. Sensitivity shifts can result from physical wear to the microphone membrane, exposure to moisture, UV and thermal cycling, or fouling by dust and debris. These changes alter the effective detection area of the recorder — the volume of space within which a sound of a given level will be reliably detected — and can also affect acoustic indices that are sensitive to absolute or relative amplitude. Without routine tracking, gradual sensitivity loss can accumulate across deployments and masquerade as a genuine ecological trend, particularly in studies designed to detect long-term change.

The risk is compounded by manufacturing variability: even new microphones of the same model may differ slightly in sensitivity, meaning that a monitoring programme using multiple units may have an uneven detection baseline from the outset. This heterogeneity becomes more significant as units age at different rates, particularly where some recorders have experienced more severe field conditions than others.

Recording devices differ in their support for quantitative sensitivity assessment. Some models include built-in utility functions that report microphone output in dBFS; others are explicitly not intended for applications requiring consistent, known absolute sound levels. Where a calibration utility is available, it is only meaningful when paired with a calibrated signal generator or reference source at a known amplitude and distance. Where no such utility exists, sensitivity checks using a repeatable playback setup with a fixed reference recording can still provide a relative baseline sufficient to track drift over time.

Where multiple recorder models are used within a project, or where models are replaced between deployment seasons, differences in frequency response and gain can introduce systematic biases in acoustic indices that are independent of any ecological change. Such biases can be substantially reduced using equalisation pipelines, but only if device characteristics have been measured and documented. The strongest approach is to treat calibration as a programme design requirement, built in from the outset rather than applied retrospectively.

**Research evidence**

Jarrett et al. (2025) identified hardware change as a key source of long-term bias in terrestrial ecoacoustic studies. They recommended regular calibration tests to measure variation in the acoustic detection space and to remove unwanted biases, and advocated for documentation and storage strategies that keep reanalysis feasible as hardware evolves.
https://doi.org/10.1111/1365-2664.70000

Luna-Naranjo et al. (2024) developed an automated pipeline to quantify and mitigate recorder-induced variability in ecological acoustic indices, testing it across AudioMoth and Song Meter units. The pipeline reduced cross-device variation in acoustic indices by up to 75%, but was dependent on having measured device characteristics available. They noted that recordings of the same landscape with different devices hindered reproducibility and could produce contradictory results.
https://doi.org/10.1016/j.ecoinf.2024.102668

Potenza et al. (2024) proposed and evaluated a protocol to equalise audio recorders for ecoacoustic analysis. Their approach demonstrated a significant reduction in index biases attributable to device differences, and was applicable to situations where multiple recorder models are deployed within the same project.
https://doi.org/10.3390/s24144642

Madhusudhana et al. (2022) reviewed equipment selection for animal bioacoustic research and highlighted that constraints and capabilities of sensors and recorders must be explicitly matched to study aims. They noted that equipment progress increases accessibility but does not eliminate the need to understand what each device is — and is not — measuring.
https://doi.org/10.1007/978-3-030-97540-1_2

Turgeon et al. (2017) quantified the effects of microphone variability and degradation on detection probability in ARU-based bird monitoring. Sensitivity loss reduced effective detection area by approximately 25% for microphones only slightly outside specification and approximately 66% for severely compromised microphones. Microphones deployed for one field season showed a median sensitivity approximately 1.0 dBV lower than new microphones; those deployed for two or more seasons were approximately 1.9 dBV less sensitive. The authors explicitly recommended regular sensitivity testing, replacing microphones with declining sensitivity, and recording sensitivity as a covariate in analyses dependent on detection probability.
https://doi.org/10.5751/ACE-00958-120109

[Back to top](#introduction)
---

## Recorder maintenance

Effective maintenance in long-term ecoacoustic monitoring is as much about preventing silent data-quality drift as it is about preventing equipment failure. Key failure modes include water ingress through degraded gaskets or improperly sealed lids, clogged vents and windscreens that alter frequency response, microphone damage from wildlife interference or UV exposure, SD card corruption or filling before retrieval, battery voltage collapse mid-deployment, and clock drift that misaligns recordings with environmental metadata. Many of these failures are detectable only through systematic post-deployment inspection, not through a cursory check in the field.

> We recommend a four-stage maintenance structure for every deployment cycle: pre-deployment bench check, field deployment with documented setup, post-retrieval quality assurance, and periodic sensitivity review. Keep a written log of device and microphone identifiers, firmware versions, housing types, consumable replacement dates, and any anomalies detected.

**Rationale**

The pre-deployment bench check should cover firmware version and clock accuracy, battery state (fresh or charged to a known level), SD card formatting and a write/read verification, and a test recording that is listened to and visually inspected on a spectrogram before the unit is deployed. For recorders with microphone sensitivity utilities, a sensitivity spot-check against a baseline at this stage creates a record of microphone condition at the start of each deployment. Units that fail any check should be quarantined and not deployed until the fault is resolved.

At deployment, the setup should be documented with a photograph and a metadata record that includes device ID, microphone ID, housing type, firmware version, settings, and the precise location and mount. Weatherproofing should be verified at the point of installation: gaskets should be clean and undamaged, vents and windscreens should be clear of debris, and lids or enclosures should be properly closed and sealed. For recorders where sealing depends on gasket alignment or screw torque, this step is maintenance-critical, since failure to close correctly affects weatherproofing and facilitates water intrusion.

Post-retrieval quality assurance should include file integrity checks, a review of metadata completeness, and a short listening and spectrogram inspection of recordings from each channel to detect corruption, silent segments, excess static, or channel faults. Water ingress typically produces characteristic noise signatures that are visible in spectrograms. Any anomalies should be flagged and the affected unit should not be redeployed until inspected. After inspection, recorders should be cleaned and dried before storage, with batteries removed where manufacturer guidance recommends this.

At a programme level, periodic cross-calibration — ideally at least once per season — should compare recorders against each other or against a reference source to detect sensitivity drift before it accumulates into a trend. For multi-year programmes, planned overlap deployments (running old and new devices simultaneously at the same locations for a period) provide the strongest basis for correcting any discontinuity introduced by hardware replacement. SD cards should be sourced from reputable suppliers; counterfeit cards are a documented cause of data loss and may have misleading speed and capacity specifications.

**Research evidence**

Jarrett et al. (2025) recommended that long-term ecoacoustic monitoring programmes implement regular calibration tests to measure variation in acoustic detection space and remove unwanted biases. They highlighted that hardware changes are inevitable in long-term programmes and that documentation, calibration, and storage strategies are needed to keep reanalysis feasible.
https://doi.org/10.1111/1365-2664.70000

Teixeira et al. (2024) provided recommendations for conservation practitioners using passive acoustic sensors, emphasising that equipment selection and deployment procedures must be matched to study aims, and that poor planning and inconsistent field practices undermine the ecological value of data collected. They highlighted that quality assurance throughout the monitoring cycle — not just at data processing — is essential for defensible ecological inference.
https://doi.org/10.1111/csp2.13132

Lapp et al. (2023) quantified the dependence of AudioMoth battery life on sample rate, SD card characteristics, and temperature. Their results showed that higher SD speed classes draw more power and reduce runtime, and that at high sample rates storage fills before batteries deplete — operational variables that must be explicitly considered when planning deployment durations and servicing intervals.
https://doi.org/10.3390/s23115254

Turgeon et al. (2017) recommended routine sensitivity testing and explicit replacement criteria for microphones in ARU-based monitoring programmes, and demonstrated that sensitivity declines occur after a single field season of use. Their results support time-based or deployment-count-based maintenance triggers rather than ad hoc replacement.
https://doi.org/10.5751/ACE-00958-120109

[Back to top](#introduction)
---
