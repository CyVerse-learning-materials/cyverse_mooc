.. include:: cyverse_rst_defined_substitutions.txt
.. include:: custom_urls.txt

|CyVerse_logo|_

|Home_Icon|_
`Learning Center Home <http://learning.cyverse.org/>`_


Data Management I
-------------------

    .. admonition:: learning-objectives

       - Describe the components of FAIR data
       - Describe the Data Lifecycle
       - Download data from the Data Store
       - Create a README file and upload it to the Data Store


**Description:**

..
	#### Comment: short text description goes here ####

In this module, we introduce the concepts of FAIR data and the Data Lifecycle and demonstrate how to move data between your computer and the CyVerse Data Store.

Here is a link to the FAIR Data assessment tool mentioned in the video: |Fair Data Assessment Tool|

       .. raw:: html

           <div class="video-container">
           <iframe width="560" height="315" src="https://www.youtube.com/embed/yDptqWLfxXk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
           </div>

----

Downloading data from the Discovery Environment
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. 	#### Comment: Step title should be descriptive (i.e. Cleaning Read data) ###


1. If necessary, log into the CyVerse |Discovery Environment|.

2. Click the |Data Icon| (Data Icon) to browse your collection of files in the
   CyVerse Data Store.

3. In the top left of the page, you should see your username with a dropdown
   arrow next to it; Click on your username, then click Community Data in the
   dropdown menu.

    .. tip::

       This dropdown menu allows you to navigate between your home directory
       in the Data Store (i.e. your username), and other CyVerse data
       collections such as files shared with you (i.e. "Shared with Me"), and
       files shared by the CyVerse community (i.e. "Community Data"). You may
       also access files located in your "Trash" folder.

4. From the **Community Data** directory, scroll down until you find the
   **cyverse_training** folder, and click on it. Then navigate to the
   **cyverse_mooc** folder, then **muscle_3_8_31**, then to
   **01_muscle_input**, which will contain our example data. This is the full
   file path, which should show up as part of your URL:

   `/iplant/home/shared/cyverse_training/cyverse_mooc/muscle_3_8_31/01_muscle_input`

5. Click (Select) the checkbox next to the **DE_sample_plants.fas** file to
   select it.


6. Click on the **More Actions** button on the upper right and select the
   **Download** option to download the file to your local computer.

   .. tip::

      We don't recommend downloading many (more than 10) or large (more than
      2GB) files directly from the Discovery Environment since files transferred
      in this way will make use of HTML protocols which are slow and subject to
      failure for very large data sets. Cyberduck or iCommands (discussed below
      and in the |Data Store Guide|) are recommended for these uses.

Uploading a File to the Discovery Environment
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

1. On your computer, use any text editor to create a file called **README.txt**.
   You may wish to save it in the same place you have the
   **DE_sample_plants.fas** file (i.e. your Desktop, Downloads, etc.).

2. In the **README.txt** file, add several pieces of information about the
   **DE_sample_plants.fas** file you just downloaded:

    - Name of file: DE_sample_plants.fas
    - Type of file: FASTA file containing DNA sequences
    - Type of organism: plants

    Adding a simple README with this sort of information can quickly make your data more FAIR.

    .. note::

       Make sure you save this as a plain text file (".txt"), other file
       formats (e.g. ".docx") may not be rendered in the Discovery Environment.


3. In the Discovery Environment, click the |Data Icon| (Data Icon) to access
   your home folder; you can access this from the same dropdown menu where you
   previously selected **Community Data**.

4. Navigate to the **tutorial_folder** directory you created earlier.

5. Click the **Upload** icon in the upper right, then select **Browse Local**.
   Then navigate to your **README.txt** file and select it.

6. It may take a moment, but your **README.txt** file should now be uploaded to
   your **tutorial_folder** on the Data Store; you may need to refresh your
   web browser to see the update.


----

**Output/Results**

.. list-table::
    :header-rows: 1

    * - Output
      - Description
      - Example
    * - - On CyVerse
            **README.txt**
        - On your Computer
            **DE_sample_plants.fas**
      - The README file is a simple but useful way to describe folder contents.
        The fasta file contains data we will use in future steps.
      - View the |example tutorial folder|.

----

Self Assessment Questions
````````````````````````````


  .. admonition:: Question
       :class: admonition-question

       Q1. What do the letters in FAIR refer to?

       A. Fixable, Assessable, Interpretable, Recyclable
       B. Fast Access In Repetition
       C. Findable, Accessible, Interoperable, Reusable
       D. Fixable, Automated, Intersectional, Reducible


       .. admonition:: Answer

          The correct answer is C.


  .. admonition:: Question
       :class: admonition-question

       Q2. True or False, is FAIR data is the same as Open data?

       .. admonition:: Answer

          False. Open data must be free for use and distribution by anyone, whereas
          data can be limited in access while still being FAIR. Likewise, Open data
          are not necessarily easily findable, interoperable, or reusable.

  .. admonition:: Question
       :class: admonition-question

       Q3. Which of the following are NOT true of the process of making your data FAIR?

       A. It will be the same regardless of discipline
       B. It may require some technical skills
       C. It can be easier with CyVerse
       D. It happens on a continuum, not a binary FAIR/not FAIR


       .. admonition:: Answer

          The correct answer is A. Making your data FAIR **can** vary widely by discipline.
          For example, human health data may be subject to stricter security and more
          limited sharing, which must be accounted for when attempting to make data FAIR.

  .. admonition:: Question
       :class: admonition-question

       Q4. True or false, is adding a README file a quick way to make your data more FAIR?


       .. admonition:: Answer

          True, a README can provide quick access to metadata and is easily discovered within
          a given directory.
----

**Fix or improve this documentation**

- Search for an answer:
  |CyVerse Learning Center|
- Ask us for help:
  click |Intercom| on the lower right-hand side of the page
- Report an issue or submit a change:
  |Github Repo Link|
- Send feedback: `learning@CyVerse.org <learning@CyVerse.org>`_

----

|Home_Icon|_
`Learning Center Home <http://learning.cyverse.org/>`_

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
