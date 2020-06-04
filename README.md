# Combine EEG/MRI/Behavioral data-sets to learn more about Music/Auditory system

![SEff](selection_effect.png)

<!-- ![Mri](fmri.png ) -->

## Summary

I'm currently a PhD student of the IPN at McGill University.

~~In this project I aim to combine data from different modalities (fMRI, EEG, and behavioral) to understand more about sound and music processing.~~

My main focus in this project was to try to reproduce some of the results from a published paper starting form raw data.

The overall goal of the current project is to be able to organize, pre-process and do some basic analyses form a fMRI study

## Project definition

### Background

TODO

### Tools

The project will rely on the following technologies:

* fmriprep

* pandas

* nipype

* bids

* nilearn

* numpy

* pathlib

* jupiter lab

### Data

The first step was to search for candidates open datasets. I prioritized music/auditory related, as it is closer to my PhD project.

<!-- I was not able yet to acquire any data myself, but there are some open data-sets out there where I want to start working on. -->

Possible existing potential datasets can be:

#### Chosen


TODO: Add descriptions and papers.

* Forrest Gump:
  
  | N      | Type      | Tasks    | Comments |
  |--------|-----------|----------|----------|
  | 37     |     bold, T1w, T2w, angio, dwi, fieldmap      |   Forrest Gump, objectcategories, movielocalizer, retmapccw, retmapcon, retmapexp, movie, retmapclw, coverage, orientation, auditory perception        |    Maybe the most promising example     |

  <https://openneuro.org/datasets/ds000113/versions/1.3.0>
* Neural Processing of Emotional Musical and Nonmusical Stimuli in Depression

  | N      | Type      | Tasks | Comments |
  |--------|-----------|----------|----------|
  |  39   |      T1w, bold      |     Music, Non-Music listening     |    missing stims    |

  <https://openneuro.org/datasets/ds000171/versions/00001>

#### Other Options

* A dataset recording joint EEG-fMRI during affective music listening.

  | N      | Type      | Tasks | Comments |
  |--------|-----------|----------|----------|
  |  21   |    T1w, channels, eeg, events, bold       |     GeneratedMusic, classicalMusic, genMusic01, genMusic02, washout, genMusic03     |  Could be very noisy EEG but also promising      |

  <https://openneuro.org/datasets/ds002725/versions/1.0.0>

  * Article <https://www.nature.com/articles/s41598-019-45105-2.pdf>  

* Decoding Musical Training from Dynamic Processing of Musical Features in the Brain.

  | N      | Type      | Tasks | Comments |
  |--------|-----------|----------|----------|
  |  36   |    bh bold       |  music listening        |    Non standard format    |

  <https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5768727/>

* Neuroimaging predictors of creativity in healthy adults

  | N      | Type      | Tasks | Comments |
  |--------|-----------|----------|----------|
  |  66   |    T1w, T2w, dwi, bold, fieldmap       |    Rest     |   Interesting to study resting state, good number of subjects     |
  
  <https://openneuro.org/datasets/ds002330/versions/1.1.0>

* Functional Connectivity of Music-Induced Analgesia in Fibromyalgia

  | N      | Type      | Tasks | Comments |
  |--------|-----------|----------|----------|
  |    40 |     T1w, dwi, bold      |   pre-control, pre-music, post-control, post-music      |     healthy and Fibromyalgia patients listening to music  |

  <https://openneuro.org/datasets/ds001928/versions/1.1.0>

  <http://www.eecs.qmul.ac.uk/mmv/datasets/deap/>

* Music BCI (006-2015)

  | N      | Type      | Tasks | Comments |
  |--------|-----------|----------|----------|
  | 10    |    eeg       |    oddball 3 music instruments     |  not much to extract maybe      |

  <http://bnci-horizon-2020.eu/database/data-sets>

  Publication:
  * <http://doc.ml.tu-berlin.de/bbci/BNCIHorizon2020-MusicBCI/BNCI_MusicBCI.pdf>

