.. include:: cyverse_rst_defined_substitutions.txt
.. include:: custom_urls.txt

|CyVerse_logo|_

|Home_Icon|_
`Learning Center Home <http://learning.cyverse.org/>`_


Data Management III
--------------------

    .. admonition:: learning-objectives

       - Apply metadata in the Discovery Environment interface
       - Share data with other CyVerse users

**Description:**

In this module, we introduce how to apply metadata in the Discovery Environment and demonstrate how to share data with other CyVerse users.

       .. raw:: html

           <div class="video-container">
           <iframe width="560" height="315" src="https://www.youtube.com/embed/shqShSoTOW8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
           </div>
----

**Input Data:**

.. list-table::
    :header-rows: 1

    * - Input
      - Description
      - Example
    * - - **README.txt**
          **DE_sample_plants.fas**
      - These are the metadata and dataset uploaded previously.
      - View the |example tutorial folder|.

*Editing Metadata on Single Files in the Discovery Environment*
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

  1. If necessary, log into the CyVerse |Discovery Environment|.

  2. Click the |Data Icon| (Data Icon) to browse your collection of files in the
     CyVerse Data Store.

  3. Navigate to the **raw_data** folder inside **tutorial_folder** and select
     (checkbox) the **DE_sample_plants.fas** file uploaded previously.

  4. Under the **More Actions** menu, click on the **Metadata** choice.
     You will see existing metadata for the file/folder in the Attribute,
     Value, Unit (AVU) format.

*Adding metadata*

  1. Click the “+ Add Metadata” button to add a new entry. Then follow the
     directions for editing metadata below.

*Editing or deleting metadata*

  1. Use the “pencil” icon to edit an existing entry or the “trash can”
     icon to delete an entry.

  2. After you have made any edits or deletion, click ‘Save’ (on the top right
     of the screen) to save all entries and apply the metadata.


*Apply metadata on multiple files in the Discovery Environment*
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

It is possible to add or edit metadata on multiple files in the Discovery Environment by uploading a spreadsheet with this metadata. The spreadsheet can be designed to follow a metadata format or standard, or contain whatever metadata entries you want associated with a set of files. See the |Metadata documentation in the Data Store Guide| for more details.


**Output/Results**

.. list-table::
    :header-rows: 1

    * - Output
      - Description
      - Example
    * - **DE_sample_plants.fas** with metadata applied.
      - Although the file itself has not been edited, viewing the metadata in
        the Discovery Environment lets you view all annotations you have made
        to the file.
      - View |DE_sample_plants.fas| with metadata applied (you will need to
        view the file in the Discovery Environment to view the associated
        metadata; select the file and click **More Actions** and then **Metadata**).


*Data Sharing in the Discovery Environment*
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

  1. If necessary, log into the CyVerse |Discovery Environment|.

  2. Click the |Data Icon| (Data Icon) to browse your collection of files in the
     CyVerse Data Store.

  3. Navigate to the **tutorial_folder** created previously and select
     (checkbox) the folder. Click the **Share** button.

  4. In the ‘search for users’ field search for the CyVerse user you wish to
     share with by searching for their username or email address.

  5. Next, under ‘Permissions’ choose what permission you want to grant the
     person you are sharing this file with.

     .. tip::

     	  See more on |Sharing Permissions| in the Data Store Guide.

  6. Once you are finished, click Done to begin sharing. The user will be
     notified that a file has been shared with them.


----

Self Assessment Questions
````````````````````````````

  .. admonition:: Question
       :class: admonition-question

       Q1. Use the readme file from Data Management I and apply the metadata correctly to your file using the DE.

       .. admonition:: Answer

           Click |DE_sample_plants.fas| to see how it should look and compare your results; click the **More Actions** menu, then **Metadata**.


  .. admonition:: Question
       :class: admonition-question

       Q2. Which of the following are true about metadata in the CyVerse Data Store?

       A. Are structured in Attribute-Value-Unit in CyVerse
       B. Contain information about the corresponding data file
       C. Are discoverable in CyVerse through ElasticSearch
       D. Contain results of experiments


       .. admonition:: Answer

          Correct answer is A, B, and C

  .. admonition:: Question
       :class: admonition-question

       Q3. Select the correct statement: Sharing of research data in CyVerse...

       A. Will be sent to collaboration partners automatically
       B. Will transfer of ownership to a collaborator
       C. Enables cross-institutional collaboration
       D. Ensures that data stays in a single accessible location you control
          access to.

       .. admonition:: Answer

          Correct answer is C, D

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
