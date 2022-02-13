# Interactive Analyses

??? tip "Learning Objectives"

    - Request VICE access.
    
    - Launch and access VICE application.
  
    - Configure the VICE application and run an analysis.
    
    - Save the outputs of a VICE application to your Data Store.

**Description:**

The Visual Interactive Computing Environment () allows you to work with popular interactive data science applications such JupyterLab, RStudio, Linux shell and others. In this exercise we will cover a simple introductory use case that allows us to complete our goal of visualizing a phylogenetic tree.

*In this exercise we will:*

1.  Launch an RStudio session, loading the sequence alignments created earlier in the course.

2.  Install an R package and create a phylogenetic tree from the alignment, saving it to a file.

3.  Save our work to the Data Store and terminate the application.

??? tip "Why use VICE"

    The Discovery Environment excels at running compute intensive analyses non-interactively. 
    
    In other words, once you launch a job in the DE, you get an output, but to start a new analysis (for example to tweak parameters), you need to relaunch that job, and await new results. 
    
    This style of computing allows you to run large jobs that require lots of resources. However, several analyses we'd like to do are interactive -- we need to visualize and manipulate parameters on the fly -- for example, creating a figure where you need to see and adjust the results of an upstream analysis. 
    
    This kind of work is often done using tools like R and RStudio, or other programing tools such as Jupyter. Hence VICE!


<div class="video-container">
<iframe width="560" height="315" src="https://www.youtube.com/embed/PPFD7z4XOVc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

------------------------------------------------------------------------

## Input Data

