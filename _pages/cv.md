---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

[MalachiPhillipsCV.pdf](https://MalachiTimothyPhillips.github.io/files/MalachiPhillipsCV.pdf)

{% include base_path %}

Education
======
* Ph.D in Computer Science, University of Illinois at Urbana-Champaign, 2023 (expected)
* B.S. in Chemical Engineering, University of Oklahoma, 2018

Work experience
======
* Aug 2018 - Present: Graduate Researcher, Dr. Paul Fischer
	* Develop nekRS, an integral contribution to the Center of Efficient Exascale Discretizations Project
	* Prepare nekRS for Frontier
	* Optimize GPU kernels through OCCA
	* Speedup code performance by a factor of 3
  * Implement several features: novel matrix-free pressure Poisson preconditioners, ALE, AVM, ...

* May 2016 - Present: Software Developer
	* Port large finite element method multiphysics simulation code to utilize GPUs through Kokkos
	* Integrate new solver techniques, such as GCRODR, into code base
	* Develop GPU kernel fusion through objected-oriented node fusion in expression graph
  
* Aug 2015 - May 2016: Undergraduate Researcher
	* Perform numerical simulations on transitional and fully-turbulent fluid flow
	* Experience writing/debugging F77 code for DNS/Lagrangian scalar tracking

* June 2014 - May 2016: Undergraduate Researcher
	* Design computational experiments to probe stability of aymloid fibrils
	* Experience running simulations in popular programs such as GROMACS and AMBER

Skills
======
* Languages
  * C++
  * Python
  * FORTRAN
* Programming Models
  * OCCA
  * Kokkos
  * MPI
  * CUDA
  * HIP
  * OpenMP
* Tools
  * LaTeX
  * Git

Publications
======
  <ul>{% for post in site.publications %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Talks
======
  <ul>{% for post in site.talks %}
    {% include archive-single-talk-cv.html %}
  {% endfor %}</ul>
  
Teaching
======
  <ul>{% for post in site.teaching %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Service and leadership
======
* President, SIAM Student Chapter at UIUC 2020-2023