* OpenMIIR - Music imagery information retrieval

  <https://github.com/sstober/openmiir>

  <https://academictorrents.com/details/c18c04a9f18ff7d133421012978c4a92f57f6b9c>

  | N      | Type      | Tasks | Comments |
  |--------|-----------|----------|----------|
  |  10   |   eeg        |  imagery        |   very short musical exerts      |

  Existing Publications:

  * <https://bib.sebastianstober.de/2015-01-31_NEMISIG.pdf>

  * Sebastian Stober. Towards Studying Music Cognition with Information Retrieval Techniques: Lessons Learned from the OpenMIIR Initiative. In: Frontiers in Psychology Volume 8, 2017.
  doi: 10.3389/fpsyg.2017.01255

  * Sebastian Stober. Learning Discriminative Features from Electroencephalography Recordings by Encoding Similarity Constraints. In: Proceedings of 42nd IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP’17), Pages 6175-6179, 2017.
  doi: 10.1109/ICASSP.2017.7953343

  * Sebastian Stober; Thomas Prätzlich & Meinard Müller. Brain Beats: Tempo Extraction from EEG Data. In: 17th International Society for Music Information Retrieval Conference (ISMIR’16), 2016.
  available from: <https://wp.nyu.edu/ismir2016/wp-content/uploads/sites/2294/2016/07/022_Paper.pdf>

  * Sebastian Stober; Avital Sternin; Adrian M. Owen & Jessica A. Grahn. Deep Feature Learning for EEG Recordings. In: arXiv preprint arXiv:1511.04306 2015.
  available from: <http://arxiv.org/abs/1511.04306>

  * Avital Sternin; Sebastian Stober; Jessica A. Grahn & Adrian M. Owen. Tempo Estimation from the EEG Signal during Perception and Imagination of Music. In: 1st International Workshop on Brain-Computer Music Interfacing / 11th International Symposium on Computer Music Multidisciplinary Research (BCMI/CMMR’15), 2015.
  available from: <http://bib.sebastianstober.de/bcmi2015.pdf>

* The neural basis of spoken word perception in older adults

  | N      | Type      | Tasks | Comments |
  |--------|-----------|----------|----------|
  |   61  |     T1w, T2w, bold, events       |   LISTEN02, REPEAT02, REPEAT01, LISTEN01      |    Interesting, need to read more about the data. there are 375 different monosyllabic words |

  <https://openneuro.org/datasets/ds002382/versions/1.0.0>

* A dataset recorded during development of an affective brain-computer music interface:

  | N      | Type      | Tasks | Comments |
  |--------|-----------|----------|----------|
  |  19-10-9   |    channels, eeg, events       |   music listening and reported arousal and valance      |    Low subj number but interesting data    |

  * <https://openneuro.org/datasets/ds002724/versions/1.0.1>

  * <https://openneuro.org/datasets/ds002722/versions/1.0.1>

  * <https://openneuro.org/datasets/ds002723/versions/1.1.0>

* An EEG dataset recorded during affective music listening

  | N      | Type      | Tasks | Comments |
  |--------|-----------|----------|----------|
  |  31   |   channels, eeg, events        |   music listening       |   Very littel information about what files where use     |

  <https://openneuro.org/datasets/ds002721/versions/1.0.1>

  Possible article:
  
  * <https://www.sciencedirect.com/science/article/abs/pii/S030439401400367X>

* Sherlock_Merlin waiting bids validator

  | N      | Type      | Tasks | Comments |
  |--------|-----------|----------|----------|
  |   37  |  mri      |   listen and see movie (A/B groups)      |   Very interesting, stimuli are provided     |

  <https://openneuro.org/datasets/ds001110/versions/00003>

* Milky-Vodka - (2 different stories )

  | N      | Type      | Tasks | Comments |
  |--------|-----------|----------|----------|
  |  54   |      T1w, bold, events     |     Milky, Synonyms, Scrambled, Vodka    |    stims available,     |

  <https://openneuro.org/datasets/ds001131/versions/1.0.0>

* Audiovisual Learning MEG Dataset
  | N      | Type      | Tasks | Comments |
  |--------|-----------|----------|----------|
  |   30  |    coordsystem, channels, events, meg       |   The auditory and visual stimuli were 12 Georgian letters and 12 Finnish phonemes      |     mapping things?   |

  <https://openneuro.org/datasets/ds002598/versions/1.0.0>

