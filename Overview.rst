Overview
_________

AtlasXbrowser was built to help facilite the workflow of DBiT-sequencing. The problem AtlasXbrowser 
specifically solves is the conversion of tissue images into data that can be inputted directly
into a bioinformatics pipeline. 

.. figure:: /images/AtlasBrowser_Figure.png

As displayed in the image above, once images of the DBiT slide are prepared, the images are run through AtlasXbrowser
while the slide is sent off to be sequenced in paralell. Once the sequencing is preformed and all necessary insights
AtlasXbrowser have been obtained, both can be loaded back into the broswer to observe how the reads map onto the image.
From here any bioinformatic analysis can be preformed on the spatial data, such that UMAP or spatial clustering.


The two primary pieces of information AtlasXbrowser seeks to obtain are the coordinates of the four corners that
define the Region of Interest, as well as deliniating which sites of the image correspond to biological tissue.

AtlasXbrowser requires the loading of images taken of a glass slide from a DBiT Spatial Sequencing experiment.

From a distance a DBiT run works by:

* Adhering tissue sample of interest to glass slide.

   .. figure:: /images/TissueOnSlide.png
      :width: 300
      
      The tissue which DBiT sequencing is to be preformed on is fixed onto a glass
      slide in preparation for the procedure.

* Clamping chip A ontop of slide and flowing Chip A barcodes through tissue.

   .. figure:: /images/chipA.png

    The A chip flows DNA barcodes in vertical channels down the slide.
    Using the unique molecular identifier (UMI) associated with these barcodes allows to place an x coordinate on reads
    once the sequencing is preformed.

* Removing A chip and clamping B chip onto slide.

   .. figure:: /images/chipB.png

      The B chip flows DNA barcodes in horizontal rows across the slide.
      The UMI associated with each of these barcodes allows for a Y coordinate to be inferred from a read.

* From here pictures are taken of the glass slide, following the removal of the B chip.

   .. figure:: /images/barcoded.png
      
      After the B chip is removed, an X-Y plane has been created by the A chip barcodes flown across
      the tissue, and the B chip barcodes flown down the tissue. As such, any space on the tissue that
      has had both barcodes from the B and A chip flown through it, can have any reads sequencing from
      that region mapped back onto that spot in the image. These regions are called **Tixels**. 
      Tixels are the basis of how spatial information is encoded from the DBiT process.

* From here the two steps of loading the images into AtlasXbrowser as well as sequencing the tissue can begin in paralell.

   .. figure:: /images/AtlasBrowser_sequencing.png
      
      As neither step is reliant on the other, AtlasXbrowser can be used to generate information about the image
      such as the metadata corresponding to the experiment, the boundaries of the overlapping A and B chips, and
      classification of on and off tissue sites of the image, while the particular assay being run on the tissue
      can be sequenced. 

* Using the results of the sequencing in conjunction with the spatial information encoded by the DBiT process,
  any bioinformatic analysis can be run on the data, like the spatial clustering shown below.

   .. figure:: /images/SpatialClustering.png

