\_

\_ [Learning Center Home](http://learning.cyverse.org/)

Analysis with the Discovery Environment
=======================================

> ::: {.admonition}
> learning-objectives
>
> -   Understand basic analysis capabilities of the Discovery
>     Environment
> -   Find an app and launch an analysis
> -   Monitor analysis results
> -   Access analysis results
> :::

**Description:**

In this module, we introduce analyses in the CyVerse discovery
environment and demonstrate how to launch and monitor analyses in the
discovery environment.

> <div class="video-container">
> <iframe width="560" height="315" src="https://www.youtube.com/embed/LBtyt5bG2VY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
> </div>

------------------------------------------------------------------------

**Input Data:**

  Output                        Description                                                            Example
  ----------------------------- ---------------------------------------------------------------------- ---------
  **DE\_sample\_plants.fas**.   A FASTA file containing unaligned DNA sequences from a common locus.   

*Find a Tool and Launch an Analysis*
------------------------------------

1.  If necessary, log into the CyVerse .
2.  Click the (Data Icon) and navigate to your **results** folder in the
    **tutorial\_folder**; click the (Add Folder button) and create a
    folder called **muscle\_output** inside your tutorial folder.
3.  Click (Apps icon) from the DE workspace; search for
    **Muscle-3.8.31**; Click on the application name/link to open the
    application.
4.  Under "Analysis Info", for **Output Folder** click **Browse** and
    navigate to and select the **muscle\_output** created above. No
    other changes are needed at this step, but you may edit the analysis
    name or comments (optional).
5.  Under "Select input data" click Browse, then navigate to the
    **raw\_data** folder in the **tutorial\_folder** and select
    (checkbox) the **DE\_sample\_plants.fas** previously uploaded.
6.  Under "Sequence Type", select DNA.
7.  Under the optional "Advanced Settings", make no changes. If
    required, some analyses may be launched with requests for more
    minimum Resource Requirements, but this may cause those analyses to
    sit longer in the submission queue until a node matching those
    minimum requirements becomes available; click **Next**.
8.  Click **Launch Analysis**.
9.  You will receive a notification and be redirected to the Analyses
    page.

10. When Muscle analysis has the status **Completed**, you may click the folder

:   icon next to the analysis name, to navigate to and browse the
    outputs for this analysis. You may need to refresh your web browser
    to see the updated status.

------------------------------------------------------------------------

**Output/Results**

+-----------------------+-----------------------+-----------------------+
| Output                | Description           | Example               |
+=======================+=======================+=======================+
| -   A folder of logs  | The logs folder are   | View the example      |
| -   clstalw.aln       | log files returned    | folder.               |
| -   fasta.aln         | with every Discovery  |                       |
| -   phylip\_interleav | Environment analyses. |                       |
| ed.aln                | These can be useful   |                       |
| -   phylip\_sequentia | for diagnosing failed |                       |
| l.aln                 | analyses. All other   |                       |
|                       | files are outputs of  |                       |
|                       | the Muscle software   |                       |
|                       | and contain multiple  |                       |
|                       | sequence alignments   |                       |
|                       | in a variety of       |                       |
|                       | common formats.       |                       |
+-----------------------+-----------------------+-----------------------+

------------------------------------------------------------------------

### Self Assessment Questions

> ::: {.admonition .admonition-question}
> Question
>
> Q1. Which of the following are true about Docker containers?
>
> A.  They share the host OS
> B.  They have process-level isolation.
> C.  They are are heavyweight.
> D.  They have a startup time in the minutes range.
>
> ::: {.admonition}
> Answer
>
> Correct answer is A and B
> :::
> :::
>
> ::: {.admonition .admonition-question}
> Question
>
> Q2. Which of the following are incorrect about Docker containers?
>
> A.  Dockerfiles are a recipe for creating Docker images.
> B.  Docker containers are a collection of Dockerfiles.
> C.  Docker images get built by running a Docker command which uses the
>     Dockerfile.
> D.  Docker containers are running instances of a Docker image.
>
> ::: {.admonition}
> Answer
>
> The incorrect statement is B
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


