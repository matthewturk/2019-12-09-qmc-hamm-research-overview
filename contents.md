<!-- .slide: class="titleslide" -->

# QMC-HAMM Research Overview

<div style="height: 6.0em;"></div>

## Matthew Turk

<p style="text-align: right;" data-markdown=true><tt>mjturk@illinois.edu</tt></p>

---

## Some Background ... 

> "What's in this for you, Matt?"
>
> &mdash; <cite>Everyone Else in This Room, 2019</cite>

<ul>
<li class="fragment">Computational <b>astrophysicist</b> by training</li>
<li class="fragment">Developed simulation platforms and analysis <b>tools</b> for astrophysics</li>
<li class="fragment">Worked in interdisciplinary applications, study <b>communities</b> of practice in open source scientific software</li>
<li class="fragment">Tenure-track at the School of Information Sciences, developing and implementing a <b>grammar</b> of volumetric analysis
</ul>

---

## My Interest in This

I have two principle interests in this project.

<p class="fragment"><b>Physical Sciences:</b> I do have an interest in hydrogen!  It turns out, it's really important to how stars form in the early universe!</p>
<p class="fragment"><b>Information Sciences:</b> Understanding the dynamics of group interactions around software, the development of systems for preserving and sharing data, and the mechanisms by which researchers analyze and process data.  These are the core components of my research agenda.</p>
<p class="fragment">Let's talk about the first one first!</p>

---

## Cartoon History of the Universe

<div class="multiCol">
<div class="col">
<div class="fig-container" data-style="height: 600px;" data-file="figures/collapse_heating.html" data-markdown=true>
</div>
</div>
<div class="col" data-markdown=true>
<p class="fragment" data-fragment-index="0">After recombination, the universe was in a nearly-but-not-totally homogeneous state, seeded with instabilities and with a few residual electrons.</p>
<div class="fragment" data-fragment-index="1">
<p>Early-on, dark matter clumps collected and formed "halos," drawing in baryonic material.</p>
<p>This process converted potential energy into thermal energy, heating the baryonic matter, which shed the thermal energy through radiative processes.</p>
</div>
<p class="fragment" data-fragment-index="2">Eventually, this cloud becomes fully-molecular through the three-body interaction and forms an accretion disk.</p>
</div>
</div>

---

## Molecular Hydrogen

<div class="multiCol">
<div class="col" data-markdown=true>
<div class="fig-container" data-style="height: 400px;" data-file="figures/three_body.html" data-markdown=true>
</div>
<div class="fragment" data-fragment-index="1">
$$
\begin{align}
\mathrm{H} + \mathrm{H} + \mathrm{H} & \rightarrow \mathrm{H}_2 + \mathrm{H} \\
\mathrm{H}_2 + \mathrm{H} & \rightarrow \mathrm{H} + \mathrm{H} + \mathrm{H} \\
\mathrm{H}_2 + \mathrm{H} + \mathrm{H} & \rightarrow \mathrm{H}_2 + \mathrm{H}_2 \\
\mathrm{H}_2 + \mathrm{H}_2 & \rightarrow \mathrm{H} + \mathrm{H} + \mathrm{H}_2
\end{align}
$$
</div>
</div>
<div class="col" data-markdown=true>
<p data-markdown=true>In an environment absent heavy elements, the mechanisms by which gas can cool are quite limited.  The principal coolant is molecular hydrogen, which forms first via electron association ($\mathrm{H}^{-}$) and then through three body interactions.</p>
<p class="fragment" data-markdown=true>
This formation channel results in molecular hydrogen that begins in an excited state.
</p>
<p class="fragment" data-markdown=true>
This molecule then quickly de-excites through collisions, resulting in a net heating of the gas by roughly 4.48 eV per molecule.
</p>
</div>
</div>

---

## Data Sharing

