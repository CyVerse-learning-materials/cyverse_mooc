.. include:: cyverse_rst_defined_substitutions.txt
.. include:: custom_urls.txt

|CyVerse_logo|_

|Home_Icon|_
`Learning Center Home <http://learning.cyverse.org/>`_


Data Management II
---------------------

    .. admonition:: learning-objectives

       - Know how to configure Cyberduck
       - Understand how Cyberduck works
       - Upload a dataset using Cyberduck


**Description:**
In this module, we discuss how you can upload and download your dataset(s) in the Discovery Environment. This is done using Cyberduck, a 3rd party software that connects your local computer to the Data Store to enable drag-and-drop download and upload of data.


**Input Data:**

.. list-table::
    :header-rows: 1

    * - Input
      - Description
      - Example
    * - - On CyVerse
            **README.txt**
        - On your Computer
            **DE_sample_plants.fas**
      - The README file is a simple but useful way to describe folder contents.
        The fasta file contains data we will use in future steps.
      - View the |example tutorial folder|.


*Upload data with Cyberduck*
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. 	#### Comment: Step title should be descriptive (i.e. Cleaning Read data) ###


1. Download and install |Cyberduck| for your operating system.

2. Follow instructions 1-5 from the Data Store Guide to download and
   |configure Cyberduck|.

3. Log into Cyberduck, and locate the  **raw_data** folder inside your
   **tutorial_folder** in the Cyberduck display of your home directory.

4. Upload the file **DE_sample_plants.fas** to the **raw_data** folder inside
   the **tutorial_folder**.

5. In the |Discovery Environment|, click the |Data Icon| (Data Icon) to access
   your home folder.

6. Navigate to the **raw_data** folder inside your **tutorial_folder** and
   verify the upload was successful.


----

**Output/Results**

.. list-table::
    :header-rows: 1

    * - Output
      - Description
      - Example
    * - - On CyVerse
            **README.txt** (in **tutorial_folder**)
            **DE_sample_plants.fas** (in **tutorial_folder/raw_data**)
      - Now, both the readme and fasta file are co-located on the CyVerse Data
        Store.
      - View the |example tutorial folder|.

----

Self Assessment Questions
````````````````````````````

  .. admonition:: Question
       :class: admonition-question

       Q1. Why do you need Cyberduck?

       A. To conveniently chat with CyVerse support
       B. To conveniently download and upload files from your local computer
       C. To conveniently create teams on the Discovery Environment
       D. To view apps and tools on the Discovery Environment


       .. admonition:: Answer

          Correct answer is B.


  .. admonition:: Question
       :class: admonition-question

       Q2. Select all that applies: Which of these will you need to configure and access the datastore using Cyberduck

       A. SSH access
       B. CyVerse account
       C. CyVerse cyberduck connection profile
       D. Discovery Environment


       .. admonition:: Answer

          Correct answer is B, C.
	CyVerse cyberduck connection profile can be downloaded following the |Data Store Guide|.
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
