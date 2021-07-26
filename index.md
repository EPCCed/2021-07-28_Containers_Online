---
layout: lesson
root: .  # Is the only page that doesn't follow the pattern /:path/index.html
permalink: index.html  # Is the only page that doesn't follow the pattern /:path/index.html
venue: Online
address: 
country: "UK"
language: "English"
latlng: 
humandate: 10:00-16:00 BST, 28 - 29 July 2021
humantime: 10:00-16:00 BST
startdate: 2021-07-28
enddate: 2021-07-29
instructor: ["Andy Turner", "Jeremy Cohen"]
helper: []
email: ["support@archer2.ac.uk"]
collaborative_notes: https://pad.archer2.ac.uk/p/210728-Containers
---
This course aims to introduce the use of containers with the goal of using them to effect reproducible computational environments. Such environments are useful for ensuring reproducible research outputs and for simplifying the setup of complex software dependencies across different systems. The course will mostly be based around the use of Docker containers but the material will be of use for whatever container technology you plan to, or end up, using. We will also introduce the Singularity container environment which is compatible with Docker and designed for use on multi-user systems (such as HPC resources).

> ## After completing this session you should:
> - Have an understanding of what Docker and Singularity containers are, why they are useful
>  and the common terminology used
> - Have a working Docker installation on your local system to allow you to
>  use containers
> - Understand how to use existing Docker and Singularity containers for common tasks
> - Be able to build your own Docker containers by understanding both the role
>  of a `Dockerfile` in building containers, and the syntax used in `Dockerfile`s
> - Be able to build your own Singularity containers from Singularity definition files
>  and understand the syntax used in definition files
> - Understand how to manage Docker containers on your local system and Singularity
>  containers on a remote HPC system
> - Appreciate issues around reproducibility in software, understand how 
>  containers can address some of these issues and what the limits to
>  reproducibility using containers are
> - See how Singularity containers can work even when running parallel MPI programs
>  on an HPC system
{: .objectives}

The practical work in this lesson is primarily aimed at using Docker on your own laptop, building Singularity containers on your own laptop (using a Docker container!) and using Singularity containers on a remote high performance computing (HPC) system. Beyond your laptop, software container technologies such as Docker can also be used in the cloud and on HPC systems. Some of the material in this lesson will be applicable to those environments too.

This site covers day 1 of the course (focussed on Docker). The material for day 2 (focussed on Singularity) can be found at: [Introduction to Singularity](https://epcced.github.io/2021-07-29_Singularity_Online/)

<h2 id="general">General Information</h2>

{% comment %}
  LOCATION

  This block displays the address and links to maps showing directions
  if the latitude and longitude of the workshop have been set.  You
  can use https://itouchmap.com/latlong.html to find the lat/long of an
  address.
{% endcomment %}
<p id="where">
  <strong>Where:</strong>
  This course will be taught online via Blackboard Collaborate. All attendees will
  be sent the joining link prior to the event.
</p>

{% comment %}
  DATE

  This block displays the date and links to Google Calendar.
{% endcomment %}
{% if page.humandate %}
<p id="when">
  <strong>When:</strong>
  {{page.humandate}}.
  {% include workshop_calendar.html %}
</p>
{% endif %}

{% comment %}
  SPECIAL REQUIREMENTS

  Modify the block below if there are any special requirements.
{% endcomment %}
<p id="requirements">
  <strong>Requirements:</strong> Participants must bring a laptop with a
  Mac, Linux, or Windows operating system (not a tablet, Chromebook, etc.) that they have administrative privileges
  on. They should have a few specific software packages installed (listed
  <a href="#setup">below</a>). They are also required to abide by the <a href="https://www.archer2.ac.uk/about/policies/code-of-conduct.html">ARCHER2 Code of Conduct</a>.
</p>

{% comment %}
  ACCESSIBILITY

  Modify the block below if there are any barriers to accessibility or
  special instructions.
{% endcomment %}
<p id="accessibility">
  <strong>Accessibility:</strong> We are committed to making this workshop
  accessible to everybody.
</p>
<p>
  Materials will be provided in advance of the workshop and
  large-print handouts are available if needed by notifying the
  organizers in advance.  If we can help making learning easier for
  you please get in touch (using contact details below) and we will
  attempt to provide them.
</p>

{% comment %}
  CONTACT EMAIL ADDRESS

  Display the contact email address set in the configuration file.
{% endcomment %}
<p id="contact">
  <strong>Contact</strong>:
  Please email
  {% if page.email %}
    {% for email in page.email %}
      {% if forloop.last and page.email.size > 1 %}
        or
      {% else %}
        {% unless forloop.first %}
        ,
        {% endunless %}
      {% endif %}
      <a href='mailto:{{email}}'>{{email}}</a>
    {% endfor %}
  {% else %}
    to-be-announced
  {% endif %}
  for more information.
</p>

<hr/>

> ## Prerequisites
>
> - You should have basic familiarity with using a command shell, and the lesson text will at times request that you "open a shell window", with an assumption that you know what this means.
>   - Under Linux or macOS it is assumed that you will access a `bash` shell (usually the default), using your Terminal application.
>   - Under Windows, Powershell and Git Bash should allow you to use the Unix instructions.
> - As an item of setup, it is assumed that you have a directory named `container-playground` that you are able to `cd` to using your command shell, *and* are also able to find using your computer's graphical file browser (e.g., Finder on macOS or Windows Explorer). A simple way to achieve this is to create your `container-playground` directory within your computer's `Desktop` folder. (See the [Software Carpentry Shell lesson](https://swcarpentry.github.io/shell-novice/) for more details.)
> - The lessons will sometimes request that you use a text editor to create or edit files in particular directories. It is assumed that you either have an editor that you know how to use that runs within the working directory of your shell window (e.g. `nano`), or that if you use a graphical editor, that you can use it to read and write files into the working directory of your shell.
{: .prereq}

<h2 id="setup">Getting Started</h2>

<p>To get started, follow the directions on the <a href="setup.html">Setup</a> page to ensure you have installed the Docker software, have registered for a Dockerhub account, have an SSH client available and have registered a user account on ARCHER2 (the HPC
facility we will be using for the Singularity part of the course).</p>

<hr/>

<h2>Collaborative Document</h2>

During the course, we will make use of a collaborative document known as an *Etherpad*. You
can find the document at:

 - [Course Etherpad]({{page.collaborative_notes}})


{% include links.md %}

{% comment %}

TODO: systematically check for Windows-isms

<!--  LocalWords:  prereq links.md endcomment
 -->
{% endcomment %}
