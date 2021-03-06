.. include:: cyverse_rst_defined_substitutions.txt
.. include:: custom_urls.txt

|CyVerse_logo|_

|Home_Icon|_
`Learning Center Home <http://learning.cyverse.org/>`_

**Introduction to CyVerse Self-Guided Course: CyVerse USA**
==============================================================


Goal
----

This is a short self-guided course that will take you through the basics of
using CyVerse.

  .. tip::
        **See other versions of this documentation (CyVerse UK and CyVerse Austria)**

        |readthedocs|

        In the lower-left hand side of the screen, change the version of this
        documentation from cyverse-us to one of the other documentation sets
        developed for this online guide (*cyverse-uk* or *cyverse-at*) to see
        specifics for those installations.

----

Tutorial Maintainer(s)
------------------------

Who to contact if this guide needs fixing. You can also email
`learning@CyVerse.org <learning@CyVerse.org>`_

.. list-table::
    :header-rows: 1

    * - Maintainer
      - Institution
      - Contact
    * - Michael Culshaw-Maurer
      - CyVerse / University of Arizona
      - culshawmaurer@arizona.edu
    * - Jason Williams
      - CyVerse / Cold Spring Harbor Laboratory
      - williams@cshl.edu
    * - Tyson Lee Swetnam
      - CyVerse / University of Arizona
      - tswetnam@cyverse.org
----

.. toctree::
	:maxdepth: 2

  Tutorial home <self>
  Course Overview <step1.rst>
  CyVerse Background <step2.rst>
  Tour of the Discovery Environment <step3.rst>
  Data Management I <step4.rst>
  Data Management II <step5.rst>
  Data Management III <step6.rst>
  Analysis with the Discovery Environment <step7.rst>
  Interactive Analyses <step8.rst>
  Conclusion and Advanced Applications <final_step.rst>
	Delete this example guide page <example_directives_delete.rst>


Prerequisites
-------------

Downloads, access, and services
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

*In order to complete this tutorial you will need access to the following services/software*

..
	#### comment: delete any row not needed in this table ####

.. list-table::
    :header-rows: 1

    * - Prerequisite
      - Preparation/Notes
      - Link/Download
    * - CyVerse account
      - You will need a CyVerse account to complete this exercise
      - |CyVerse User Portal|
    * - VICE access
      - You must have permission to use Discovery Environment VICE
        applications; request access on the user portal (under 'Services')
      - |CyVerse User Portal|
    * - Cyberduck
      - Standalone software for upload/download to Data Store
      - Download |Cyberduck|

Platform(s)
~~~~~~~~~~~

*We will use the following CyVerse platform(s):*


.. list-table::
    :header-rows: 1

    * - Platform
      - Interface
      - Link
      - Platform Tour
    * - Data Store
      - GUI/Command line
      - |Data Store|
      - |Data Store Guide|
    * - Discovery Environment
      - Web/Point-and-click
      - |Discovery Environment|
      - |Discovery Environment Guide|


Application(s) used
~~~~~~~~~~~~~~~~~~~
..
	#### Comment: these tables are examples, delete whatever is unnecessary ####

**Discovery Environment App(s):**

.. list-table::
    :header-rows: 1

    * - App name
      - Version
      - Description
      - App link
      - Notes/other links
    * - Muscle
      - 3.8.31
      - Multiple sequence aligner
      -	|CyVerse_launch MUSCLE|
      - |Original App documentation muscle|
    * - Rocker
      - Latest
      - RStudio VICE application
      -	|CyVerse_rocker_launch|
      - |Original App documentation rocker|
----

**Fix or improve this documentation**

- Search for an answer:
  |CyVerse Learning Center|
- Ask us for help:
  click |Intercom| on the lower right-hand side of the page
- Report an issue or submit a change:
  |Github Repo Link|
- Send feedback: `learning@CyVerse.org <learning@CyVerse.org>`_

.. comment:

   Uncomment the below and fix with this repo's information if citing

   **Citation**

   You may cite this work as:
   [Repository Title]
   [Author(s)]
   [Repository Release Version]
   [DOI: Zenodo DOI link (generated from Github Release/Zenodo)]
----

|Home_Icon|_
`Learning Center Home <http://learning.cyverse.org/>`__


.. Comment: Place Images Below This Line
   use :width: to give a desired width for your image
   use :height: to give a desired height for your image
   replace the image name/location and URL if hyperlinked


 .. |Clickable hyperlinked image| image:: ./img/IMAGENAME.png
    :width: 500
    :height: 100
 .. _CyVerse logo: http://learning.cyverse.org/

 .. |Static image| image:: ./img/IMAGENAME.png
    :width: 25
    :height: 25



.. Comment: Place URLS Below This Line

   # Use this example to ensure that links open in new tabs, avoiding
   # forcing users to leave the document, and making it easy to update links
   # In a single place in this document

   .. |Substitution| raw:: html # Place this anywhere in the text you want a hyperlink

      <a href="REPLACE_THIS_WITH_URL" target="blank">Replace_with_text</a>