* Auditory localization with 7T fMRI

  | N      | Type      | Tasks | Comments |
  |--------|-----------|----------|----------|
  |   10  |   T1w, PD, T2star, dwi, bold, events, fieldmap        |   rest, auditory, TODO: full task name for rest, TODO: full task name for auditory      |  need to be down sampled       |

  <https://openneuro.org/datasets/ds001942/versions/1.2.0>

* FFR ?.

  <https://www-jneurosci-org.proxy3.library.mcgill.ca/content/37/4/830>

#### Interesting but not related

* Go-nogo categorization and detection task

  | N      | Type      | Tasks | Comments |
  |--------|-----------|----------|----------|
  |     |           |         |        |

  <https://openneuro.org/datasets/ds002680/versions/1.0.0>

* A multi-modal human neuroimaging dataset for data integration: simultaneous EEG and MRI acquisition during a motor imagery neurofeedback task

  | N      | Type      | Tasks | Comments |
  |--------|-----------|----------|----------|
  |   10  |      T1w, eeg, bold     |      eegNF, fmriNF, motorloc, eegfmriNF, MIpre, MIpost   |   Not interested     |

  <https://openneuro.org/datasets/ds002336/versions/2.0.0>

  <https://openneuro.org/datasets/ds002338/versions/2.0.0>  

* TUH EEG Corpus Too big for the 3 weeks.

  <https://www.isip.piconepress.com/projects/tuh_eeg/html/downloads.shtml>

* Dataset: rsfMRI before and after one session EEG NF vs Sham NF

<https://openneuro.org/datasets/ds001408/versions/1.0.3>

* Data relating "Alpha/beta power decreases track the fidelity of stimulus-specific information"

  <https://openneuro.org/datasets/ds002000/versions/1.0.0>

* Real-time EEG feedback on alpha power lateralization leads to behavioral improvements in a covert attention task

  <https://openneuro.org/datasets/ds002034/versions/1.0.1>

* EEG meditation study

  <https://openneuro.org/datasets/ds001787/versions/1.0.2>

* EEG study of the attentional blink; before, during, and after transcranial Direct Current Stimulation (tDCS)

  <https://openneuro.org/datasets/ds001810/versions/1.1.0>

* Simultaneous EEG-fMRI - Confidence in perceptual decisions

  | N      | Type      | Tasks | Comments |
  |--------|-----------|----------|----------|
  |  24   |     T1map, bold, events, eeg      |  motion direction of random dot kinematograms        |        |

  <https://openneuro.org/datasets/ds002739/versions/1.0.0>

* Audiocue walking study

  <https://openneuro.org/datasets/ds001971/versions/1.1.1>

* Auditory and Visual Rhythm Omission EEG

  <https://openneuro.org/datasets/ds002218/versions/2.0.0>

* Auditory and Visual Oddball EEG-fMRI

  | N      | Type      | Tasks | Comments |
  |--------|-----------|----------|----------|
  |   17  |    T1w, inplaneT2, bold, eeg, events       |         auditory oddball with button response to target stimuli, visual oddball with button response to target stimuli|        |

  <https://openneuro.org/datasets/ds000116/versions/00003>

#### NOT Accessible

* DEAP: A Database for Emotion Analysis Using Physiological Signals:
  (Not Accessible without explicit permission, which we are missing for no)

  | N      | Type      | Tasks | Comments |
  |--------|-----------|----------|----------|
  |     |           |         |    Not Accessible without explicit permission, which we are missing for now    |

### Deliverables

At the end of this project, we will have:

* Scripts to download the dataset

* Scrips to pre-process the data using fmriprep in a cluster

* Basic processing of 1 subject including.
  
  *  asdf

## Results


## Conclusion and acknowledgement

After the multiple problems I found trying to process the data, reproduce the analyses, and limitations imposed by the missing of information form the dataset I am more aware of what I will need to do to efficiency share my data/analyses in the near future.
