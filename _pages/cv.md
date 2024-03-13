---
layout: archive
title: "Curriculum Vitae"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}
<br/>

Education
======
* Ph.D. in High Energy Experimental Nuclear Physics, Ohio University, USA (2019): GPA = 3.795
* M.S. in Physics, Ohio Unversity, USA (2016): : GPA = 3.759
* M.Sc. in Physics, Tribhuvan University, Nepal (2012)
* B.Sc. in Physics, Tribhuvan University, Nepal (2009)


Experience
======
* <ins>**Lead Modeler**, Discover Financial Services (Aug 2023- current)<ins>
   * Developing fraud detection models 

* <ins>**Post-Doctoral Researcher**, New Mexico State University (Aug 2019- July 2023)<ins>
   * Analyzing the production mechanism of an elementary particle from collision experiment at Fermilab.
      - Estimated background noise in data with **Gaussian Process Regression (GPR)** method. Montecarlo simulation technique is used to validate the background elimination process.
      - Developed “mixing method” framework to estimate the combinatorial background (random combination of tracks mimicking real signal).
      - Implemented data driven methods for **data unfolding ( Iterative Bayesian, Singular Value Decomposition, Iterative Dynamically Stabilized, Gaussian Process)** to correct the resolution and limited acceptance of the detector.
   * Working on future experiment at Fermilab to measure an intrinsic property (spin) of a subatomic particle (proton).
      - Leading the effort in **development and maintenance of the analysis software framework** (C/C++ based).
      - Implemented **Kalman Filter Algorithm** and developed energy loss model for reconstruction of particle track.
      - Developed model to estimate the realistic distribution of interaction vertices of particles across the beam volumes.
      - Developed model to simulate the full background produced in experiment.
      - Managing **data Pipeline** and analyzing data for integrity check. **Bash scripts** were written and
run as **cron job** for the purpose.
      - Implemented the use of **singularity container** of the analysis software to run the grid jobs at different cluster in OSG (Open Scince Grid) and Fermilab Grid.
      - Created the optimized set of hit pattern, **Trigger Road-sets**, to record the desired signal in the experiment. As enormous amount of data are produced in high rate, not all the data can be recorded.
      - Developed a framework to reconstruct interaction vertex of tracks with **Deep Neural Network (PyTorch)**.

* <ins>**Graduate Researcher**, Ohio University (Aug 2013- Aug 2019)<ins>
   * Analyzed data from collision experiment at Brookhaven Lab. The goal of the analysis was to help better understand the state (Quark Gluon Plasma, QGP) of our early universe In particular, measured azimuth angle correlation of two particles to study the energy loss behavior due to the presence of QGP.
      - Performed QA (Quality Analysis) of data, identified and separated the particles (photons and hadrons) of interest and corrected the data for limited detector acceptance
      - Measured the observable to quantify the two particle correlation in the azimuthal angle difference between them. The result provided the hint of the production of QGP in the collision
      - Performed various simulation checks were made to rule out the contributions of other physics in the obtained result.
   * Performed various simulation study for the Detector Design at Brookhaven Lab.
      - Evaluated different Clustering Algorithms to collect the hits deposited by single particle in detector.
      - Performed position dependent calibration of detector (Electromagnetic Calorimeter).
      - Contributed towards the software for detector design and analysis.z


<!--
* Development and maintenance of the software and analysis framework (C/C++ and CERN ROOT based) for SpinQuest Experiment at Fermi National Laboratory
* Data management for SpinQuest Experiment (Grid Computing)
* Measurement Angular decay coefficients of J/Psi mesons from p+Fe collisions at $\sqrt{s}$ = 15.065 GeV
* Electro-Magnetic Calorimeter of sPHENIX experiment at RHIC (Brookhaven National Laboratory): Design Study with Simulation
* Jet-related Two Particle Correlations Measurement in small systems at PHENIX experiment at RHIC (Brookhaven National Laboratory)
-->

