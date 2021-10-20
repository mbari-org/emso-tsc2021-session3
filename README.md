# About

A collection of notebooks for the TSC 2021 "Observing Sound" workshop, Training session 3, Gran Canaria in the Canary Islands, Spain, 20-22 October 2021.

## Session3 Overview

### Methods for the detection and identification of marine mammals sounds
Trainers: Danelle E. Cline & John Ryan – Monterey Bay Aquarium Research Institute
- 
- [Danelle Cline](dcline@mbari.org), Senior Software Engineer, Monterey Bay Aquarium Research Institute (MBARI)
- [John Ryan](ryjo@mbari.org), Senior Research Specialist, Monterey Bay Aquarium Research Institute (MBARI)

** We are still looking for data in the EMSO portal that may contain blue whale signals.  
If anyone knows where we might find this, please contact us directly at the email above. Thank you! ** 

The MBARI research activity with Blue whales is proposed as the focal content for the EMSO TSC training, because:
* It uses a combination of Machine Learning (ML) and signal processing methods, depending on the type of call.
* Blue Whales are a fascinating endangered species for which science can inform protection.

Objectives
-------
* Apply signal processing methods to discover what can be heard when Blue Whales are migrating (https://www.mbari.org/blue-whale-songs-migration/). The reason these methods (signal: noise, energy detection) are used to quantify song occurrence on key time scales is that there are times when the whales are calling so much that individual calls cannot be distinguished from each other (while the total signal from all calling whales can still be quantified relative to background).
* Demonstrate use of Machine Learning to successfully detect and classify other call types that occur less frequently and thus do not have the above “chorusing” difficulty.
MBARI are proposing to use an existing AWS (Amazon Web Services) Open Data project with both data and tutorials already up and tested in the cloud, for both Machine learning and signal processing methods applied to blue whales. To make the most effective use of a 3-hour period, MBARI suggest that we have participants simply use a web-browser and work in provided Google Colab notebooks – this is the simplest approach to quickly get up and running as it is straightforward to convert any examples in AWS to Google for a tutorial.

## Notebook access

### EMSO Portal

Setup your account per the instructions mailed to you, then clone this repository in the EMSO jupyter environment with:

```shell
git clone https://github.com/mbari-org/emso-tsc2021-session3.git
```

## Colab

**Colaboratory** is also known as Colab. It is a Google Research product that allows one to write code in a web browser.
Colab is free with limitations in compute and memory.  To use these notebooks in Colab:

1. Setup a gmail account if you don't already have one.
2. Launch the notebook by clicking on one of the links below:

| Notebook | Description  |
| -----------------------------------------  | -----------------------------------------
| [blueB/bluewhale_B_call_index.ipynb](https://colab.research.google.com/github/mbari-org/emso-tsc2021-session3/blob/master/blueB/bluewhale_B_call_index.ipynb)  | This tutorial describes use of the *Pacific Ocean Sound Recordings* archive to examine temporal patterns in the occurrence of blue whale song.  Signal processing methods focus on the blue whale B call. |
| [blueA/lesson1_data/call_exploration.ipynb](https://colab.research.google.com/github/mbari-org/emso-tsc2021-session3/blob/master/blueA/lesson1_data/call_exploration.ipynb) | A basic exploration of the blue A call. |
| [blueA/lesson2_spectrogram_generation/pcen_overview.ipynb](https://colab.research.google.com/github/mbari-org/emso-tsc2021-session3/blob/master/blueA/lesson2_spectrogram_generation/pcen_overview.ipynb) | An overview of per-channel energy normalization (PCEN) |
| [blueA/lesson2_spectrogram_generation/pcen_versus_log_humpback.ipynb](https://colab.research.google.com/github/mbari-org/emso-tsc2021-session3/blob/master/blueA/lesson2_spectrogram_generation/pcen_versus_log_humpback.ipynb) | Side-by-side comparison of PCEN versus log mel transformation for more complex humpback song |
| [blueA/lesson3_detect_classify/bled_classify.ipynb](https://colab.research.google.com/github/mbari-org/emso-tsc2021-session3/blob/master/blueA/lesson3_detect_classify/bled_classify.ipynb) | Classify blue whale A calls from Band-limited-energy-detection outputs using a Convolutional Neural Network (CNN) model trained on *Pacific Ocean Sound Recordings*. |
| [blueA/lesson3_detect_classify/stream_detect_classify.ipynb](https://colab.research.google.com/github/mbari-org/emso-tsc2021-session3/blob/master/blueA/lesson3_detect_classify/stream_detect_classify.ipynb) | Detect and classify blue whale A calls with streamable PCEN and a Convolutional Neural Network (CNN) model trained on *Pacific Ocean Sound Recordings*. |

### Local

Install [Anaconda](http://anaconda.org)

Setup environment

```shell
conda env create --file conda.yaml
conda activate emso-tsc2021-session3
```

Launch notebooks
```shell
jupyter notebook
```