| Location | File | Example |
|----------|------|---------|
| `muscle_output/`  | logs folder | [View the example `muscle_output/`](https://datacommons.cyverse.org/browse/iplant/home/shared/cyverse_training/cyverse_mooc/tutorial_folder/results/muscle_output){target=_blank} |
| `clstalw.aln` | |
| `fasta.aln` | | 
| `phylip_interleaved.aln` | | 
| `phylip_sequential.aln` | |

## Getting VICE Access


To minimize inappropriate use, VICE is a restricted service, currently accessible from CyVerse US. You must request access to use.

1.  Visit the and access the ; look for **DE -- VICE** and select the
>     **REQUST ACCESS** link.
>
>     ::: {.tip}
>     ::: {.admonition-title}
>     Tip
>     :::
>
>     Ensure that your CyVerse account is associated with an and a valid
>     email address from an organization (i.e., .org, an educational
>     institution with the .edu ending, or a government .gov). We will
>     not grant access to commercial email addresses, e.g., \@gmail.com
>     \@yahoo.com \@msn.com etc.
>     :::
>
*Launching a VICE application*
------------------------------

> 1.  If necessary, log into the CyVerse .
> 2.  Click the (Data Icon) and navigate to your **results** folder in
>     the **tutorial\_folder**; click the (Add Folder button) and create
>     a folder called **rocker\_output** inside your tutorial folder.
> 3.  Use this quicklaunch link or click on (Apps icon) to launch the
>     **Rocker RStudio Latest** App. You can also use the DE search bar
>     to search for this application in the Apps category.
>
>     ::: {.tip}
>     ::: {.admonition-title}
>     Tip
>     :::
>
>     We provide and maintain the latest versions of R and RStudio made
>     available by the .
>     :::
>
> 4.  Launch the application and adjust the following:
>
>     > a.  Under "Analysis Info", for **Output Folder** click
>     >     **Browse** and navigate to and select the **rocker\_output**
>     >     created above. click **Next**;
>     > b.  For \"Parameters\", under "Input Folder" click **Browse**
>     >     and navigate to the **tutorial\_folder**, then the
>     >     **results** folder and select the **muscle\_output** folder
>     >     where your Muscle analysis results should be located; click
>     >     **Select Current Folder**; then **Next**;
>     > c.  Click **Next** to skip Advanced Settings;
>     > d.  Click **Launch Analysis** to launch your application
>
> 5.  In the navigation, click on the (Analyses) view. Your application
>     will be listed as "Submitted" for a few minutes (usually just a
>     few, but more depending on both the size of the application
>     software and any imported datasets).
> 6.  When the Status of the launch is Running, click on the (link out
>     icon); a new tab where your VICE application will run should open
>     in your browser.
>
>     ::: {.tip}
>     ::: {.admonition-title}
>     Tip
>     :::
>
>     Even when the application is in the \'Running\' status, you may
>     still have to wait some additional time if data is being
>     transferred.
>     :::
>
*Completing our analysis in R*
------------------------------

Once you have your RStudio session, it will largely behave as would an
RStudio session running on your local Desktop. Some potential benefits
of running RStudio in VICE include more processing power (especially if
you choose additional resources at launch -- see the Advanced Settings).
Since this session is running on CyVerse hardware, transferring large
data will also happen at increased speed. To complete our analyses, we
will install the and compute a phylogenetic tree.

> ::: {.tip}
> ::: {.admonition-title}
> Tip
> :::
>
> While you don't need to be an expert R user to complete this section,
> familiarity with R will help since we won't be going into specific
> detail about this example.
> :::
>
> ::: {.tip}
> ::: {.admonition-title}
> Tip
> :::
>
> The data we loaded at launch of the VICE application will be in the
> 'work' directory at 'home'.
>
> 1.  From the R console, enter the following commands:
>
>     ``` {.sourceCode .R}
>     # install and load the needed R library
>     install.packages("ape")
>     library(ape)
>
>     #Read in the aligned DNA fasta file
>     alignment <- read.FASTA ("~/work/data/input/muscle_output/fasta.aln", type="DNA")
>
>     # Create a distance matrix for the sequences
>     dist_mtrx <- dist.dna(alignment)
>
>     #Compute a neighbor-joining tree
>     nj_tree <- nj(dist_mtrx)
>
>     # plot the tree
>     plot.phylo(nj_tree)
>
>     # save the tree to a file
>     write.tree(nj_tree, file = "~/work/data/output/tree.newick")
>
>     #OR save to your CyVerse Data Store directly in the file browser
>     write.tree(nj_tree, file = "~/work/home/YOUR_CYVERSE_USERNAME/tutorial_folder/rocker_output/tree.newick")
>     ```
>
> 2.  You should have visualized the resulting tree and also created the
>     file 'tree.newick' in your work directory.
> :::

Terminating your VICE session and saving work to the Data Store
---------------------------------------------------------------

Once you have completed your work, you can save your work to the Data
Store and terminate your VICE application.

> ::: {.tip}
> ::: {.admonition-title}
> Tip
> :::
>
> VICE applications typically have a 48-hour run time. Unless you
> request an extension, your application will automatically save
> outputs. It is recommended that you save your work to the Data Store
> before time expires.
> :::
>
> 1.  In the Analyses pane of the Discovery Environment, select your
>     running RStudio VICE application.
> 2.  Under **More Actions**, select **Terminate**; confirm Termination
>     on the pop-up notice.
> 3.  When the VICE application has the status completed, click the
>     folder icon to view the folder on your data store where results
>     will be written. It may take time for all outputs to be saved
>     depending on the size of the data generated.
>
>     ::: {.tip}
>     ::: {.admonition-title}
>     Tip
>     :::
>
>     You don\'t have to terminate your analyses to save your work to
>     the Data Store. From within the RStudio environment using the
>     terminal, you can use iCommands to transfer data (See on
>     iCommands). RStudio itself allows you to download files and plots
>     directly to your local computer. Use the Export features present
>     in the file pane.
>     :::
>
------------------------------------------------------------------------

**Output/Results**

  Output            Description                                                                                  Example
  ----------------- -------------------------------------------------------------------------------------------- ---------
  \'tree.newick\'   A Newick-formatted phylogenetic tree file which can visualized using your choice of tools.   

------------------------------------------------------------------------

### Self Assessment Questions

> ::: {.admonition .admonition-question}
> Question
>
> Q1. What kind of applications are supported in VICE?
>
> A.  Applications with their own graphical interface
> B.  Open-source applications
> C.  Applications that have interactive visualizations
> D.  All of the above
>
> ::: {.admonition}
> Answer
>
> Correct answer is D
> :::
> :::
>
> ::: {.admonition .admonition-question}
> Question
>
> Q2. Which of the following are restrictions on using VICE?
>
> A.  You must request access on the CyVerse user portal
> B.  VICE applications have a 48-hour runtime limit
> C.  You must install VICE applications yourself
> D.  A and B
> E.  C only
>
> ::: {.admonition}
> Answer
>
> Correct answer is D, you must request separate access to use VICE at
> the . There is a default 48-hour run time but you can extend your time
> by requesting this in the Analysis view for the launched application.
> :::
> :::

------------------------------------------------------------------------

**Fix or improve this documentation**

-   Search for an answer:
-   Ask us for help: click on the lower right-hand side of the page
-   Report an issue or submit a change:
-   Send feedback: [learning\@CyVerse.org](learning@CyVerse.org)

------------------------------------------------------------------------

\_ [Learning Center Home](http://learning.cyverse.org/)