<!-- 
* Summer 2015: Research Assistant
   * Github University
   * Duties included: Tagging issues
   * Supervisor: Professor Git

* Fall 2015: Research Assistant
   * Github University
   * Duties included: Merging pull requests
   * Supervisor: Professor Hub
-->

Software and Computation Skills
======
* Languages: C/C++, Python (NumPy, Pandas, scipy, lmfit, Scikit-learn, PyTorch, TensorFlow, Keras, OpenCV), Fortran, Bash Script, SQL, Latex
* Tools: GitHub, Jupyter-Notebook, Linux/Unix, Docker, Singularity, Doxygen
* Algoritm: Kalman Filter, Iterative Bayesian Unfolding, Detector hit Clustering
* HEP Packages: ROOT, GenFit, GEANT, Fun4All, RooUnfold, Scikit-HEP
* Others: Grid computing (High-Throughput Computing-HTC, Open Science Grid-OSG), Amazon Web Service (SageMaker Traning Job-SMT), IBM Watson 


Trainings and Certifications
======
* High Throughput Computing (HTC): OSG (Open Science Grid) Virtual School 2021
* Computational and Data Science: CODAS-HEP 2022 (Princeton University)
* IBM Data Science Professional Certificate (Coursera)
* IBM Machine Learning Professional Certificate (Coursera)

Leadership and Mentoring
======
* **Manager**, ["GitHub"](https://github.com/E1039-Collaboration) of SpinQuest Collaboration (2019-present)
* Providing guidance to three graduate students in the New Mexico State University (NMSU) particle physics group. 
* **Co-ordinator**, "Tracking and simulation" at SpinQuest Experiment (2019-present)
* **Co-ordinator**, "Data management" at SpinQuest Experiment (2019-present)
* **Incharge**, "Lunch with INPP seminar speaker at Ohio University" (2018-2019)
* **President**, "Nepalese Student Association at Ohio University, NEPSA" (2018-2019)
* **Founding Vice-President**, "Nepalese Student Association at Ohio University, NEPSA" (2017)
* **Instructor**, Various Under Graduate Labs (PHYS 2001, PHYS 2051, PHYS 2052, PHYS 4701): (2013-2019)

<!-- 
* Skill 1
* Skill 2
   * Sub-skill 2.1
   * Sub-skill 2.2
   * Sub-skill 2.3
* Skill 3
-->

<!--
Publications
======
-->
<!-- 
  <ul>{% for post in site.publications %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
-->

<!--
Talks
======
-->

<!-- 
  <ul>{% for post in site.talks %}
    {% include archive-single-talk-cv.html %}
  {% endfor %}</ul>
-->  

<!--
Student Advising and Mentorship
======
* Dinupa Batugedara Mohottalalage (Graduate Student, NMSU): Single Track and Dimuon Reconstruction Efficiency
* Forhad Hossain (Graduate Student, NMSU): Unfolding Study to Recover Azimuthal Asymmetry in Dimuon

Teaching 
======
* Various Under Graduate Labs (PHYS 2001, PHYS 2051, PHYS 2052, PHYS 4701): (2013-2019)
-->

<!-- 
  <ul>{% for post in site.teaching %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
-->

Collaborations
======
* SpinQuest (Experiment at Fermilab)
* SeaQuest (Future Experiment at Fermilab)
* PHENIX (Experiment at Brookhaven National Lab)
* sPHENIX (Experiment at Brookhaven National Lab)

Professional Memberships
======
* American Physical Society (APS)
* Nepal Physical Society (NPS)


Honors and Awards
======
* Ranked among top 5% in my M. Sc. class, Tribhuvan Univ. 2012
* Dean’s Merit Scholarship, Institute of Science and Technology, Tribhuvan Univ. 2011
* Ranked 7th among 1000+ test-takers in the qualifying examination of the M.Sc. program in Physics 2010
* Dean’s Merit Scholarship, Tri-Chandra Multiple Campus, Tribhuvan Univ. 2006 - 2009