How can we make our data [FAIR](https://www.force11.org/group/fairgroup/fairprinciples)?

 * Findable
 * Accessible
 * Interopable
 * Reusable

---

## Data Sharing: Findable

 1. (meta)data are assigned a globally unique and eternally persistent identifier.
 2. data are described with rich metadata.
 3. (meta)data are registered or indexed in a searchable resource.
 4. metadata specify the data identifier.

---

## Data Sharing: Accessible

1.  (meta)data are retrievable by their identifier using a standardized communications protocol.
  1. the protocol is open, free, and universally implementable.
  2. the protocol allows for an authentication and authorization procedure, where necessary.
2. metadata are accessible, even when the data are no longer available.

---

## Data Sharing: Interoperable

 1. (meta)data use a formal, accessible, shared, and broadly applicable language for knowledge representation.
 2. (meta)data use vocabularies that follow FAIR principles.
 3. (meta)data include qualified references to other (meta)data.

---

## Data Sharing: Reusable

 1. meta(data) have a plurality of accurate and relevant attributes.
    1. (meta)data are released with a clear and accessible data usage license.
    2. (meta)data are associated with their provenance.
    3. (meta)data meet domain-relevant community standards.

---

## Data Sharing: Implementation

The "yt hub" is a flexible data storage system, based on [girder](https://girder.readthedocs.org/), using technology developed during the [Whole Tale](https://wholetale.org/) project to provide:

 * Partial or complete access to datasets or their subsets
 * Filesystem-like access to data in interactive environments
 * Multiple, flexible storage backends
 * In-browser visualization and catalog access

(More on Whole Tale [and some of its cool features](https://matthewturk.github.io/post/exploration-whole-tale/), but let's take a look at it.)

---

<!-- .slide: data-background-image="images/clouds.jpg"
             data-background-size="cover" data-background-repeat="none" -->

---

<!-- .slide: data-background-image="https://upload.wikimedia.org/wikipedia/commons/b/bd/Kelvin_Helmholz_wave_clouds.jpg"
             data-background-size="cover" data-background-repeat="none" class="full" -->

<div class="multiCol">
<div class="col" data-markdown=true>
</div>
<div class="col fragment fade-in" style="opacity:0.7;background-color: white;" data-markdown=true>
$$\begin{aligned}{\partial \rho  \over \partial t}+\nabla \cdot (\rho \mathbf{v}) &= 0\\
{\frac {\partial \mathbf {v} }{\partial t}}+\mathbf {v} \cdot \nabla \mathbf {v} +{\frac {\nabla p}{\rho }}&=\mathbf {g}\\
{\partial e \over \partial t}+\mathbf {v} \cdot \nabla e+{\frac {p}{\rho }}\nabla \cdot \mathbf {v} &=0\end{aligned}$$
</div>
</div>

<!--<p class="mediumtext centered"><a href="https://commons.wikimedia.org/wiki/File:Kelvin_Helmholz_wave_clouds.jpg">Brocken Inaglory [CC BY-SA 4.0], via Wikimedia Commons</a></p> -->

---

<div class="multiCol">
<div class="col">
<div class="fig-container" data-style="height: 600px;" data-file="figures/kh_example.html" data-scroll="no" data-markdown=true>
</div>
</div>
<div class="col" data-markdown=true>
$$\begin{aligned}{\partial \rho  \over \partial t}+\nabla \cdot (\rho \mathbf{v}) &= 0\\
{\frac {\partial \mathbf {v} }{\partial t}}+\mathbf {v} \cdot \nabla \mathbf {v} +{\frac {\nabla p}{\rho }}&=\mathbf {g}\\
{\partial e \over \partial t}+\mathbf {v} \cdot \nabla e+{\frac {p}{\rho }}\nabla \cdot \mathbf {v} &=0\end{aligned}$$
</div>
</div>

---

# Vocabulary of Data Analysis

<div class="appearing_row" style="margin-top: 1em;">
  <div class="fragment" data-fragment-index=1>
  <div class="right_align">
    <span><i class="fas fa-align-right fa-5x"></i></span>
  </div>
  </div>
  <div class="fragment" data-fragment-index=1>
  <div class="left_align" style="font-size: 200%;">
    Registration
  </div>
  </div>
</div>

<br clear="all"/>

<div class="appearing_row" style="margin-top: 1em;">
  <div class="fragment" data-fragment-index=2>
  <div class="right_align">
    <span><i class="fas fa-calculator fa-5x"></i></span>
  </div>
  </div>
  <div class="fragment" data-fragment-index=2>
  <div class="left_align" style="font-size: 200%;">
    Transformation
  </div>
  </div>
</div>

<br clear="all"/>

<div class="appearing_row" style="margin-top: 1em;">
  <div class="fragment" data-fragment-index=3>
  <div class="right_align">
    <span><i class="fas fa-object-group fa-5x"></i></span>
  </div>
  </div>
  <div class="fragment" data-fragment-index=3>
  <div class="left_align" style="font-size: 200%;">
    Selection
  </div>
  </div>
</div>

<br clear="all"/>

<div class="appearing_row" style="margin-top: 1em;">
  <div class="fragment" data-fragment-index=4>
  <div class="right_align">
    <span><i class="fas fa-mortar-pestle fa-5x"></i></span>
  </div>
  <div class="fragment" data-fragment-index=4>
  <div class="left_align" style="font-size: 200%;">
    Reduction
  </div>
  </div>
</div>

<br clear="all"/>

---

<div class="multiCol">
<div class="col">

# Registration

<p class="fragment">Data is laid out on <b>disk</b> in some manner that may or may not correspond to the spatial organization or physical meaning of what it represents.</p>

<p class="fragment">This data can be laid out in a data structure in <b>memory</b> that represents its logical ordering, with axes and dimensions.</p>

<p class="fragment">Finally, we can register one or multiple datasets in a consistent <b>spatial</b> representation so that we can query fields at specific locations and define $f(\mathbf{x})$.</p>

</div>

<div class="col">
<div class="fig-container" data-file="figures/volume_layout.html" data-preload data-style="height: 600px;">
</div>
</div>
</div>

---

<div class="multiCol">
<div class="col">

# Registration

<p class="fragment">Given a functional form, discretely sampled data can also be registered for analysis, regardless of its layout on disk.</p>

<div class="fragment" data-markdown=true>
<p>This data may carry with it attributes regarding the density of samples, its neighbors, and fundamental quantities, which can be input into a sampling function over a location.</p>

`$$ A(\mathbf{r}) = \int A(\mathbf{r}')W(|\mathbf{r} - \mathbf{r}'|, h)\mathrm{d} V(\mathbf{r}') $$`
</div>

</div>

<div class="col">
<div class="fig-container" data-file="figures/particle_layout.html" data-preload data-style="width: 500px;">
</div>
</div>
</div>


---

<div class="multiCol">
<div class="col">
<div class="fig-container" data-file="figures/galaxy_transformations.html" data-preload data-style="height: 768px;">
</div>
</div>
<div class="col" data-markdown=true>

# Transformations

<p class="fragment">"Primitive" variables: $\rho, \mathbf{v}, e, ...$ can be combined in many different ways to produce fields that exist <i>in potentia</i>.</p>
<p class="fragment">Registration enables combinations at fixed spatial locations.</p>
<p class="fragment">For example, we can apply the arithmetic manipulation:
$$|v| = \sqrt{v_x^2 + v_y^2}$$
</p>
</div>
</div>

---

<div class="multiCol">
<div class="col" data-markdown=true>

# Selection

<p>Points can be filtered based on their connectivity, spatial organization, or criteria from one or more field values.</p>
</div>
<div class="col">
<div class="fig-container" data-file="figures/kh_operations.html" data-preload data-style="height: 768px;">
</div>
</div>
</div>

---

# Reductions

We can apply reductions along axes, paths and non-trivial manifolds.

<div class="fig-container" data-file="figures/kh_path.html" data-preload data-style="height: 600px;" data-scroll="no">
</div>

---

# Composability

<div class="fig-container" data-file="figures/cosmology.html" data-preload data-style="height: 768px;">

---

# Two-Headed Approach

<p class="fragment">
Understand vocabulary and implementation of volumetric analysis in domain sciences, such as Quantum Monte Carlo.
</p>
<p class="fragment">
Develop an implementation of this descriptive grammar of analysis.
</p>

---

# Volumetric Analysis Platform

<div class="multiCol">
<div class="col">
<img src="images/yt_logo.svg">
</div>
<div class="col">
The `yt` platform for analysis is a mechanism for abstracting the underlying
operations and building reproducible analysis procedures, independent of data
representation and distribution.

[yt-project.org](https://yt-project.org/)

<p class="fragment">
The implementation of a physically-aware grammar of analysis of this data will
foster better connections between machine learning models and data from the
natural sciences.
</p>

</div>
</div>

---

<!-- .slide: class="titleslide" -->

# Thank you!
