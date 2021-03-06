.. include:: cyverse_rst_defined_substitutions.txt
.. include:: custom_urls.txt

|CyVerse_logo|_

|Home_Icon|_
`Learning Center Home <http://learning.cyverse.org/>`_


Interactive Analyses
-----------------------

    .. admonition:: learning-objectives

       - Request VICE access.
       - Launch and access VICE application.
       - Configure the VICE application and run an analysis.
       - Save the outputs of a VICE application to your Data Store.



**Description:**

The Visual Interactive Computing Environment (|VICE|) allows you to work with
popular interactive data science applications such JupyterLab, RStudio, Linux
shell and others. In this exercise we will cover a simple introductory use case
that allows us to complete our goal of visualizing a phylogenetic tree.

*In this exercise we will:*

  1. Launch an RStudio session, loading the sequence alignments created earlier
     in the course.
  2. Install an R package and create a phylogenetic tree from the alignment,
     saving it to a file.
  3. Save our work to the Data Store and terminate the application.

.. tip::

   **Why use VICE?**

   The Discovery Environment excels at running compute intensive analyses non-
   interactively. In other words, once you launch a job in the DE, you get an
   output, but to start a new analysis (for example to tweak parameters), you
   need to relaunch that job, and await new results. This style of computing
   allows you to run large jobs that require lots of resources. However,
   several analyses we’d like to do are interactive – we need to visualize and
   manipulate parameters on the fly – for example, creating a figure where you
   need to see and adjust the results of an upstream analysis. This kind of
   work is often done using tools like R and RStudio, or other programing tools
   such as Jupyter. Hence VICE!

.. raw:: html

           <div class="video-container">
           <iframe width="560" height="315" src="https://www.youtube.com/embed/PPFD7z4XOVc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
           </div>

----

**Input Data:**

.. list-table::
    :header-rows: 1

    * - Input
      - Description
      - Example
    * - - A folder of logs
        - clstalw.aln
        - fasta.aln
        - phylip_interleaved.aln
        - phylip_sequential.aln
      - The logs folder are log files returned with every Discovery Environment
        analyses. These can be useful for diagnosing failed analyses. All other
        files are outputs of the Muscle software and contain multiple sequence
        alignments in a variety of common formats.
      - View the example |muscle_output| folder.

*Getting VICE Access*
~~~~~~~~~~~~~~~~~~~~~~~~~

To minimize inappropriate use, VICE is a restricted service, currently
accessible from CyVerse US. You must request access to use.


  1. Visit the |CyVerse User Portal| and access the |services panel|; look for
     **DE – VICE** and select the **REQUST ACCESS** link.

     .. tip::

        Ensure that your CyVerse account is associated with an |ORCID| and a
        valid email address from an organization (i.e., .org, an educational
        institution with the .edu ending, or a government .gov). We will not
        grant access to commercial email addresses, e.g., @gmail.com @yahoo.com
        @msn.com etc.


*Launching a VICE application*
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


  1. If necessary, log into the CyVerse |Discovery Environment|.

  2. Click the |Data Icon| (Data Icon) and navigate to your **results** folder
     in the **tutorial_folder**; click the |Add folder icon| (Add Folder button) and create a folder called **rocker_output** inside your tutorial folder.

  3. Use this quicklaunch link |CyVerse_rocker_launch| or click on |Apps icon|
     (Apps icon) to launch the **Rocker RStudio Latest** App. You can also use
     the DE search bar to search for this application in the Apps category.

     .. tip::

        We provide and maintain the latest versions of R and RStudio made
        available by the |Rocker Project|.

  4. Launch the application and adjust the following:

      a. Under “Analysis Info”, for **Output Folder** click **Browse** and
         navigate to and select the **rocker_output** created above. click
         **Next**;
      b. For "Parameters", under “Input Folder” click **Browse** and navigate
         to the **tutorial_folder**, then the **results** folder and select the
         **muscle_output** folder where your Muscle analysis results should be
         located; click **Select Current Folder**; then **Next**;
      c. Click **Next** to skip Advanced Settings;
      d. Click **Launch Analysis** to launch your application

  5. In the navigation, click on the |Analyses icon| (Analyses) view. Your
     application will be listed as “Submitted” for a few minutes (usually just
     a few, but more depending on both the size of the application software and
     any imported datasets).

  6. When the Status of the launch is Running, click on the |Link out icon|
     (link out icon); a new tab where your VICE application will run should open in your browser.

     .. tip::

        Even when the application is in the 'Running' status, you may still have to wait some additional time if data is being transferred.


