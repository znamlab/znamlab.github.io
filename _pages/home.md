---
layout: homelay
excerpt: "Znamenskiy lab at the Francis Crick Institute studying the relationships between gene expression, connectivity and function of cortical neurons."
sitemap: false
permalink: /
---

<div class="col-sm-12">
<img class="float-left biglogo" src="{{ site.url }}{{ site.baseurl }}/images/lab_logo_color.svg">
<div class="bigtitle titlebox">
Specification and Function of Neural Circuits Laboratory
</div>
</div>

<div class="col-sm-12">
  <p>
  We are <a href="https://www.crick.ac.uk/research/labs/petr-znamenskiy">a laboratory at the Francis Crick Institute</a>
  in London studying the relationships between gene expression, connectivity and
  function of cortical neurons. Using primary visual cortex as a model, we aim
  to understand how the activity of specialized classes of cortical neurons
  enables animals to see, how it emerges from the structure of their connections,
  and how these connections are established during development. To answer these
  questions we combine the approaches of molecular and systems neuroscience and
  develop new tools to study the relationships between gene expression
  and connectivity of neurons at scale.
  </p>
</div>

<div class="col-12" markdown="1">
<div class="carousel slide" data-ride="carousel">
  <div class="carousel-inner" role="listbox" style="max-width:900px; max-height:600px !important;">
    {% for image in site.data.gallery %}
    {% if forloop.index == 1 %}
    <div class="carousel-item active">
    {% else %}
    <div class="carousel-item">
    {% endif %}
      <img class="d-block w-100" src="{{ site.url }}{{ site.baseurl }}/images/carousel/{{ image.name }}" alt="{{ image.alt }}">
    </div>
    {% endfor %}
  </div>
</div>

# Our collaborators

## Collaborators at the Crick

- [Dr. Jonny Kohl, State-Dependent Neural Processing Laboratory](https://www.kohl-lab.org/)
- [Dr. Flor Iacaruso, Neuronal Circuits and Behaviour Laboratory](https://www.crick.ac.uk/research/labs/flor-iacaruso)
- [Dr. Katharina Schmack, Neural Circuits and Immunity in Psychosis Laboratory](https://www.crick.ac.uk/research/labs/katharina-schmack)
- [Dr. Leanne Li, Cancer-Neuroscience Laboratory](https://www.crick.ac.uk/research/labs/leanne-li)

## External collaborators

- [Prof. Dinu Florin Albeanu, Cold Spring Harbor Laboratory](http://albeanulab.labsites.cshl.edu/)
- Dr. Mathieu Bourdenx, UK Dementia Research Institute, UCL
- [Dr. Harry Bulstrode, Wellcome-MRC Cambridge Stem Cell Institute](https://www.stemcells.cam.ac.uk/people/pi/bulstrode)
- [Prof. Kenneth Harris, UCL](https://www.ucl.ac.uk/cortexlab/)

</div>

<div class="col-sm-12">
<h2>Funding</h2>
<p>
We are supported by core funding from
<a href="http://www.crick.ac.uk">the Francis Crick Institute</a>. The Crick is
a partnership between
<a href="https://mrc.ukri.org/">the Medical Research Council</a>,
<a href="https://www.cancerresearchuk.org/">Cancer Research UK</a>,
<a href="https://wellcome.org/">the Wellcome Trust</a>,
<a href="https://www.ucl.ac.uk/">UCL (University College London)</a>,
<a href="https://www.imperial.ac.uk/">Imperial College London</a> and
<a href="https://www.kcl.ac.uk/">King's College London</a>.
</p>

<p></p>
</div>
