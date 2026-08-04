# 2026 IAIFI Summer School

## Introduction

Presented by Will Detmold: [View Slides](https://docs.google.com/presentation/d/1WoXBA4IplwUnJ6VltvvZWUC_9zWFC-pW/edit?usp=sharing&ouid=113795742869595335302&rtpof=true&sd=true)

## 1. Automatic Equation Discovery

(Author: Miles Cranmer)

Instructor: [Miles Cranmer](https://www.maths.cam.ac.uk/person/mc2473)

Slides: [View Here](https://drive.google.com/file/d/1kk7pLNFrBGmN9YNMsKFas2ME_TWHaMx7/view?usp=sharing)

### Useful Materials
- [PySR docs](https://ai.damtp.cam.ac.uk/pysr/)
    - [code](https://github.com/astroautomata/PySR) **Recommended to install ahead of time and run an example.**
- [SymbolicRegression.jl docs, for Julia users](https://ai.damtp.cam.ac.uk/symbolicregression/)
    - [code](https://github.com/astroautomata/SymbolicRegression.jl)
- [PySR/SymbolicRegression.jl paper](https://arxiv.org/abs/2305.01582)
- [Discovering Symbolic Models from Deep Learning with Inductive Biases](https://arxiv.org/abs/2006.11287)
- [SymTorch](https://arxiv.org/abs/2602.21307)
    - [code](https://github.com/astroautomata/SymTorch)
- [The Next Great Scientific Theory is Hiding Inside a Neural Network (Simons Foundation Presidential Lecture)](https://www.youtube.com/watch?v=fk2r8y5TfNY)

### Tutorial

(Author: Jose Munoz)

Instructor: [Jose Munoz](https://munozariasjm.github.io/)

Materials: [View Here](https://github.com/munozariasjm/sr_tutorial_material)

## 2. Efficient Diffusion Models

(Author: Jun-Yan Zhu)

Instructor: [Jun-Yan Zhu]([https://www.maths.cam.ac.uk/person/mc2473](https://www.cs.cmu.edu/~junyanz/))

Slides: [View here](https://drive.google.com/file/d/1yi801aavUuu190s3v68K_JEPsUUNpnU5/view?usp=drive_link)

### Useful Materials
- [The Principles of Diffusion Models](https://arxiv.org/abs/2510.21890)
- [Flow Matching Guide and Code](https://arxiv.org/abs/2412.06264)
- [TinyML and Efficient Deep Learning Computing](https://hanlab.mit.edu/courses/2024-fall-65940)
- [Generative models as transport](https://notes.mathisgerdes.com/posts/generative-models-as-transport/)

### Tutorial

(Author: Mathis Gerdes)

Instructor: [Mathis Gerdes](https://www.mathisgerdes.com/)

Materials: 
- [Generative models as transport](https://notes.mathisgerdes.com/posts/generative-models-as-transport/)
- [Tutorial notebooks](https://github.com/mathisgerdes/iaifi-generative-models)

## 3. Computer Vision & Physics

(Author: Berthy Feng)

Instructor: [Berthy Feng](https://www.berthyfeng.com/)

Slides: *Slides to come.*

### Useful Materials
- It is recommended to set up a Google account if you don't already have one, for the purpose of running Colab notebooks.

### Tutorial

(Authors: Aneel Damaraju and Franc O)

Instructors: Aneel Damaraju and Franc O

Materials: [Google Drive folder](https://drive.google.com/drive/folders/1j8Ey5gwIO5uhfOQLWIbbj_QWoeUOY4ho?usp=drive_link)

## 4. Dynamic Simulation-Based Inference: Extracting Physics from Complex Data and Simulations

(Author: Christoph Weniger)

Instructor: [Christoph Weniger](https://www.christophweniger.com/)

Slides: *Slides to come.*

### Useful Materials
- [Dynamic SBI: Round-free Sequential Simulation-Based Inference with Adaptive Datasets](https://arxiv.org/abs/2510.13997)
- [Simulation-Based Inference: A Practical Guide](https://arxiv.org/abs/2508.12939)
- [Awesome Neural SBI](https://github.com/smsharma/awesome-neural-sbi)
- [Machine Learning for Astroparticle Physics](https://cweniger.github.io/teaching-2606-ICTP-SAIFR/)

### Tutorial

(Author: Christina Reissel)

Instructor: [Christina Reissel](https://www.linkedin.com/in/christina-reissel-06bab818a/)

Materials: [View here](https://github.com/chreissel/sbi-tutorial-iaifi26)

## 5. Hackathon

At the end of the Hackathon on Friday, August 7, we will have a block for presentations of work done on these topics. Forming groups is strongly encouraged!

Enter your team here by noon on Friday, August 7: *Link to be posted Friday morning.*

### Prompts

1. From Miles and Jose: Equation Hunting in Gaia. We will provide a table of stars drawn from the Gaia catalogue (astrometry, photometry, and derived stellar quantities), with a held-out split kept secret. Your task: use symbolic regression, plus any sort of preprocessing you'd like, to find an equation that predicts a target physical quantity as accurately and as simply as possible. Submissions go on a live leaderboard (feel free to work individually or in teams). There is no ground truth, and nobody knows what the best achievable score is. A good enough equation could potentially lead to a paper. A starter notebook will be provided with the tutorial materials.
2. From Jun-Yan and Mathis: The tutorial's spiral has a swirl strength that stays fixed throughout. Vary it, and train a single model that takes that strength as an input, so one network covers the whole family of targets. Sweep the knob and render the density morphing; then set it outside the range you trained on and check the samples against the true density. Optionally apply this idea to a family of conjugation equivariant targets on SU(3), with a trained CNF.
3. From Jun-Yan and Mathis: Train a velocity field that transports one distribution straight into another — a ring of blobs into a spiral, or two shapes you invent — and render the deformation. Then ask what makes a good pairing between the two ends, and what happens when you chain three shapes in a loop.
4. From Berthy, Franc, and Aneel: Extend InverseBench (https://github.com/devzhk/InverseBench) with a scientific inverse problem of your choice. Implement the physics-based forward model and benchmark the available diffusion-model-based sampling algorithms included in InverseBench. Optionally, extend InverseBench with a new diffusion-model-based sampling algorithm or one based on a recent paper
5. From Berthy, Franc, and Aneel: Develop a diffusion-model-based approach for solving a blind inverse imaging problem, i.e., one where the forward model is unknown. In blind inverse problems, typically the setup is that certain parameters of the forward model are unknown, and they are fit with a learned prior along with the unknown image. See https://arxiv.org/abs/2509.25269 for an example of a diffusion-model-based approach to a blind inverse problem in ptychography.
6. From Christoph and Christina: Stellar streams are among the best dynamical probes we have of the Milky Way's gravitational potential and its dark matter. A globular cluster or dwarf galaxy caught in the Galactic tide slowly unravels into a thin ribbon of stars strung along its orbit, and the ribbon's length, width, and kinematics encode both the progenitor that made it and the potential it fell through. The forward model is a stochastic, multi-Gyr disruption simulation with no tractable likelihood. Use simulation-based inference to estimate the GD1 progenitor's parameters from a binned image of its stream, marginalize the eight stripping nuisances, and check whether the posteriors are actually calibrated.
7. Work on your own project!

### Prize Categories
- Best project (effort, presentation, use of summer school topics)
- Best visualization
- Best team effort

## 6. Closing

Presented by Mike Williams: *Slides to come.*

## NSF ACCESS Instructions

[View here.](https://docs.google.com/document/d/1ZUr1OxM9A9bAa82iTC085rGvwzqvvFheDaZoDYlNrfM/edit?usp=sharing)
