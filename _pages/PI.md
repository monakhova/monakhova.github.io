---
layout: default
permalink: /kristina/
title: PI
nav: true
nav_order: 6
category: PI

profile:
  align: left
  image: Kristina_Monakhova.jpg
  image_circular: true # crops the image to make it circular
    

---
<!-- pages/PI.md -->
<div class="post">
    <div class="profile float-{%- if page.profile.align == 'left' -%}left{%- else -%}right{%- endif -%}">
	  {%- assign profile_image_path = page.profile.image | prepend: 'assets/img/' -%}
        {% if page.profile.image_circular %}
              {%- assign profile_image_class = "img-fluid z-depth-1 rounded-circle" -%}
        {% else %}
              {%- assign profile_image_class = "img-fluid z-depth-1 rounded" -%}
        {% endif %}
        {% include figure.html
            path=profile_image_path
            class=profile_image_class
            alt=page.profile.image -%}   
          <div class="address">
		 <p> <span class="font-weight-bold"> </span></p>
	      <!--<p>Gates Hall</p>
	      <p>Ithaca, NY</p>-->
            <div class="social">
              <div class="contact-icons">
                {% include social.html %}
              </div>
		  </div>
          </div>
    </div>
        <header class="post-header">
          <h1 class="post-title">
           {{ site.first_name }} <span class="font-weight-bold">{{ site.last_name }}</span>, Ph.D.
          </h1>
      <p><b>Assistant Professor</b> <br> Department of Computer Science <br> Cornell University</p>
	  </header>

</div>

<div>
<p>		
I am an Assistant Professor in the <a href="http://www.cs.cornell.edu/">Department of Computer Science</a> at Cornell. I work on co-designing optics and algorithms to create better, smaller, and more capable cameras and microscopes.</p>
<p>
Before Cornell, I was a postdoctoral fellow at MIT working with <a href="https://www.rle.mit.edu/yougroup/">Sixian You</a> and <a href="https://meche.mit.edu/people/faculty/gbarb@mit.edu">George Barbastathis</a>, and supported by the <a href="https://engineering.mit.edu/the-mit-postdoctoral-fellowship-program-for-engineering-excellence/">MIT Postdoctoral Fellowship for Engineering Excellence.</a>  I obtained my PhD in Electrical Engineering and Computer Sciences from UC Berkeley with <a href="http://www.laurawaller.com/">Laura Waller</a>. During my PhD, I was affiliated with the Berkeley Artificial Intelligence Research (BAIR) Lab and was supported by the NSF GRFP fellowship. My PhD dissertation was on <a href="https://www2.eecs.berkeley.edu/Pubs/TechRpts/2022/EECS-2022-177.html">Physics-Informed Machine Learning for Computational Imaging</a>.</p>

<p>I lead the <span class="font-weight-bold"><a href="{{ '/' | relative_url }}">Computational Imaging Lab @ Cornell</a></span> and advise several wonderful <span class="font-weight-bold"><a href="{{ '/team/' | relative_url }}">PhD students</a></span>.</p>

<p>
email: monakhova[at]cornell.edu <br>
office: Gates 446
</p>

<h2>teaching</h2>
<p>
<span class="font-weight-bold"><a href="https://www.cs.cornell.edu/courses/cs6662/2024fa/">CS6662</a></span>: Computational Imaging, Cornell University, Fall 2024
</p>
<h4>guest lectures</h4>
<p>
<b>ECE 285</b>: Computational Imaging Systems, UCSD, <span class="font-italic">'Robust and physics-informed machine learning for low light imaging'</span>, Spring 2024 <br>
<b>6.300</b>: Signal Processing, MIT, <span class="font-italic">'Computational Imaging: using signal processing to make better imaging systems'</span>, Spring 2024	
</p>


<h2><a href="{{ '/news/' | relative_url }}" style="color: inherit;">news</a></h2>
{%- include news.html limit=true %}

<h2><a href="{{ '/publications/' | relative_url }}" style="color: inherit;">selected publications</a></h2>
{%- include selected_papers.html %}
</div>