*Completing our analysis in R*
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Once you have your RStudio session, it will largely behave as would an RStudio
session running on your local Desktop. Some potential benefits of running
RStudio in VICE include more processing power (especially if you choose
additional resources at launch – see the Advanced Settings).  Since this
session is running on CyVerse hardware, transferring large data will also
happen at increased speed. To complete our analyses, we will install the |ape package| and compute a phylogenetic tree.

 .. tip::
   While you don’t need to be an expert R user to complete this section,
   familiarity with R will help since we won’t be going into specific detail
   about this example.

 .. tip::
  The data we loaded at launch of the VICE application will be in the ‘work’
  directory at ‘home’.

  1. From the R console, enter the following commands:

     .. code-block:: R

       # install and load the needed R library
       install.packages("ape")
       library(ape)

       #Read in the aligned DNA fasta file
       alignment <- read.FASTA ("~/work/data/input/muscle_output/fasta.aln", type="DNA")

       # Create a distance matrix for the sequences
       dist_mtrx <- dist.dna(alignment)

       #Compute a neighbor-joining tree
       nj_tree <- nj(dist_mtrx)

       # plot the tree
       plot.phylo(nj_tree)

       # save the tree to a file
       write.tree(nj_tree, file = "~/work/data/output/tree.newick")

       #OR save to your CyVerse Data Store directly in the file browser
       write.tree(nj_tree, file = "~/work/home/YOUR_CYVERSE_USERNAME/tutorial_folder/rocker_output/tree.newick")

  2. You should have visualized the resulting tree and also created the file
     ‘tree.newick’ in your work directory.


Terminating your VICE session and saving work to the Data Store
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Once you have completed your work, you can save your work to the Data Store and terminate your VICE application.

  .. tip::

     VICE applications typically have a 48-hour run time. Unless you request an
     extension, your application will automatically save outputs. It is
     recommended that you save your work to the Data Store before time expires.

  1. In the Analyses pane of the Discovery Environment, select your running
     RStudio VICE application.

  2. Under **More Actions**, select **Terminate**; confirm Termination on the
     pop-up notice.

  3. When the VICE application has the status completed, click the folder icon
     to view the folder on your data store where results will be written. It may
     take time for all outputs to be saved depending on the size of the data
     generated.

     .. tip::

       You don't have to terminate your analyses to save your work to the Data
       Store. From within the RStudio environment using the terminal, you can
       use iCommands to transfer data (See |Data Store Guide| on iCommands).
       RStudio itself allows you to download files and plots directly to
       your local computer. Use the Export features present in the file pane.

----

**Output/Results**

.. list-table::
    :header-rows: 1

    * - Output
      - Description
      - Example
    * - 'tree.newick'
      - A Newick-formatted phylogenetic tree file which can visualized using
        your choice of tools.
      - |Rstudio output|

----

Self Assessment Questions
````````````````````````````

  .. admonition:: Question
       :class: admonition-question

       Q1. What kind of applications are supported in VICE?

       A. Applications with their own graphical interface
       B. Open-source applications
       C. Applications that have interactive visualizations
       D. All of the above


       .. admonition:: Answer

          Correct answer is D


  .. admonition:: Question
       :class: admonition-question

       Q2. Which of the following are restrictions on using VICE?

       A. You must request access on the CyVerse user portal
       B. VICE applications have a 48-hour runtime limit
       C. You must install VICE applications yourself
       D. A and B
       E. C only


       .. admonition:: Answer

          Correct answer is D, you must request separate access to use VICE at
          the |services panel|. There is a default 48-hour run time but you can
          extend your time by requesting this in the Analysis view for the
          launched application.

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
